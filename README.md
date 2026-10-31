# The UX Review

A responsive, neo-brutalist landing page for a design & tech blog. Built with plain HTML, CSS, and a few lines of vanilla JavaScript, with no frameworks and no build step.

> **Brutal thoughts. Bold ideas.**

---

## Features

- **Neo-brutalist design** with thick black borders, hard offset shadows, rotated badges, and bold typography.
- **Fixed navbar** with smooth-scroll anchor links to every section.
- **Fully responsive** with breakpoints for tablet and mobile.
- **Hamburger menu** on screens up to 992px, including a Subscribe button inside the menu.
- **Hover micro-interactions** on cards, buttons, and social icons.
- **Zero dependencies** apart from Font Awesome (icons) and Google Fonts (Exo).

## Sections

| Section | Anchor | Description |
| --- | --- | --- |
| Hero | `#hero` | Headline, intro text, CTA buttons, and featured image |
| Latest Articles | `#articles` | Article cards, trending list, and category filter |
| Authors | `#authors` | Three author cards with role badges and social links |
| Community | `#community` | Membership perks, join CTA, and testimonials |
| Footer | n/a | Brand blurb, categories, newsletter form, and legal links |

## Tech Stack

- **HTML5**: semantic structure
- **CSS3**: Flexbox, Grid, media queries, `:is()`, transitions
- **JavaScript (vanilla)**: mobile menu toggle
- **[Font Awesome 7](https://fontawesome.com/)**: icons (CDN)
- **[Google Fonts: Exo](https://fonts.google.com/specimen/Exo)**: typography (CDN)

## Responsive Breakpoints

| Breakpoint | Behavior |
| --- | --- |
| `> 992px` | Full desktop layout with inline nav links |
| `≤ 992px` | Hamburger menu, sections stack into one column, footer becomes 2 columns |
| `≤ 576px` | Smaller type, stacked article cards, footer becomes 1 column |

## Customization

**Colors.** The palette is used directly in `style.css`. Search and replace to re-theme:

| Color | Usage |
| --- | --- |
| `#FFF085` | Hero and header background |
| `#FFD15B` / `#FFDF20` | Primary yellow (buttons, badges) |
| `#f3aa00` | Hover accent |
| `#e7000b` | Red accent |
| `#155dfc` | Blue accent |
| `#ad46ff` | Purple accent |
| `#000` | Borders, shadows, and footer |

**Font.** Change the Google Fonts `<link>` in `index.html` and the `font-family` in `body` inside `style.css`.

**Content.** All text lives in `index.html`. Duplicate an `.articles-card`, `.author-card`, or `.community-articles` block to add more entries.

## Mobile Menu

The hamburger toggles an `open` class on the navbar:

```js
const nav = document.getElementById("nav");
document.querySelector(".menu-btn").onclick = () => nav.classList.toggle("open");
document.querySelectorAll(".nav-links a").forEach(a => a.onclick = () => nav.classList.remove("open"));
```

The menu closes automatically when a link is clicked.

## Known Limitations

- Buttons ("Subscribe", "Load more", "Join now") and the newsletter form are visual only and have no backend or handlers yet.
- Social links point to `#`.
- Dates and copyright in the footer are static text.

## Roadmap

- [ ] Wire up the newsletter form
- [ ] "Load more articles" pagination
- [ ] Category filtering
- [ ] Article detail pages
- [ ] Dark mode

## License

This project was built for learning and portfolio purposes. Add a license of your choice (MIT is a good default) before publishing.