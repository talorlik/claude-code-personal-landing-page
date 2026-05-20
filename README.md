# Personal Landing Page

A course assignment from the **AI Game Changer** program. The goal was to build
a personal landing page from scratch using AI tooling - no manual coding, just
prompts and iteration.

## Live Site

[https://talorlik.github.io/claude-code-personal-landing-page/](https://talorlik.github.io/claude-code-personal-landing-page/)

## How It Was Built

Everything was prompt-driven inside **Claude Code**. I described what I wanted -
layout, sections, content, styling - and iterated from there. No starter template,
no copy-paste.

The hero banner and profile photo were generated with **ChatGPT Images**, then
dropped in as static assets.

The page itself is plain **HTML and CSS** - no framework, no build step. A small
`main.js` injects structured JSON-LD data for SEO.

## What I Learnt

- **Prompting for structure first pays off.** Describing the layout and intent
  before asking for code produced cleaner results than jumping straight to
  "write me a page."

- **AI-generated images need direction.** Vague prompts give generic results.
  Specifying mood, color palette, and subject matter made the banner actually
  match the page.

- **CSS custom properties keep things consistent.** Claude reached for them
  naturally, and it made tweaking the color scheme trivial later.

- **Iteration is faster than perfection on the first prompt.** Getting something
  on screen quickly, then refining section by section, was more effective than
  trying to specify everything upfront.

- **Claude Code tracks context well.** It remembered design decisions made
  earlier in the session without me repeating them, which kept the output
  consistent across the whole page.
