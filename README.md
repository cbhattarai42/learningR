# 📘 Learn R — Interactive Beginner Tutorial

An interactive R tutorial that runs entirely in the browser — **no R installation required for students.**

Built with [R Markdown](https://rmarkdown.rstudio.com/) + [WebR](https://webr.r-wasm.org/), hosted free on [GitHub Pages](https://pages.github.com/).

---

## 🌐 Live Demo

> **https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/**

---

## 📁 File Structure

```
your-repo/
├── index.Rmd          ← Main tutorial (edit this to add content)
├── style.css          ← All visual styling
├── header.html        ← WebR JavaScript engine (loads in <head>)
├── footer.html        ← Page footer
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml ← Auto-renders & deploys on every git push
```

---

## 🚀 How to Host on GitHub Pages (Step-by-Step)

### Step 1 — Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it something like `learn-r` or `r-tutorial`
3. Set visibility to **Public**
4. Click **Create repository**

### Step 2 — Upload your files

**Option A — GitHub web interface (no Git needed):**
1. Open your new repo on GitHub
2. Click **Add file → Upload files**
3. Upload all files: `index.Rmd`, `style.css`, `header.html`, `footer.html`
4. Then create the folder `.github/workflows/` and upload `deploy.yml` inside it

**Option B — Git command line:**
```bash
git init
git add .
git commit -m "Initial commit: Learn R tutorial"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **GitHub Actions**
3. Click **Save**

### Step 4 — Wait for deployment (~2 minutes)

1. Go to the **Actions** tab in your repo
2. Watch the **Render & Deploy to GitHub Pages** workflow run
3. When it shows ✅ green, your site is live!

### Step 5 — Visit your site

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

---

## ✏️ How to Add New Content

Edit `index.Rmd`. The two key helper functions are:

### `example_block(code, id)` — Read-only demo

```r
```{r results='asis'}
example_block(
'x <- c(1, 2, 3)
mean(x)',
  id = "my_unique_id"
)
```
```

### `practice_block(placeholder, id, prompt, hint)` — Student writes code

```r
```{r results='asis'}
practice_block(
  placeholder = '# Write your code here\n',
  id          = "pr_unique_id",
  prompt      = "Calculate the mean of c(10, 20, 30).",
  hint        = "Use <code>mean()</code> on your vector."
)
```
```

**Important:** Every `id` must be **unique** across the whole document.

---

## 🔄 Updating Your Tutorial

Every time you push to the `main` branch, GitHub Actions automatically:
1. Renders `index.Rmd` → `index.html`
2. Deploys the new version to GitHub Pages

You never need to run R locally!

---

## 🎓 Chapters Included

| # | Topic |
|---|---|
| 1 | Welcome to R |
| 2 | Arithmetic |
| 3 | Variables |
| 4 | Data Types |
| 5 | Vectors |
| 6 | Built-in Functions |
| 7 | Data Frames |
| 8 | Visualization |

---

## 🛠️ Tech Stack

| Tool | Role |
|---|---|
| [R Markdown](https://rmarkdown.rstudio.com/) | Document authoring format |
| [WebR](https://webr.r-wasm.org/) | R engine compiled to WebAssembly, runs in browser |
| [GitHub Actions](https://github.com/features/actions) | Auto-renders Rmd to HTML on push |
| [GitHub Pages](https://pages.github.com/) | Free static site hosting |

---

## 📄 License

MIT — feel free to use and adapt for your own teaching!
