# OneRoster CSV Validator — Global Launch & Distribution Kit

This kit contains high-engagement announcement templates to publish and distribute `oneroster-csv-validator` across EdTech, K-12 systems, and data engineering communities.

---

## 1. Twitter / X Viral Launch Thread

### Post 1 (Hook + Banner):
> EdTech engineers know the back-to-school nightmare:
>
> 200 school districts upload OneRoster CSV packages, and half crash your backend because `users.csv` has orphaned IDs or circular org trees.
>
> Today we're releasing **OneRoster CSV Validator**: an autonomous agent skill for bulletproof 1EdTech compliance 🧵👇
>
> `npx skills add wwewtech/oneroster-csv-validator`
> [Attach: assets/oneroster-banner.svg]

### Post 2 (The 8-Table Relational Graph):
> OneRoster is not a single CSV; it's a relational database split across 8 tables (orgs, users, courses, classes, enrollments, demographics, academicSessions, userProfiles).
>
> OneRoster CSV Validator enforces:
> - Relational foreign key integrity across all 8 files
> - Cycle detection in parentOrgId hierarchy
> - ISO 8601 UTC timestamp validation
> - Required header preservation & delimiter escaping (RFC 4180)

### Post 3 (Zero Ingestion Failures):
> Pre-validating district data saves customer onboarding engineers hours of manual troubleshooting.
> Runs locally with zero cloud dependencies.

### Post 4 (Install & Run):
> 📦 skills.sh: https://skills.sh/wwewtech/oneroster-csv-validator
> ⭐ GitHub: https://github.com/wwewtech/oneroster-csv-validator
> 🌐 Web Linter: https://wwewtech.github.io/oneroster-csv-validator/

---

## 2. Reddit (`r/edtech`, `r/k12sysadmin`, `r/dataengineering`, `r/ClaudeAI`)

### Title:
> **An open-source agent skill for validating 1EdTech (IMS Global) OneRoster 1.1 and 1.2 CSV exports**

### Body:
> Hey EdTech developers & sysadmins,
>
> If you integrate with district SIS software (PowerSchool, Infinite Campus, Skyward, Genesis), you know that OneRoster CSV export quality varies wildly between districts.
>
> We built **OneRoster CSV Validator** (https://github.com/wwewtech/oneroster-csv-validator), an agent skill (`SKILL.md`) that guides agents in:
> - Validating mandatory tables and required columns per OneRoster v1.1 / v1.2 specifications
> - Catching orphaned foreign keys across `enrollments.csv`, `users.csv`, and `classes.csv`
> - Detecting circular dependencies in organizational hierarchy trees
> - Generating human-readable audit reports and sanitized CSV outputs
>
> **Install:**
> ```bash
> npx skills add wwewtech/oneroster-csv-validator
> ```
>
> Web App: https://wwewtech.github.io/oneroster-csv-validator/
> Repo: https://github.com/wwewtech/oneroster-csv-validator

---

## 3. Pull Request Submission Template

```markdown
## Summary
Adds the `oneroster-csv-validator` skill to `skills/oneroster-csv-validator/SKILL.md`.

### Overview
`oneroster-csv-validator` equips autonomous coding agents with schema rules, relational integrity validation, and anomaly detection for 1EdTech / IMS Global OneRoster 1.1 and 1.2 CSV bundles.

### Features
- Relational foreign key verification across all 8 standard OneRoster tables
- Cycle detection in parent-child organizational hierarchies
- Strict RFC 4180 delimiter escaping and header schema linting
- Timestamp formatting and role-based enumeration validation

### Validation
Passes all CI checks with 0 errors and 0 warnings. Verified against comprehensive schema and relational evals.
```
