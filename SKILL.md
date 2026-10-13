---
name: boolean-string-builder
description: Turns a pasted job description into ready-to-use candidate search strings for LinkedIn (Boolean), Google X-ray (site: operators), and GitHub (user search qualifiers plus a Google X-ray fallback). Use whenever someone pastes a job description, req, or role summary and wants Boolean strings, X-ray searches, sourcing strings, GitHub searches, or asks "how do I search for this role", even if they never say "Boolean".
---

# Boolean String Builder

Paste a job description, get search strings for three platforms, each with a one-line note on what it targets so it can be tightened or broadened fast.

## Step 1: Extract the search inputs

Read the JD and pull out, in a short table:

- **Core titles**: the title in the JD plus 4-8 titles people actually hold (e.g. "Backend Engineer", "Software Engineer", "Platform Engineer"). Include seniority variants.
- **Must-have skills**: 3-6 skills the JD treats as required. Group synonyms (e.g. "JavaScript" / "JS" / "TypeScript").
- **Nice-to-haves**: kept out of the main strings, used only in a "broaden" or "narrow" variant.
- **Location**: city, metro, and nearby areas. Note if the role is remote.
- **Exclusions**: titles or terms that flood results with wrong people (e.g. "recruiter", "intern", "student", "sales"). Only add exclusions that are clearly wrong for the role.
- **Seniority signal**: years of experience or level words, translated into title words (Senior, Staff, Lead, Principal).

Do not invent requirements that are not in the JD. If something important is missing (location, level), say so in one line and proceed with a sensible assumption stated out loud.

## Step 2: Build the strings

Always produce all three. Put each string in its own code block so it can be copied cleanly.

### LinkedIn (Boolean)
- Operators: `AND`, `OR`, `NOT` in capitals, quotation marks around phrases, parentheses to group.
- Structure: `(title variants) AND (skill group 1) AND (skill group 2) NOT (exclusions)`
- Provide a **Tight** version (titles AND 2-3 core skills) and a **Wide** version (fewer skill requirements, more title variants).
- Keep strings compact. If LinkedIn rejects or truncates a long string, split it into two searches instead of shrinking the logic.

### Google X-ray
- Use `site:linkedin.com/in` for profiles, with quoted titles and skills, plus a location word.
- Example shape: `site:linkedin.com/in ("backend engineer" OR "software engineer") ("Go" OR "Golang") "Austin"`
- Add a second string using `site:linkedin.com/in` with `intitle:` for the title if useful.
- Mention that Google results vary and the first page is usually the best signal.

### GitHub
GitHub has two different search surfaces. Use the right one and say which is which.
1. **GitHub user search** (github.com/search, type Users). Supports qualifiers such as `language:`, `location:`, `followers:`, `repos:`. Keywords match username, name, and email, so do not rely on it for bio text. Example: `language:go location:austin followers:>10 repos:>5`
2. **Google X-ray for GitHub profiles and READMEs**: `site:github.com "Austin" "backend" "Go"` for bio text, which GitHub's own user search does not cover well.
3. **GitHub repository search** (optional): find repos by topic or language and then look at contributors.

Only include GitHub strings when the role is technical. For non-technical roles, say GitHub does not apply and skip it.

## Step 3: Output format

1. A 5-line summary of what you extracted (titles, skills, location, exclusions).
2. LinkedIn: Tight and Wide.
3. Google X-ray: one or two strings.
4. GitHub: the strings that apply.
5. One line per string: what it targets and one tweak to try if too few or too many results.

## Rules

- Never fabricate candidates, company names, or numbers. This skill produces search strings only.
- Do not target protected characteristics (age, gender, ethnicity, religion, etc.) in any string.
- If the user pastes a very short or vague JD, ask one question (usually location or level) or proceed with stated assumptions.
- Adapt to the market: skilled trades roles lean on certifications, licenses, and union or trade-school keywords; tech roles lean on stack and language.
