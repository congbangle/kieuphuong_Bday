# 🌸 Birthday Website — Setup & Editing Guide

## Folder structure

```
your-project/
├── index.html          ← Main website file
├── _source/
│   ├── photo_01.jpeg   ← Photo 1 (Chapter 1)
│   ├── photo_02.jpeg
│   ├── photo_03.jpeg
│   ├── ...
│   ├── photo_40.jpeg   ← Photo 40 (Chapter 8)
│   └── music.mp3       ← Background music
└── README.md
```

---

## Part 1 — Upload to GitHub Pages (free hosting)

### Step 1: Create a GitHub account
Go to [github.com](https://github.com) and sign up for a free account if you don't have one.

### Step 2: Create a new repository
1. Click the **+** button at the top-right → **New repository**
2. Name it: `birthday` (or any name you like)
3. Set it to **Public**
4. Click **Create repository**

### Step 3: Upload your files
1. Inside your new repository, click **Add file** → **Upload files**
2. Drag and drop your entire project folder contents:
   - `index.html`
   - the `_source/` folder (with all photos + music inside)
3. Scroll down, write a commit message like `"first upload"`, then click **Commit changes**

### Step 4: Enable GitHub Pages
1. Go to your repository → click **Settings** (top menu)
2. Scroll down to the **Pages** section (left sidebar)
3. Under **Branch**, select `main` and folder `/root (root)`
4. Click **Save**
5. Wait about 1–2 minutes, then your site will be live at:
   ```
   https://YOUR-USERNAME.github.io/birthday/
   ```

> **Tip:** Share this link with her directly — it works on any phone browser, no app needed.

---

## Part 2 — Add your photos

### Naming your photos
Rename each of your 40 photos to match exactly:

| File name | Chapter | Slot |
|---|---|---|
| `photo_01.jpeg` | Chapter I | Photo 1 |
| `photo_02.jpeg` | Chapter I | Photo 2 |
| ... | ... | ... |
| `photo_05.jpeg` | Chapter I | Photo 5 |
| `photo_06.jpeg` | Chapter II | Photo 1 |
| ... | ... | ... |
| `photo_40.jpeg` | Chapter VIII | Photo 5 |

> **Important:** The file name must be lowercase with an underscore: `photo_01.jpeg` not `Photo1.jpg`.  
> If your photos are `.jpg` (not `.jpeg`), either rename them to `.jpeg` or open `index.html` and find every `photo_XX.jpeg` and change `.jpeg` to `.jpg`.

### Upload photos to GitHub
1. In your repository, click on the `_source` folder
2. Click **Add file** → **Upload files**
3. Select all 40 photos at once
4. Commit the changes

---

## Part 3 — Add background music

1. Rename your music file to exactly: `music.mp3`
2. Upload it into the `_source/` folder on GitHub (same as photos above)
3. On the live website, a small **play button** appears at the bottom-right corner — tap it to start the music

> **Note:** Due to browser rules, music cannot autoplay on mobile. The visitor must tap the play button once.

---

## Part 4 — Edit text content

Open `index.html` in any text editor (Notepad, VS Code, etc.).  
Look for comments marked with `✏️ EDIT:` — these are the spots you should change.

### Hero section (first screen)
```html
<!-- ✏️ EDIT: Change the title below -->
<h1 class="hero-h1 reveal d1">Happy<br><em>Birthday</em></h1>

<!-- ✏️ EDIT: Change the subtitle below -->
<p class="hero-sub reveal d2">To the girl who makes every ordinary moment feel like a painting worth keeping.</p>
```

### Chapter title & description
Each chapter looks like this — change the text inside the tags:
```html
<!-- ✏️ EDIT: Chapter title -->
<h2 class="ch-title">The Beginning<br><em>of Us</em></h2>

<!-- ✏️ EDIT: Chapter description -->
<p class="ch-desc">Every love story starts with a single, quiet moment neither of you plans for.</p>
```

### Bible verses
Each verse card looks like this:
```html
<!-- ✏️ EDIT: Bible verse -->
<div class="verse-card reveal d1">
  <p class="verse-text">Two are better than one, because they have a good return for their labor.</p>
  <span class="verse-ref">Ecclesiastes 4:9–10</span>
</div>
```
Change the text inside `<p class="verse-text">` and `<span class="verse-ref">`.

### Interlude (full-screen verse between chapters)
```html
<p class="interlude-q reveal">
  "She is worth far more than <em>rubies</em>."
  <span class="interlude-ref">Proverbs 31:10</span>
</p>
```
The word(s) inside `<em>...</em>` will appear in rose/pink color.

### Closing message
```html
<!-- ✏️ EDIT: Closing message -->
<h2 class="cl-h2 reveal">Here is to you,<br><em>my love</em></h2>
<p class="cl-body reveal d1">May this new year bring you all the warmth...</p>

<!-- ✏️ EDIT: Date -->
<p class="cl-date reveal d4">your birthday &middot; 2025</p>
```

### Photo slot labels
In `index.html`, scroll to the `<script>` section. You will see:
```js
{ file:'photo_01.jpeg', tint:'ta', label:'How we met' },
{ file:'photo_02.jpeg', tint:'tb', label:'First glance' },
```
Change the `label` text to name each photo however you like. This label only shows if the photo file is missing.

---

## Part 5 — Update files on GitHub (after edits)

After editing `index.html` locally:
1. Go to your repository on GitHub
2. Click on `index.html`
3. Click the **pencil icon** (Edit) at the top-right of the file preview
4. Paste your updated HTML content
5. Scroll down and click **Commit changes**

The site updates automatically within 1–2 minutes.

---

## Quick checklist before sharing the link

- [ ] All 40 photos named `photo_01.jpeg` through `photo_40.jpeg`
- [ ] All photos uploaded to the `_source/` folder on GitHub
- [ ] Music file named `music.mp3` and uploaded to `_source/`
- [ ] Text content (names, dates, verses) edited in `index.html`
- [ ] GitHub Pages is enabled (Settings → Pages)
- [ ] Tested on phone browser before sharing

---

*Made with love — powered by GitHub Pages*
