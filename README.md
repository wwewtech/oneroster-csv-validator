# oneroster-csv-validator

Validate OneRoster 1.1/1.2 CSV roster sets (manifest, users, classes, enrollments, orgs) for bulk vs delta correctness, GUID integrity, orphan links, and encoding traps before SIS/Clever import. Use when a school IT admin has a roster zip that fails import or needs pre-flight validation. Never invent SourcedIDs.

Bad roster files fail silently or, worse, delete students. Validate locally before anything touches the SIS or Clever.

## Links
- Live Showcase: https://wwewtech.github.io/oneroster-csv-validator
- Skills.sh: https://skills.sh/wwewtech/oneroster-csv-validator
- SKILL.md: [SKILL.md](./SKILL.md)

## Why use this skill?
Bad roster files fail silently or, worse, delete students. Validating OneRoster CSVs manually or debugging after a failed sync is tedious. This skill enables AI agents to accurately detect missing manifests, GUID orphan references, encoding issues, Excel corruption, and ensure bulk vs delta data discipline.

## Quick Installation

### 1. Via `skills.sh` / Vercel Skills CLI
```bash
npx skills add wwewtech/oneroster-csv-validator
```

### 2. Via Claude Code
```bash
claude skills add https://github.com/wwewtech/oneroster-csv-validator
```

### 3. For Google Antigravity
Clone or copy `SKILL.md` directly into your Antigravity skills directory:
```bash
# Windows
mkdir -p "$HOME\.gemini\config\skills\oneroster-csv-validator"
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o "$HOME\.gemini\config\skills\oneroster-csv-validator\SKILL.md"

# macOS / Linux
mkdir -p ~/.gemini/config/skills/oneroster-csv-validator
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o ~/.gemini/config/skills/oneroster-csv-validator/SKILL.md
```

### 4. For Cursor & Windsurf
Add `SKILL.md` to your workspace prompt context:
```bash
mkdir -p .cursor/skills/oneroster-csv-validator
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o .cursor/skills/oneroster-csv-validator/SKILL.md
```


## Core Concepts

- **Manifest first:** `manifest.csv` must exist at zip root.
- **Bulk vs delta discipline:** Bulk rows MUST NOT carry `dateLastModified`/`status`; delta rows MUST.
- **GUID integrity:** Every `sourcedId` referenced must be defined somewhere in the set.
- **Enrollment sanity:** Each class needs a primary teacher + at least one student.
- **Encoding traps:** Files MUST be UTF-8; tolerate and strip BOM.

## License
MIT © 2026 wwewtech (Pavel Lebedev)
