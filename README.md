# 10 Lives Studios — Email Signature Builder

A static, client-side tool for creating unified 10 Lives Studios email signatures.
Open the page, tweak your details, copy into Gmail. **Nothing is stored** and any
number of people can use it at once.

**Live:** https://jayhawkrules.github.io/10lives-signature/

---

## How to update this tool

The live site **rebuilds automatically** from this repo's `main` branch — any change
that lands here goes live in about 30 seconds. There is no separate "deploy" step.

There are three ways to make a change, easiest first:

### 1. Ask Claude (easiest)
Just describe the change in plain English, e.g.:
- "Change the London office address to …"
- "Add a Chicago office to the standard template"
- "Swap in the new logo"
- "Add Bluesky as a social platform option"

Claude edits the file, pushes it, and confirms it's live. You don't touch anything.

### 2. Edit on GitHub.com (good for quick text fixes, works on phone)
1. Open the repo: https://github.com/jayhawkrules/10lives-signature
2. Click **`index.html`**
3. Click the **pencil ✏️ (Edit)** icon
4. Make your change → **Commit changes**
5. Wait ~30 seconds — the live site updates itself.

### 3. Edit locally on the Mac
The repo lives at `~/10lives-signature`.
```bash
cd ~/10lives-signature
# edit index.html (or files in assets/)
git add -A
git commit -m "Describe your change"
git push
```

---

## What's in here

| File | What it controls |
|------|------------------|
| `index.html` | The entire app — the form, the layout, **and the company standard everyone starts from**. |
| `assets/logo.js` | The 10 Lives logo (embedded image). Swap this to change the logo. |
| `assets/brands.js` | The social-media brand icons + which platforms are offered. |
| `assets/qrcode.js` | The QR-code library (no need to touch this). |

### Changing the company standard
The values every person starts with — offices, website, company social links,
brand colors, the confidentiality disclaimer — all live in **one block near the top
of `index.html` labeled `COMPANY_DEFAULTS`**. That's the single place to edit to
change what the whole team sees by default.

---

## Good to know

- **It's a public page.** GitHub Pages free hosting requires a public repo. It's just
  a signature generator with public brand info, so that's expected — but anyone with
  the link can open it.
- **Nothing is saved.** No logins, no database, no cookies. Each visit is a clean
  slate. That's by design.
- **Gmail is the primary target.** The embedded logo and icons paste perfectly into
  Gmail. For bulletproof rendering in Outlook / Apple Mail too, move the images to
  hosted URLs (a future enhancement — just ask).
- **Custom domain** (e.g. `signatures.10livesstudios.com`) can be added anytime.
