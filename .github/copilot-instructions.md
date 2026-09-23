# GitHub Copilot Instructions for awesome-python

awesome-python is a curated shortlist of Python projects. README.md is the single source of content truth; the website renders it to [awesome-python.com](https://awesome-python.com/).

**Authoritative documentation**:
- [AGENTS.md](AGENTS.md) — entry rules and curation principles
- [CONTEXT.md](CONTEXT.md) — terminology and structural definitions
- [CONTRIBUTING.md](CONTRIBUTING.md) — admission rules, quality requirements, entry format, ordering, review process
- [DESIGN.md](DESIGN.md) — website design system, typography, colors, layout, components, constraints

## Essential Copilot Instructions

### Before Making Changes

1. **Inspect relevant files** before editing — read the affected sections in the authoritative docs above.
2. **Follow established conventions** — AGENTS.md, CONTEXT.md, CONTRIBUTING.md, and DESIGN.md are binding.
3. **Preserve architecture** — do not alter structural rules, use-case caps, entry format, or design constraints.
4. **Make minimal, targeted changes** — avoid broad rewrites or scope creep.

### Development

- **Do not introduce unnecessary dependencies** — use existing tools (uv, Makefile targets).
- **Run appropriate validation after changes**:
  - README.md edits: verify format against CONTRIBUTING.md, rebuild with `make build`
  - Website/CSS changes: run `make build`, verify layout and responsiveness (see DESIGN.md constraints)
  - General changes: run `make test` and `make build`
- **Do not claim validation succeeded** unless actually run and passed.

### Security

- **Never expose or commit** API keys, tokens, credentials, `.env` contents, or other secrets.
- **Never replace environment-variable or GitHub Secrets usage** with hard-coded credentials.

### Reporting

**After any change, clearly report**:
- Which files changed and what changed in each
- Why the change was made
- Validation results (test/build pass or fail with error output)
- Any errors, incomplete work, or limitations

### Approval Required

Ask for approval before:
- Destructive operations or deleting substantial content
- Major structural changes (new sections, subcategories)
- Security configuration changes
- Modifying files outside the requested task scope

---

**For detailed rules**: See CONTRIBUTING.md (entry format, caps, displacement), DESIGN.md (website constraints), AGENTS.md (curation), and CONTEXT.md (terminology).
