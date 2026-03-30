# Plan Template

When presenting a plan to the user for approval, always use this structure:

---

## Plan: <short title>

**Goal:** One sentence describing what this plan delivers.

**Branch:** `feat/<feature-name>` or `fix/<description>`

**Stack:** Language, framework, and key dependencies (if known).

**Tasks:**

| # | Task | Agent(s) |
|---|------|----------|
| 1 | ... | Tester → Developer → Reviewer |
| 2 | ... | Tester → Developer → Reviewer |

**Files to create:**
- `<path>` — purpose

**Files to modify:**
- `<path>` — what changes

**Test approach:** Brief description of what BDD scenarios will cover.

**Out of scope:** Anything explicitly not being done in this plan.

---

Wait for user to say "approved" or request changes before proceeding.
