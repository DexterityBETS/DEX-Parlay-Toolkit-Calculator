# DEX Parlay Toolkit Calculator

A tiny, single‑file web app that turns **Last 5** and **Key 3** results into a single **Projection Line** using Rae’s 60/40 method. Built to be extremely simple and phone‑friendly.

> **Workflow:** Paste numbers → Projection appears. No public knobs. Math is handled internally.

---

## ✨ Features
- **Projection‑only UI**: Last 5, Key 3 → Projection Line
- **Auto‑calc** as you type (and a Compute button for manual tap)
- **60/40 blend** toward Last 5
- **Adaptive auto‑trim** (0% / 10% / 15%) per list using IQR
- **Light/Dark theme** with toggle (persists)
- **Mobile‑friendly inputs** (spaces **or** commas, comma chip for phones)

---

## 🧮 Formula (summary)
If both lists are present:

```
Projection = 0.60 * RobustMean(Last5) + 0.40 * RobustMean(Key3)
```

If only one list is present, the projection is simply the robust mean of that list.

**RobustMean(list)** trims outliers based on IQR:
- 0% if no outliers
- 10% if mild outliers
- 15% if extreme outliers

---

## 🚀 Quickstart (GitHub Pages)
These steps make your repo serve the tool at a public URL (so JavaScript runs everywhere).

1. **Create a repo** (e.g., `dex-parlay-toolkit`).
2. **Add files** to the repo root:
   - `index.html` → the app (use the file I sent you)
   - `README.md` → this file
3. **Enable Pages**  
   - Repo → **Settings → Pages**  
   - **Build and deployment**: *Deploy from a branch*  
   - **Branch**: `main` • **Folder**: `/root` → **Save`
4. **Open the site URL** GitHub shows (e.g.,  
   `https://<your-username>.github.io/dex-parlay-toolkit/`)

> Note: Viewing `index.html` inside the repo (GitHub’s file preview) does **not** execute JavaScript. Always use the **Pages URL** for the live app.

---

## 💻 Adding files (two ways)

### Option A — Web UI
1. Go to your repo on github.com → **Add file → Upload files**.
2. Drag in **`index.html`** and **`README.md`**.
3. Commit to `main`.  
4. Turn on **Pages** (see Quickstart step 3).

### Option B — Git (Terminal)
```bash
# 1) Make a new folder & init
mkdir dex-parlay-toolkit && cd dex-parlay-toolkit
git init -b main

# 2) Add files (copy index.html and README.md here first)
git add index.html README.md
git commit -m "Initial commit: DEX Parlay Toolkit Calculator"

# 3) Create repo on GitHub, then link & push
git remote add origin https://github.com/<your-username>/dex-parlay-toolkit.git
git push -u origin main
```

Then enable **Pages** as described above.

---

## 📱 How to use
1. Open your **Pages URL** in Safari/Chrome.
2. Paste **Last 5** numbers (`25 31 29 18 34`).
3. Paste **Key 3** numbers (`28 26 33`) — optional.
4. The **Projection Line** updates automatically (or tap **Compute**).  
   - Commas **or** spaces both work.
   - There’s a tiny **comma chip** if your phone keyboard hides “,”.

---

## 🧩 Customization (optional)
- **Branding**: Replace the embedded logo in `index.html` (search for `data:image/png;base64,`).
- **Blend**: Change `0.60` / `0.40` in the compute section.
- **UI text**: Update labels and footer as you prefer.

---

## 🛡️ Disclaimer
For internal/educational use only. No guarantees or warranties. Always verify lines and payouts.
