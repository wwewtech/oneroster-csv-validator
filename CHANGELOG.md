# Changelog

All notable changes to the `oneroster-csv-validator` skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-09-22

### Initial Release — 1EdTech OneRoster CSV Pre-Flight Linter

#### Added
- **Master Skill (`SKILL.md`):** Complete validation specifications for OneRoster v1.1 and v1.2.
- **Relational Integrity Linter:** Foreign key verification across users, courses, classes, and enrollments.
- **Zero-Orphan Enforcement:** Detection of broken student and class linkages prior to import.
- **UTF-8 BOM Sanitizer:** Protection against Excel export encoding artifacts.
- **Bulk vs Delta Purity:** Strict column and timestamp separation between exchange modes.
- **Interactive Web Linter (`docs/index.html`):** In-browser CSV suite validator with zero student data exfiltration.
- **CI Validation:** Automated YAML frontmatter and SHA256 file symmetry verification.
