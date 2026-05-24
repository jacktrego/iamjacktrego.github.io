[README.md](https://github.com/user-attachments/files/28198032/README.md)
# iamjacktrego.com — Site Rebuild

## File Structure

```
/
├── index.html              ← Homepage (the intro text)
├── main.css                ← All styles, one file
├── pages/
│   ├── producer.html       ← Creative Producer (shell, awaiting case studies)
│   ├── writer.html         ← Writing: Poems, Substack, Essays, Research
│   ├── reader.html         ← All reading lists 2015–2026, hover notes ready
│   └── about.html          ← Bio, Model, Resume
├── images/                 ← Drop your images here (icon 3.ico, aboutPic.gif, project images)
└── documents/              ← Drop your PDFs here (resume, poems, research papers)
```

## How to Deploy

This is a drop-in replacement for your existing GitHub Pages repo.

1. **Back up your current repo** — download or branch first.
2. Replace `index.html` and `main.css` at the root.
3. Replace or add the `pages/` folder with the four new HTML files.
4. Your existing `images/` and `documents/` folders stay exactly as they are — don't touch them.
5. Push to `main`. GitHub Pages will deploy automatically.

## Adding Book Notes (Hover State)

In `reader.html`, find any `<li>` you want to add a note to and:

1. Add the class `has-note` to the `<li>`
2. Add a `.book-note` span inside it

Example — before:
```html
<li><span class="book-title">Pond</span> by Claire-Louise Bennett</li>
```

After:
```html
<li class="has-note">
  <span class="book-title">Pond</span> by Claire-Louise Bennett
  <span class="book-note">Your note here.</span>
</li>
```

The note appears on hover automatically. On mobile it appears on tap.

## Adding Project Content (Producer)

In `producer.html`, each project has a `<div class="project-panel">` block. To populate one:

1. Replace the `<div class="project-carousel">[ Images coming soon ]</div>` with actual images
2. Replace `<p>Case study coming soon.</p>` with your copy

For the carousel, the simplest approach is to add multiple images and use basic JS to cycle them — let me know when you're ready and I'll build that out.

## Adding the Model Section Images

In `about.html`, same pattern as Producer — find the `.project-carousel` block for each model project and swap in images.

## Things Still To Do

- [ ] Populate Producer case studies (Batch, Bombas, Ocean, No Filter, ToF)
- [ ] Add book notes to reading lists
- [ ] Add model photos (No Filter, Remnants)
- [ ] Update book count in about.html bio (currently 405 — adjust as needed)
- [ ] Add favicon if you have a new one
- [ ] Check all existing PDF links still resolve correctly after restructure
