# 📘 Learn R — Interactive Beginner Tutorial

An interactive R tutorial (21 chapters + file upload) that runs entirely in the browser using [WebR](https://webr.r-wasm.org/). No R installation required for students.

## 🌐 Live Site
> `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

---

## 📁 Files in This Package

```
learn-r/
├── index.Rmd                          ← Main tutorial (all 21 chapters)
├── navbar.html                        ← Top navigation bar
├── header.html                        ← WebR engine + package installer
├── style.css                          ← All styling
├── footer.html                        ← Page footer
├── data/
│   └── students.csv                   ← Sample dataset (Ch 17–21)
└── .github/
    └── workflows/
        └── deploy.yml                 ← Auto-render & deploy on push
```

---

## 🚀 Deploy to GitHub Pages (Step-by-Step)

### Step 1 — Create a public GitHub repo
Go to https://github.com/new → name it `learn-r` → **Public** → Create

### Step 2 — Upload the 5 root files
Click **Add file → Upload files**, drag and drop:
- `index.Rmd`
- `navbar.html`
- `header.html`
- `style.css`
- `footer.html`

Scroll down → **Commit changes**

### Step 3 — Upload the CSV data file
Click **Add file → Create new file**
Type in filename box: `data/students.csv` (the `/` creates the folder)
Paste the contents of `students.csv` → **Commit changes**

### Step 4 — Create the workflow file
Click **Add file → Create new file**
Type in filename box: `.github/workflows/deploy.yml`
Paste the contents of `deploy.yml` → **Commit changes**

### Step 5 — Enable GitHub Pages
Go to **Settings → Pages → Source → GitHub Actions** → Save

### Step 6 — Wait ~2 minutes
Go to **Actions tab** → watch the workflow turn green ✓

### Step 7 — Visit your site!
`https://YOUR-USERNAME.github.io/learn-r/`

---

## ✏️ Adding New Lessons

Edit `index.Rmd` using two helper functions:

```r
# Read-only example (students click Run):
example_block('mean(c(1,2,3))', id = "ex_unique_id")

# Editable practice block:
practice_block(
  placeholder = '# your starter code',
  id          = "pr_unique_id",
  prompt      = "What should students do?",
  hint        = "Optional hint with <code>inline code</code>"
)
```

Every `id` must be unique. After editing, commit → Actions auto-redeploys.

---

## 📦 Chapters

| # | Topic | # | Topic |
|---|---|---|---|
| 1 | Welcome to R | 13 | dplyr Verbs |
| 2 | Arithmetic | 14 | Pipes & Grouping |
| 3 | Variables | 15 | ggplot2 Basics |
| 4 | Data Types | 16 | ggplot2 Advanced |
| 5 | Vectors | 17 | Load GitHub Data |
| 6 | Built-in Functions | 18 | Descriptive Statistics |
| 7 | Data Frames | 19 | Correlation & t-test |
| 8 | Visualization | 20 | Linear Regression |
| 9 | If / Else | 21 | Curve Fitting & Plots |
| 10 | Loops | 22 | 📂 Upload Your Own Data |
| 11 | Write Functions | | |
| 12 | Lists | | |

---

## 🛠️ Tech Stack
- [R Markdown](https://rmarkdown.rstudio.com/) — document format
- [WebR](https://webr.r-wasm.org/) — R running in WebAssembly in the browser
- [GitHub Actions](https://github.com/features/actions) — auto-renders on push
- [GitHub Pages](https://pages.github.com/) — free static hosting

## 📄 License
MIT — free to use and adapt for your own teaching.
