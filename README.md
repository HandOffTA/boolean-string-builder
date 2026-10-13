# Boolean String Builder

> Part of the [HandOffTA](https://github.com/HandOffTA) portfolio: practical AI tools for hiring teams.

## What It Does

Paste a job description and get ready-to-use search strings for **LinkedIn (Boolean)**, **Google X-ray**, and **GitHub**. Every string comes with a short note on what it targets and how to tweak it.

## The Problem It Solves

Writing good Boolean strings takes time and practice. Recruiters often reuse the same tired strings, miss relevant title variations and skills, or skip platforms like GitHub entirely. The result is thinner pipelines and slower sourcing.

## Who It's For

Sourcers, recruiters, and recruiting coordinators who source candidates directly, plus hiring managers who want to see what the talent pool looks like.

## How It Works

1. **Paste the job description.**
2. **Extract what matters.** Core titles, alternate titles, must-have skills, nice-to-haves, location, seniority signals, and exclusions.
3. **Generate platform-specific strings.** LinkedIn Boolean (tight and wide), Google X-ray (`site:` operators), and GitHub (user search qualifiers plus an X-ray fallback).
4. **Review and tweak.** Each string notes what it targets so you can tighten or broaden fast.

## How To Use It

- **Claude Skill:** add `SKILL.md` to your Claude skills, then paste a job description and ask for search strings.
- **Any AI chat:** paste the contents of `SKILL.md` as instructions, then paste your job description.

## Tools Used

- Claude Skill (runs inside Claude / Claude Code), or Claude API

## Status

🟢 In active use

- Last updated: October 2026

---

**Questions or want to see a demo?** Reach out at [handoffta@proton.me](mailto:handoffta@proton.me) or visit [handoffta.com](http://handoffta.com).
