---
name: serhant-brand-skill
description: >
  Apply Ryan Serhant's Brand It Like Serhant system to personal-brand work:
  Formula V, the AND, three power adjectives, content matrix, On/Off table,
  authenticity connectors, 3 C's, and employer-as-chapter. Use when the user
  runs /serhant-brand-skill or $serhant-brand-skill, asks to assess a brand
  or X/LinkedIn/site, write or review a bio, H1, About, or post, plan a
  content matrix, or check whether a job or company is branding them.
when-to-use: >
  Brand It Like Serhant, personal brand, bio, About page, content matrix,
  assess @handle, review this post, employer branding, Formula V, the AND,
  /serhant-brand-skill, $serhant-brand-skill
argument-hint: "assess | draft | review | matrix | employer | <url or text>"
compatibility: Claude Code, Codex, Grok
metadata:
  short-description: Serhant brand system as an agent workflow
---

# Serhant brand skill

Standard `SKILL.md` bundle. Loads in Claude Code, Codex, and Grok.

Skill root = the directory that contains this file. Read `references/serhant.md` relative to that root. Invoke as `/serhant-brand-skill` (Claude, Grok) or `$serhant-brand-skill` (Codex).

You are running Serhant's system as a procedure, not summarizing the book.

**Rule 1:** if they do not control the brand, someone else will brand them.
The employer, the feed, and the first Google result all count as "someone else."

## Setup

1. Read `references/serhant.md` in this skill directory. That file owns the frameworks. Do not restate the book from memory if it contradicts that file.
2. Subject is whoever the user named. If they named nobody, the subject is the user.
3. If `references/subject.md` exists, read it. It owns that subject's vision, AND, adjectives, On/Off table, and surfaces. Do not invent a new H1 or AND that contradicts it unless they are explicitly rewriting the foundation. If it does not exist, work from conversation plus live fetch. Do not ask them to fill a profile before doing the work.
4. If assessing a live account or site, fetch it. Do not grade from memory.

## Route

Pick one. If the user did not pick, infer from the ask.

| Intent | Do |
|---|---|
| **assess** | Full three-phase audit. Output shape below. |
| **draft** | Write the artifact (bio, H1, About, post, pin). Run the 3-word test and On/Off before showing it. |
| **review** | Grade an existing post, feed, site, or bio. Keep / cut / rewrite. |
| **matrix** | Fill 3 characters × entertain / educate / encourage. Name one next post per cell or mark empty cells. |
| **employer** | Treat the job as a chapter. Check H1 vs subtitle, speak-the-book risk, what stays on *their* domain. |

Assessing a third party: run **assess**, then end with lessons for the user (not the third party) if a comparison was implied. Do not flatten the user into the third party.

## Assess

Score each item as **solid / leak / missing**. Cite a live post, bio line, or page. No vibes without a URL or quote.

Phase 1 — identity

- Formula V: viewpoint + values → a 3–5 year vision they would not tattoo, but would fight for
- The AND: profession AND unexpected pairing. Skill alone is not an AND
- Three power adjectives: no baseline words (honest, hardworking, dependable, passionate, authentic)
- Visuals last. Domain email over gmail. Face and lifestyle only after the sentence exists

Phase 2 — consistency

- Which of the Five Families is actually worked, and is it where buyers are
- Content matrix: 3 characters × entertain / educate / encourage
- Connector: Punch Line, Let Me Solve Your Problems, or Inspire on Demand — pick the primary
- Posts use numbers → lived story → CTA
- On/Off table exists. Four killers: lie, vent, faux expert, call-out

Phase 3 — shout

- Credibility (thought leadership from the AND, speaking, awards)
- Coverage (press, Big Unlock)
- Community as GLEE — speak *with*, not only *to*
- Partnerships pass values / strengths / audience. Own eggs before asking for coattails

Lead with what is true. Then the scorecard. Then 3 next actions, ordered.

## Draft

Order is mandatory: vision and AND first, copy second, visuals never first.

1. One sentence the stranger can retell. If `references/subject.md` has public lines, start there.
2. Status / job is a subtitle, never the H1.
3. Body follows: what I believed → what I ran → what happened → what to copy. Numbers in. Pedigree as proof under the sentence, not the sentence.
4. Test: does this represent the three power adjectives? If no, it can be a reply, not an original.
5. Test: On table, Off table, caution zone. A capability can be On; a crusade about that capability is Off unless they asked for the unfiltered register.
6. One CTA or none. Do not tack a follow-for-more onto a story that already landed.

## Review

For each piece, say:

- Matrix cell (character × offering) or **junk drawer**
- 3-word test pass/fail
- Killer risk, if any
- Keep / cut / rewrite, with the rewritten line if rewrite

If reviewing a whole site vs a feed vs a bio, say whether the three surfaces tell the same sentence. If they do not, name the sentence that should win.

## Employer

A job is a chapter. It is not Formula V.

- H1 stays the AND. Logo in the status line after ink is dry
- Speak-the-book test: can they publicly recommend a different product or approach when it is the honest answer? If no, they are a mouth. Say so.
- Name what must keep shipping on *their* domain so two years of confidential work do not become a silent chapter
- Rewrite On/Off for that comms policy. Do not wait until week one
- Side projects: one personal cake that does not compete. The rest go Past or Upstream

## Voice

Write like a direct editor. Complete sentences. Lead with the answer. No jersey-picking, no hustle-thread cadence, no "let's circle back on your personal brand."

If the subject file names a public register vs a private one, use the public register for homepage, pin, and employer-facing bio unless they asked for the private register.

## Attribution

Frameworks are from Ryan Serhant, *Brand It Like Serhant* (Hachette Go, 2024), distilled in `references/serhant.md`. Do not quote long passages. Do not claim the book as original work.
