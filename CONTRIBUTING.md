# Contributing to OneRoster CSV Validator

We welcome contributions from district IT administrators, EdTech developers, and data engineers.

---

## Ways to Contribute

1. **Vendor Adaptations:** Add pre-flight validation rules for specific vendor targets (Clever, ClassLink, Canvas, Infinite Campus).
2. **Schema Extension (OneRoster v1.2):** Expand demographic, resource, and result table validations.
3. **Evals (`evals/evals.json`):** Contribute tricky real-world export edge cases (e.g. multi-line comments, foreign characters).

---

## Submission Guidelines

- Ensure byte-for-byte SHA256 symmetry between `./SKILL.md` and `./skills/oneroster-csv-validator/SKILL.md`.
- Maintain single-file self-containment in `SKILL.md`.
- Validate before opening a PR:
  ```bash
  python -c "import hashlib; assert hashlib.sha256(open('SKILL.md','rb').read()).hexdigest() == hashlib.sha256(open('skills/oneroster-csv-validator/SKILL.md','rb').read()).hexdigest(), 'Hash mismatch!'"
  ```
