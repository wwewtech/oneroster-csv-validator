# Complete Distribution & Collections Directory

This registry catalogs **`oneroster-csv-validator`** across every AI agent directory, Cursor rule repository, Claude Code showcase, awesome-list, and community distribution channel.

---

## 1. Official Registries & Package Hubs

| Platform | Type | Link / Command | Submission Method | Status |
| :--- | :--- | :--- | :--- | :--- |
| **skills.sh** (Vercel) | Universal CLI Registry | [skills.sh/wwewtech/oneroster-csv-validator](https://skills.sh/wwewtech/oneroster-csv-validator) | Git Tag / Auto-Indexed | Indexed & Verified |
| **Anthropic Official Skills** | Show & Tell Showcase | [Anthropic Skills Forum](https://github.com/anthropics/skills/discussions) | Official Community Forum | Ready to Publish |
| **Cursor Directory** | Cursor Rules Hub | [cursor.directory](https://cursor.directory/) | Form / GitHub PR | Ready to Submit |
| **Awesome Claude** | Claude Code Hub | [awesomeclaude.ai](https://awesomeclaude.ai/) | "Submit Resource" / PR | Ready to Submit |
| **Cline Rules Hub** | Roo Code / Cline Directory | [clinerules.org](https://clinerules.org/) | GitHub PR | Ready to Submit |
| **Smithery.ai** | Agent Capabilities Registry | [smithery.ai](https://smithery.ai/) | Indexed via `smithery.json` | Manifest Configured |
| **Glama.ai** | Agent Tools & MCP Hub | [glama.ai/mcp](https://glama.ai/mcp) | Web Submission | Ready to Submit |

---

## 2. GitHub Awesome-Lists Submissions & PR Tracker (20 Curated Targets)

| Repository | Focus / Category | Status |
| :--- | :--- | :--- |
| **sickn33/agentic-awesome-skills** (46,500+ ⭐) | AAS Core / `skills/oneroster-csv-validator/SKILL.md` | Prepared / Active |
| **ComposioHQ/awesome-claude-skills** (75,000+ ⭐) | `Education, EdTech & Data Standards` | Prepared / Active |
| **heilcheng/awesome-agent-skills** (6,200+ ⭐) | `EdTech & Data Validation` | Prepared / Active |
| **VoltAgent/awesome-agent-skills** (34,500+ ⭐) | `Community Skills -> Education & Data Validation` | Prepared / Active |
| **PatrickJS/awesome-cursorrules** (10,000+ ⭐) | `EdTech / Data Standards / Python` (`rules/oneroster-csv-validator.mdc`) | Prepared / Active |
| **BehiSecc/awesome-claude-skills** (10,000+ ⭐) | `Education & Enterprise Integration` | Prepared / Active |
| **rohitg00/awesome-claude-code-toolkit** (2,300+ ⭐) | `Skills -> Data Validation` | Prepared / Active |
| **Prat011/awesome-llm-skills** (1,700+ ⭐) | `EdTech & Relational Data Validation` | Prepared / Active |
| **libukai/awesome-agent-skills** (5,100+ ⭐) | `精选技能 -> 教育科技与数据校验 (EdTech & Data Validation)` | Prepared / Active |
| **skillmatic-ai/awesome-agent-skills** (670+ ⭐) | `Popular Collections / EdTech` | Prepared / Active |
| **philipbankier/awesome-agent-skills** | `Domain-Specific -> Education Systems` | Prepared / Active |
| **karanb192/awesome-claude-skills** | `Education & Standards Compliance` | Prepared / Active |
| **spencerpauly/awesome-cursor-skills** | `Data Standards & Schema Rules` | Prepared / Active |
| **jqueryscript/awesome-claude-code** (510+ ⭐) | `Agent Skills -> Education Tools` | Prepared / Active |
| **awesome-edtech** | `Educational technology software and data standards` | Target Catalog |
| **awesome-education** | `Open education tools and SIS/LMS integrations` | Target Catalog |
| **awesome-csv** | `CSV validation, relational integrity, tabular data` | Target Catalog |
| **awesome-clever** | `Clever / ClassLink / OneRoster interoperability tools` | Target Catalog |
| **awesome-interoperability** | `Data exchange & educational standards` | Target Catalog |
| **awesome-database** | `Relational schema verification, orphaned foreign keys` | Target Catalog |

---

## 3. High-Traffic Launch Channels

### 1. Hacker News (Show HN)
- **Title:** `Show HN: OneRoster CSV Validator – Agent skill for 1EdTech / IMS Global roster validation`
- **URL:** `https://wwewtech.github.io/oneroster-csv-validator/`
- **Body:**
  ```text
  Hey HN!

  Every K-12 EdTech platform integrates with school district Student Information Systems (PowerSchool, Infinite Campus, Skyward) using the 1EdTech (IMS Global) OneRoster CSV format.

  In real deployments, districts upload ZIP archives with missing users.csv, orphaned enrollments, circular parent org hierarchies, or malformed ISO 8601 timestamps—crashing back-office sync workers.

  We built oneroster-csv-validator (https://github.com/wwewtech/oneroster-csv-validator), an open-source agent skill (SKILL.md) that guarantees strict OneRoster 1.1 / 1.2 compliance:
  1. 8-table relational integrity checks (orgs, users, courses, classes, enrollments, etc.)
  2. Orphaned foreign key detection (e.g. enrollment referencing non-existent classSourcedId)
  3. Circular organization hierarchy prevention (parentOrgId recursion detection)
  4. Header ordering, RFC 4180 delimiter escaping, and UTF-8-BOM sanitization

  Install via Skills CLI:
  $ npx skills add wwewtech/oneroster-csv-validator
  Or for Claude Code:
  $ claude skills add https://github.com/wwewtech/oneroster-csv-validator

  Interactive browser-based validator: https://wwewtech.github.io/oneroster-csv-validator/
  ```

### 2. Product Hunt
- **Tagline:** `Autonomous 1EdTech OneRoster 1.1/1.2 CSV validation & relational linting`
- **Description:** `Validate school district OneRoster CSV files, eliminate orphaned enrollments, catch circular org hierarchies, and ensure seamless LMS/SIS roster syncing.`
- **Tags:** `Education`, `EdTech`, `Developer Tools`, `Data Validation`, `Open Source`.

### 3. Reddit (`r/edtech`, `r/k12sysadmin`, `r/dataengineering`, `r/ClaudeAI`)
- **r/edtech:** `Why OneRoster CSV imports fail in production (and how to validate all 8 tables before ingestion)`
- **r/k12sysadmin:** `Free open-source OneRoster 1.1 & 1.2 CSV validator: relational integrity and schema checker`
- **r/ClaudeAI:** `[Skill] OneRoster CSV Validator: Guarantee 1EdTech specification compliance in EdTech pipelines`

### 4. Russian Tech Ecosystem (Хабр & Telegram)
- **Хабр:** «Валидация OneRoster CSV (1EdTech): как проверять целостность реляционных данных в EdTech перед синхронизацией со школами»
- **Telegram:** `@edtech_russia`, `@data_engineering_ru`, `@developers_ed`, `@neuro_dev`.

---

## 4. Universal 1-Click Installation Cheatsheet

```bash
# 1. skills.sh (Universal Skills CLI)
npx skills add wwewtech/oneroster-csv-validator

# 2. Claude Code
claude skills add https://github.com/wwewtech/oneroster-csv-validator

# 3. Google Antigravity
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o ~/.gemini/config/skills/oneroster-csv-validator/SKILL.md

# 4. Cursor (.cursor/rules/ or .cursor/skills/)
mkdir -p .cursor/skills/oneroster-csv-validator
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o .cursor/skills/oneroster-csv-validator/SKILL.md

# 5. Windsurf / Cascade
mkdir -p .windsurf/skills/oneroster-csv-validator
curl -sL https://raw.githubusercontent.com/wwewtech/oneroster-csv-validator/main/SKILL.md -o .windsurf/skills/oneroster-csv-validator/SKILL.md
```
