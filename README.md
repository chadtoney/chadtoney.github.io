# Chad Toney — Personal Website

A lightweight, multi-page personal website with a focused landing page and a separate résumé.

## Design

- Information first: clear hierarchy, quiet dividers, readable type, and a restrained accent color.
- Outcomes have direct labels and context, without decorative charts or unrelated comparisons.
- Responsive layouts, keyboard focus indicators, skip links, and current-page navigation.
- Print styles for the résumé.
- Plain HTML and shared CSS: no JavaScript, build step, fonts, or icon CDN required.

## 🚀 Getting Started

### Option 1: Open Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/chadtoney/chadtoney.github.io.git
   cd chadtoney.github.io
   ```

2. Open `index.html` in your web browser:
   - **Windows**: Double-click `index.html`
   - **Mac**: Right-click `index.html` → Open With → Browser
   - **Linux**: `xdg-open index.html`

### Option 2: Deploy with GitHub Pages

The site is automatically published at: `https://chadtoney.github.io`

### Option 3: Use a Local Server

From the repository root, serve the files locally (refresh the browser after edits):

```bash
# Using Python 3
python -m http.server 8000

```

Then open `http://localhost:8000` in your browser.

## 📁 Project Structure

```
chadtoney.github.io/
├── index.html          # Landing page and directory of pages
├── resume.html         # Professional experience and qualifications
├── page-template.html  # Copyable starter for new root-level pages
├── style.css           # Shared design tokens, layouts, and print styles
└── README.md           # This file
```

## 🎨 Customization

### Updating Content

1. **Landing page**: Edit the introduction, focus areas, outcomes, and personal section in `index.html`.
2. **Résumé**: Edit experience, skills, certifications, and education in `resume.html`.
3. **Contact information**: Keep links consistent on both pages.

### Adding a Page

1. Copy `page-template.html` to a descriptive filename in the repository root, such as `projects.html`.
2. Replace its title, description, topic, heading, introduction, and content. Remove the `noindex` meta tag when the new page is ready to be indexed; leave it on the original template.
3. Add an entry to the landing page’s `page-list` under **Explore**, using the existing résumé entry as the pattern. Link to the new filename and supply a short description.
4. Keep the shared Home/Résumé navigation for secondary pages. If promoting a page into the main navigation, update the header in every HTML file, including the template; set `aria-current="page"` only on the link matching each page.
5. Reuse `page-content`, `section`, and the shared layout classes rather than copying CSS. Root-level relative links work both on GitHub Pages and when opening files directly; nested pages would need adjusted paths.

The template is intentionally not linked from the landing page and is marked `noindex`. The deployment uploads the repository as static files, so no routing or build configuration changes are needed for new pages.

### Styling

All styles are in `style.css` with CSS variables for easy customization:

```css
:root {
    --background: #fcfcfa;
    --text: #252b2b;
    --muted: #59615f;
    --accent: #216659;
    --rule: #d9ded9;
}
```

## Validation

There are no configured build, lint, or automated test commands. Before publishing:

- Open the landing page, résumé, and any new pages using the local server.
- Follow internal navigation and check contact links.
- Check narrow and wide viewports for readable wrapping and horizontal overflow.
- Use Tab to verify visible focus, the skip link, and navigation.
- Preview the résumé in print mode.

## 📱 Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This project is open source and available for personal use.

## 👤 Contact

**Chad Toney**
- LinkedIn: [linkedin.com/in/chadtoney](https://linkedin.com/in/chadtoney)
- GitHub: [github.com/chadtoney](https://github.com/chadtoney)
- Email: chad.toney@gmail.com

---

Built with ❤️ and data-driven precision!
