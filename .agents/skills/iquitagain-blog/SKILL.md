---
name: iquitagain-blog
title: Authoring & Archiving for iquitagain.com
description: Author, format, review, and publish health, fitness, running, and weight loss reflections for Dale Sackrider's journal at iquitagain.com. Use when drafting new posts, formatting Astro markdown frontmatter, and publishing via GitHub Actions to Cloudflare.
version: 1.0.0
author: Dale Sackrider
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Health, Fitness, Running, Weight-Loss, Diabetes, Personal-Journal, IQuitAgain, Astro]
    category: domain
    requires_toolsets: []
---

# Authoring & Archiving for iquitagain.com

## Overview
This skill guides agents in writing, reviewing, archiving, and publishing journal entries, training logs, and health reflections for **I Quit... Again!** at [iquitagain.com](https://iquitagain.com).

The site is built with **Astro 5 + Tailwind CSS v4**, version-controlled in Git, and hosted on **Cloudflare Edge**.

---

## 🏃 Editorial Style & Voice

### Purpose & Audience
* **Mission:** Candid, unfiltered reflections on health, habit change, running, weight loss, diabetes management, setbacks, and persistence.
* **Tone:** Honest, humble, self-deprecating when appropriate, resilient, practical, and grounded in real-world struggle and progress.
* **Authors:** Dale Sackrider (primary), with occasional contributions from Albert Tubbs, Stephanie Sackrider, and Jason Fisher.

---

## 📁 Repository & File Structure

* **Project Root:** `/Users/skippy/repos/iquitagain-com`
* **Content Directory:** `/Users/skippy/repos/iquitagain-com/src/content/blog/`
* **Media Directory:** `/Users/skippy/repos/iquitagain-com/public/wp-content/uploads/`
* **GitHub Repository:** `https://github.com/dsackr/iquitagain-com`
* **Live Site:** `https://iquitagain.com`

---

## 📝 Post Format Specification

Every post is a Markdown file located at `/Users/skippy/repos/iquitagain-com/src/content/blog/<slug>.md`.

### Frontmatter Schema
```yaml
---
title: "Title of Post"
description: "A concise 1-2 sentence summary under 160 characters."
pubDate: "YYYY-MM-DD"
author: "Dale Sackrider"
draft: false
tags: ["Running", "Weight Loss Journal", "Diabetes"]
---
```

---

## 🚀 Publishing Workflow

### 1. Draft the Post
Create `/Users/skippy/repos/iquitagain-com/src/content/blog/<slug>.md` with frontmatter and Markdown body.

### 2. Verify Build Locally
```bash
cd /Users/skippy/repos/iquitagain-com
npm run build
```

### 3. Commit and Push to GitHub (Automated CI/CD)
Pushing to `main` automatically triggers GitHub Actions to build and deploy to Cloudflare Edge:
```bash
cd /Users/skippy/repos/iquitagain-com
git add .
git commit -m "Publish: <Title of Post>"
git push origin main
```
