# Nidhi Dattaprasad Shastri — Professional Portfolio

A single-page professional portfolio website (LinkedIn-style) built for a web
development assignment demonstrating semantic HTML5, external CSS, a CSS-selector
styled table, Flexbox, two required responsive components (image gallery and
testimonials), and media queries for tablet and phone breakpoints.

All education, experience, skills, and project content is drawn from my real
resume. The testimonials are draft placeholders written in the voice of real
working relationships (manager, teammate, faculty) and are marked in the page
for replacement with actual quotes before final submission. Project images
are original diagrams generated specifically for this project (not stock
photos or screenshots from elsewhere).

## Sections on the page

1. **About** — name, title, and a short professional summary.
2. **Education** — Northeastern University (MS) and RNS Institute of Technology (BE).
3. **Experience** — Capgemini Technology Services (Analyst → Sr. Analyst) and a
   Data Science internship, plus a volunteering aside.
4. **Skills** — a table of skill categories and tools, styled using multiple
   CSS selectors.
5. **Projects** — an image gallery of three projects (Cross-Cultural Diplomatic
   Assistant, GridDeliveryEnv, AR/AI Object Placement System).
6. **Testimonials** — three testimonial cards.
7. **Contact** — a contact form plus direct email/phone/LinkedIn links.

## HTML tags used, and why

| Tag | Used for |
|---|---|
| `<!DOCTYPE html>` | Declares the document as HTML5. |
| `<html lang="en">` | Root element, sets page language. |
| `<head>` | Metadata, title, favicon link, stylesheet link. |
| `<meta charset>` / `<meta viewport>` | Character encoding and responsive scaling (required for media queries to work on real devices). |
| `<title>` | Browser tab title. |
| `<link rel="icon">` | Points to the custom SVG favicon (initials monogram). |
| `<link rel="stylesheet">` | Loads the external CSS file (`css/styles.css`). |
| `<body>` | Main document body. |
| `<header>` | **Semantic** — site header with name/logo and navigation. |
| `<nav>` | Navigation links to each section of the page. |
| `<ul>` / `<li>` | Navigation list. |
| `<main>` | Wraps all primary page content. |
| `<section>` | **Semantic** — divides the page into About, Education, Experience, Skills, Projects, Testimonials, and Contact. |
| `<article>` | **Semantic** — each individual education entry and each job/internship is a self-contained article. |
| `<aside>` | **Semantic** — the volunteering note, tangential to the main experience list. |
| `<footer>` | **Semantic** — site footer (also used inside each testimonial `<blockquote>` for attribution). |
| `<h1>` / `<h2>` / `<h3>` | Heading hierarchy for name, section titles, and entry titles. |
| `<p>` | Body paragraphs throughout. |
| `<a>` | Hyperlinks — in-page navigation, the "Get in touch" button, `mailto:`/`tel:` links, and the LinkedIn placeholder link. |
| `<span>` | Small inline styling hook (e.g. the client name next to a job title). |
| `<strong>` | Emphasizes "Make A Difference" in the volunteering note. |
| `<ul>` / `<li>` (inside articles) | Bullet points for job responsibilities/achievements. |
| `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>` | The Skills table, styled with CSS selectors (see below). |
| `<figure>` / `<figcaption>` | Wraps each project image with a title and description, used as the image-gallery items. |
| `<img>` | Displays the three generated project diagrams. |
| `<blockquote>` | Each testimonial quote. |
| `<form>` | The contact form. |
| `<label>` | Labels for each form field, tied to inputs via `for`/`id`. |
| `<input type="text">` | Contact name field. |
| `<input type="email">` | Contact email field. |
| `<textarea>` | Contact message field. |
| `<button type="submit">` | Submits the contact form. |
| `<div>` | Non-semantic layout wrapper used only for the header inner bar, gallery, and testimonials flex containers, where no more specific semantic element applied. |

## CSS selectors used on the table (requirement: minimum 2)

The Skills table (`#skills table`) is styled with **three** selectors:

1. `tbody tr:nth-child(even)` — zebra-striping alternate rows.
2. `tbody tr:hover` — highlights a row on mouse-over.
3. `td:first-child` — bolds the first column (skill category).

## Flexbox usage

- `.header-inner` — `display: flex`, `justify-content: space-between`, `align-items: center` for the header/nav bar.
- `.gallery` (Image Gallery) — `display: flex`, `flex-wrap: wrap`, `justify-content: center`, `flex-grow` on each card.
- `.testimonials` — `display: flex`, `flex-direction: row`, `flex-wrap: wrap`, `flex-grow` on each card.
- Both responsive components switch to a single column (`flex-direction: column`) at the phone breakpoint.

## Responsive components (required)

1. **Image Gallery** (`#projects .gallery`) — project cards with a hover lift/zoom effect (`transform`, `box-shadow`).
2. **Testimonials** (`#testimonials .testimonials`) — quote cards with a hover background/lift effect.

## Media queries

- **iPad (max-width: 768px)** — gallery and testimonial cards shift to a 2-column layout, section padding and table font-size shrink slightly.
- **Smartphone (max-width: 375px)** — header stacks vertically, nav becomes a vertical list, gallery/testimonials become single-column, and the table collapses into a stacked (label-less block) layout so it doesn't overflow a narrow screen.

## Contact markup

- `mailto:` link opens a pre-addressed email.
- `tel:` link dials the phone number on mobile devices.

## Assets

- `assets/favicon.svg` — custom "NS" monogram favicon.
- `assets/img/project-*.png` — three original diagrams generated with Python/Pillow specifically for this project.

## Git history

Built with small, incremental commits — one per section (HTML) and one per
style block (CSS) — rather than a single large commit. Run `git log --oneline`
to see the full history.

## TODO before final submission

- [ ] Replace placeholder testimonial quotes with real ones (or get permission to keep drafted versions).
- [ ] Replace the LinkedIn `#` placeholder with the real profile URL.
- [ ] Optionally swap generated project diagrams for real screenshots, if available.
