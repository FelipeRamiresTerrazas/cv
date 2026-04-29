# CV Writing Instructions

## Voice and Authenticity

These CVs belong to a real person. Every word must sound like it was written by that person, not by an AI. When in doubt, write simpler.

## Characters to NEVER Use in CV Content

The following characters are AI writing tells. Do not use them in any bullet point, summary, or prose text:

- `---` (LaTeX em-dash used as a sentence connector): replace with a comma, colon, or just rewrite the sentence
- `--` as a prose dash: only allowed in date ranges like `Jul 25 -- Present`
- `_` (underscore) in any visible text
- Excessive hyphenated compound modifiers stacked together (e.g. "end-to-end data product lifecycle" chained with more hyphens)

**Good:** `Architected Snowflake infrastructure from the ground up, defining RBAC policies and schema design to serve as the system of record.`  
**Bad:** `Architected Snowflake infrastructure from the ground up---defining RBAC policies, warehouse sizing, and schema design to serve as the system of record.`

**Good:** `Owned the analytics product lifecycle for risk operations: gathering stakeholder requirements, designing data marts, and delivering dashboards.`  
**Bad:** `Owned the analytics product lifecycle for risk operations---gathering stakeholder requirements, designing data marts, and delivering dashboards.`

## Other Style Rules

- Bullet points must start with a strong action verb (past tense for old roles, past or present for current)
- No bullet should start with "Led the" three times in the same job block — vary the verbs
- Quantify impact where it is real and documented; do not invent numbers or inflate claims
- Keep the headline as written by the user — do not change the job title in the header without explicit instruction
- Do not add skills, tools, certifications, or experience that are not already present in other CV versions
- Do not fabricate projects, outcomes, or responsibilities

## Page Layout

- Every CV must fit on exactly **one page** — no exceptions
- The page must also look full and well-used: do not leave large blank areas at the bottom
- If content overflows, tighten in this order: shorten bullet text, reduce bullet count in older/less relevant roles, compress the summary, reduce margins (minimum 0.42in), tighten `\titlespacing` and `topsep` values
- If content is too short, expand bullet text, add a bullet to the most relevant role, or widen margins slightly
- Always recompile and verify page count after edits

## LaTeX-specific

- `---` and `--` in LaTeX **comments** (e.g. `% --- SPLIT HEADER ---`) are fine; this rule only applies to visible body text
- Date ranges use `--` (en-dash): `Jul 25 -- Present` — keep as is
- The `\titlerule` separator is fine; do not alter document structure
