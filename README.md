# btech-theory-2026

Course site for B.Tech Theory, built as a static Jekyll site on GitHub Pages using the **Just the Docs** theme. Search, math rendering, tutorials, assignments, and marks are all covered — no server or database required.

## 1. Create the repository

1. Go to the [Just the Docs template](https://github.com/just-the-docs/just-the-docs-template) and click **Use this template → Create a new repository**.
2. Name it `btech-theory-2026` (or whatever you like) under your own GitHub account.
3. Delete everything the template generated and copy in the files from this folder instead — or just replace the equivalent files one by one (`_config.yml`, `index.md`, etc.).

## 2. Enable GitHub Pages via Actions

In your new repo: **Settings → Pages → Build and deployment → Source → GitHub Actions.**

The included workflow at `.github/workflows/pages.yml` builds and deploys automatically on every push to `main`. First build usually takes 1–2 minutes; check the **Actions** tab for progress.

## 3. Replace the placeholders

Search the repo for these and swap in your real details:

| Placeholder | Where | Replace with |
|:--|:--|:--|
| `YOUR-USERNAME` | `_config.yml`, `contact.md` | your GitHub username |
| `REPLACE-WITH-YOUR-INVITE-LINK` | `assignments.md` | your GitHub Classroom invite link |
| `REPLACE-WITH-YOUR-FORM-ID` | `assignments.md` | your Google Form's embed URL |
| `REPLACE-WITH-SHEET-ID` | `marks.md` | your Google Sheet's ID (only if using the embedded-sheet option) |
| `replace-with-your-email@...` | `contact.md` | your actual email |
| all `.pdf` filenames | `tutorials.md`, `assignments.md`, `materials.md` | files you actually upload to `assets/materials/` |

## 4. Add your first files

Drop PDFs, datasets, etc. into `assets/materials/` and link them from any Markdown page:

```markdown
[Download Tutorial 1 PDF](/assets/materials/tut1.pdf)
```

## 5. Local preview (optional)

If you want to preview changes before pushing:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Structure

```
btech-theory-2026/
├── _config.yml          # theme, search, MathJax, nav config
├── index.md              # home page
├── syllabus.md
├── tutorials.md           # weekly tutorial question sheets
├── assignments.md         # GitHub Classroom + embedded Google Form
├── materials.md           # reference PDFs / datasets
├── marks.md               # Secret-ID results table
├── contact.md             # TA info & office hours
├── assets/materials/       # actual PDF/CSV files go here
└── .github/workflows/pages.yml   # auto build + deploy
```

## Privacy note

Never commit roll numbers, names, or grades together in this (public) repository. Use a Secret ID scheme (see `marks.md`) or an access-restricted Google Sheet embedded via `<iframe>`.
