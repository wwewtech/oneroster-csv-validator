---
name: oneroster-csv-validator
description: Validate OneRoster 1.1/1.2 CSV roster sets (manifest, users, classes, enrollments, orgs) for bulk vs delta correctness, GUID integrity, orphan links, and encoding traps before SIS/Clever import. Use when a school IT admin has a roster zip that fails import or needs pre-flight validation. Never invent SourcedIDs.
---

# OneRoster CSV Validator

Bad roster files fail silently or, worse, delete students. Validate locally before anything touches the SIS or Clever.

## Scope

- OneRoster 1.1 and 1.2 CSV binding (bulk and delta).
- Core files: manifest.csv, orgs.csv, users.csv, classes.csv, enrollments.csv, courses.csv, academicSessions.csv (+ demographics.csv).
- Out of scope: REST API bindings, gradebook/results files beyond basic presence checks.

## When NOT to use

- Live Clever/SIS sync debugging inside vendor dashboards — different surface.
- Non-OneRoster CSVs (generic SIS exports) — validate structure only, no spec claims.

## Method

1. **Manifest first.** `manifest.csv` must exist at zip root (not inside a folder). It must list exactly the files present. Missing manifest under 1.1/1.2 rules = stop, report, do not guess versions.
2. **Bulk vs delta discipline.** One file = one mode. Bulk rows MUST NOT carry `dateLastModified`/`status`; delta rows MUST. Mixed file = invalid, fail fast.
3. **Required core set.** Bulk exchange needs the core files present (manifest, orgs, users, classes, courses, enrollments, academicSessions). Report any absent file explicitly.
4. **GUID integrity.** Every `sourcedId` referenced (enrollments → users/classes, classes → orgs/courses) must be defined somewhere in the set. List orphans with file + line number. Never invent missing IDs.
5. **Enrollment sanity.** Each class needs a primary teacher + at least one student; `status=active` + `enabledUser=true` required for sync; `tobedeleted`/`inactive` rows do not sync — report them separately, do not silently drop.
6. **Encoding traps.** Files MUST be UTF-8; tolerate and strip BOM (`EF BB BF`). Never open roster CSVs in Excel and re-save: it strips leading zeros (`00123` → `123`), which deletes one student and creates another. Recommend CSVEdit/Sublime/TextEdit instead.
7. **Duplicates.** Flag duplicate `sourcedId` values within a file and the same student under two IDs (name+DOB fuzzy match) for human review.

## Output

```markdown
## OneRoster validation — [archive name]
- Spec version assumed: [1.1 / 1.2 / unknown]
- Mode: [bulk / delta / MIXED-INVALID]
- Files: [present/missing list]
- Orphan references: [file:line → missing id, ...] or none
- Enrollment issues: [...]
- Encoding issues: [...]
- Verdict: [IMPORTABLE / FIXABLE (list) / INVALID]
```

## Honesty rules

- Quote exact spec requirements with version; if unsure between 1.1 and 1.2 behavior, say which version you assumed.
- Never auto-"fix" files in place: produce a findings report; write corrected copies only on explicit request, as new files.
- Sources: `imsglobal.org OneRoster 1.1/1.2 CSV binding`, Clever OneRoster SFTP support docs.
