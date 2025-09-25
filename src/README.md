[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/dNSiaw_-)
# W01 HTML5 Foundations (CS L300)

**Short description:** Week 1 starter for CS L300. Build a small, multi-page site using real HTML5: clean semantics, sensible headings, an accessible contact form, and a working “Skip to main content” link. No frameworks.

---

## What you’ll build
A simple **2–3 page** static site that shows:
- Proper **HTML5 landmarks** (`header`, `nav`, `main`, `footer`, `aside` if needed)
- Clear **heading structure** (exactly one `h1` per page)
- **Global navigation** with current-page indication
- An **accessible form** (labels, `required`, email validation)
- A **skip link** that jumps to `#main`
- Basic **metadata** (`lang`, `title`, `meta viewport`)
- Meaningful **alt text** on images

**Learning mode:** You do most of the work on your own before lab (about **70%**). Thursday lab is coaching, fixes, and a short showcase (**30%**).

---

## Acceptance Criteria (checklist)

### Structure & Semantics
- [ ] Each page includes:  
  `<!doctype html>`, `<html lang="en">`, `<meta charset="utf-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1">`, and a descriptive `<title>`.
- [ ] Uses landmarks: `<header>`, `<nav>`, `<main>`, `<footer>` (and `<aside>` if appropriate).
- [ ] Exactly **one `<h1>`** per page; subheadings follow a logical order.
- [ ] Global navigation links across pages; the current page is indicated (`aria-current="page"` or a class).

### Accessibility & Content
- [ ] First focusable element is a **“Skip to main content”** link targeting the `<main>`’s `id`.
- [ ] All images (if used) have meaningful `alt` text (or `alt=""` when decorative).
- [ ] `contact.html` contains a form with at least:
  - Full name (text)
  - Email (`type="email"`)
  - A choice control (`select` or `radio`)
  - A message (`textarea`)
  - Proper label–control association (`for`/`id` or implicit labels)
  - `required` on **two or more** fields (email must be one)
  - Short inline hint where helpful

### Documentation
- [ ] **Update this README** with:
  - A brief project overview
  - The list of pages and what’s on them
  - A **4–6 sentence reflection**:  
    - Which semantic choices you made and why  
    - What you did for accessibility  
    - One tricky bit and how you solved it

### Git Workflow
- [ ] Create a feature branch: `feat/<your-name>-w01`
- [ ] Open a PR to `main` with the checklist above ticked (add screenshots if you can)

---

## Suggested file structure
```
/src/
  index.html
  /pages/
    contact.html
  /assets/
    img/            # optional
```

---

## Quick starters (you can rewrite freely)

**`/src/index.html`**
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>My Semantic Site — Home</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style> :focus { outline: 2px solid; } </style>
</head>
<body>
  <a href="#main">Skip to main content</a>
  <header>
    <h1>Home</h1>
    <nav aria-label="Primary">
      <a href="/src/index.html" aria-current="page">Home</a>
      <a href="/src/pages/contact.html">Contact</a>
    </nav>
  </header>
  <main id="main">
    <section>
      <h2>Welcome</h2>
      <p>Replace this with meaningful content and proper headings.</p>
    </section>
  </main>
  <footer>
    <small>© 2025 Your Name</small>
  </footer>
</body>
</html>
```

**`/src/pages/contact.html`**
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>My Semantic Site — Contact</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style> :focus { outline: 2px solid; } </style>
</head>
<body>
  <a href="#main">Skip to main content</a>
  <header>
    <h1>Contact</h1>
    <nav aria-label="Primary">
      <a href="/src/index.html">Home</a>
      <a href="/src/pages/contact.html" aria-current="page">Contact</a>
    </nav>
  </header>
  <main id="main">
    <form>
      <div>
        <label for="name">Full name</label>
        <input id="name" name="name" required />
      </div>

      <div>
        <label for="email">Email</label>
        <input id="email" name="email" type="email" required />
      </div>

      <fieldset>
        <legend>Topic</legend>
        <label><input type="radio" name="topic" value="general" required /> General</label>
        <label><input type="radio" name="topic" value="support" /> Support</label>
      </fieldset>

      <div>
        <label for="msg">Message</label>
        <textarea id="msg" name="msg" required></textarea>
      </div>

      <button type="submit">Send</button>
    </form>
  </main>
  <footer>
    <small>© 2025 Your Name</small>
  </footer>
</body>
</html>
```

---

## Getting started (VS Code)

1. **Open folder in VS Code**  
2. Install the **Live Server** extension (Ritwick Dey) or use any static server.  
3. Right-click `index.html` → **Open with Live Server** (or open in a browser directly).  
4. Keep focus outlines visible; don’t remove them with CSS.

**Recommended extensions**
- Live Server  
- Prettier (for tidy HTML)  
- HTMLHint (optional)

---

## Submission (GitHub Classroom)

1. Accept the invite → your private repo is created.  
2. Create a branch:
   ```bash
   git checkout -b feat/<your-name>-w01
   ```
3. Build inside `/src/`. Commit often:
   ```bash
   git add .
   git commit -m "feat: add semantic layout and nav"
   git push -u origin HEAD
   ```
4. Open a **Pull Request** to `main` and include the PR checklist below.  
5. Request a review.

**PR Checklist (paste into your PR description)**
```md
- [ ] All Acceptance Criteria met
- [ ] Landmarks + single <h1> per page
- [ ] Skip link targets #main
- [ ] Form has labels + required + email validation
- [ ] Images have alt (or empty alt if decorative)
- [ ] README updated with 4–6 sentence reflection
- [ ] Screenshots of pages (and focus outlines)
```

---

## Grading (10 pts)
- **Meets Acceptance Criteria** – 6 pts  
- **Accessibility & semantics quality** – 2 pts  
- **README reflection (clarity & reasoning)** – 1 pt  
- **Git hygiene (branching, commits, PR checklist)** – 1 pt

> **Deadline:** Monday 08:00 (Africa/Accra). Extensions require prior approval.

---

## Stretch goals (optional)
- Add an accessible **table** (`<caption>`, `<th scope>`).  
- Use `<figure>` + `<figcaption>` for an image with a caption.  
- Add `aria-current="page"` or suitable ARIA labels (avoid overuse).  
- Try a basic **print stylesheet** or a small set of CSS variables.

---

## Resources
- MDN – HTML overview: https://developer.mozilla.org/en-US/docs/Web/HTML  
- MDN – Elements reference: https://developer.mozilla.org/en-US/docs/Web/HTML/Element  
- MDN – Your first form: https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form  
- MDN – Client-side form validation: https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation  
- WebAIM – Alt text: https://webaim.org/techniques/alttext/  
- WebAIM – Skip navigation: https://webaim.org/techniques/skipnav/

---

## Notes
Keep it plain and readable—good structure over flashy tricks. Arrive at Thursday’s lab with most of the site already built so we can spend the time on polish and accessibility.
