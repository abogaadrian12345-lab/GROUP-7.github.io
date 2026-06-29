# HopeCare Hospital Website

## Overview
HopeCare Hospital is a responsive web-based presentation platform for Uganda's leading National Youth Referral Hospital. The website showcases the hospital's services, news, mission, vision, and key personnel information.

## Features

### 1. **Responsive Header Navigation**
- Logo and hospital branding
- Navigation menu with links to:
  - Home
  - Departments
  - Directorates
  - Gallery
  - About Us
- Mobile-friendly design

### 2. **Interactive Carousel**
- Displays 5 medical staff images
- Auto-rotates every 3 seconds
- Manual navigation with previous/next buttons (❮ ❯)
- Dot indicators for slide navigation
- Smooth fade and slide transitions (4s duration)

### 3. **Executive Director's Message**
- Features the Executive Director's photo
- Includes welcome message and hospital overview
- Highlights diagnostic and emergency services

### 4. **News & Publications Section**
- Grid layout displaying 3 news cards
- Cards include:
  - News images
  - Article headlines
  - Brief descriptions
- Hover effects for interactivity

### 5. **Vision, Mission & Values Section**
- Mission statement
- Vision statement
- Goals and core values
- Professional formatting with Bootstrap styling

### 6. **Footer**
- Hospital information and description
- Quick links navigation
- Services listing
- Contact information:
  - Address: Rubaga Hill, Kampala, Uganda
  - Phone: +256 768 709 563
  - Email: info@hopecare.go.ug
  - Website: www.hopecarehospital.go.ug
- Copyright information

---

## Technical Details

### **Technologies Used**
- **HTML5** - Page structure and semantic markup
- **CSS3** - Styling, animations, and responsive design
- **JavaScript** - Carousel functionality and interactivity
- **Bootstrap 5.3.0** - Additional responsive styling components

### **Key Components**

#### CSS Classes
- `.carousel` - Main carousel container
- `.slide` - Individual slide elements with fade/transform animations
- `.news-card` - News article cards with hover effects
- `.footer-grid` - Responsive footer layout
- `.director-message` - Executive message section

#### JavaScript Functions
| Function | Purpose |
|----------|---------|
| `showSlide(newIndex)` | Updates carousel display and dot indicators |
| `prevBtn.onclick()` | Navigate to previous slide |
| `nextBtn.onclick()` | Navigate to next slide |
| `dot.onclick()` | Jump to specific slide via dot indicator |
| `setInterval()` | Auto-advance carousel every 3 seconds |

### **Responsive Breakpoints**
- **≤ 980px**: Single column grid layout
- **≤ 720px**: Optimized padding and full-width cards

---

## File Structure
## Departments
# departments.html — HopeCare Hospital (Departments page)

This README documents the `departments.html` file in this repository. It explains the purpose of the page, how to preview it, which assets it depends on, and a short checklist of recommended fixes and improvements.

## Purpose
`departments.html` is a static HTML page that displays department information for the HopeCare Hospital website. It contains a header/navigation, a departments section showing three department cards (images + text), and a footer with contact and site links.

## Preview / How to view locally
1. Clone the repository (or open the repo folder).
2. Ensure the image assets referenced in the file are present in the same folder:
   - `logo.png`
   - `diana.jpeg`
   - `cynthia.jpeg`
   - `me.jpeg`
3. Open `departments.html` in your browser:
   - Double-click the file or
   - Use a local static server (recommended for browser security features), e.g. with Python:
     - Python 3: `python -m http.server 8000` then visit `http://localhost:8000/departments.html`

## Assets
Place these files beside `departments.html` (or update the paths in the HTML if you keep them in a subfolder):
- logo.png
- diana.jpeg
- cynthia.jpeg
- me.jpeg

## Recommended fixes and improvements
The page works as a basic static page, but there are a few HTML/CSS issues and accessibility/usability improvements that should be made:

1. HTML structure
   - Add a `<head>` element with at least `<meta charset="utf-8">` and a `<title>`.
   - The `<footer>` is currently placed after `</body>`; move the `<footer>` inside the `<body>` before the closing `</body>` tag.

2. Invalid/mistyped attributes
   - Header logo image: `<img src="logo.png" width="150" height="100")` has an extra `)` — remove it.
   - Inline paragraph uses `padding-up: 15px;` — invalid property. Use `padding-top: 15px;`.
   - CSS rule `flex wrap: wrap;` should be `flex-wrap: wrap;`.

3. Accessibility
   - Add `alt` attributes to all `<img>` tags (e.g., `alt="Head of General Surgery — Dr. Diana"`).
   - Use semantic markup for the navigation (wrap links in a `<ul>` / `<li>` or use ARIA roles) and include skip links if needed.
   - Ensure heading hierarchy is correct and unique page `<h1>` is present in the `<header>` or top of main content.

4. Responsiveness
   - The `.news-grid` uses `grid-template-columns: repeat(3, 1fr);` which can be too wide on small screens. Add media queries (e.g., switch to 1 column < 600px, 2 columns between 600–900px).
   - Consider moving styles to an external CSS file (e.g., `styles.css`) for maintainability.

5. Navigation links & filenames
   - `about us.html` contains a space in the filename. Prefer `about-us.html` (or escape the space in links) to avoid URL issues.
   - The CSS targets `nav ul` but the file uses direct `<a>` links in the `nav` (no `<ul>`). Either change the HTML to a list or adjust the CSS selectors.

6. Minor styling suggestions
   - Use relative units (rem, em) for font sizes to improve accessibility.
   - Reduce heavy box-shadow or make it color consistent for better visual design.

## Quick changelist to apply (example)
- Move `<footer>` inside `<body>`.
- Fix malformed `<img>` tag and add `alt` attributes.
- Replace `padding-up` with `padding-top`.
- Correct `flex wrap` → `flex-wrap`.
- Add `<head>` with `<meta charset="utf-8">` and `<title>HopeCare Hospital — Departments</title>`.
- Make `.news-grid` responsive via media queries.

## Contribution notes
- If you want, I can open a branch and submit a PR that implements the fixes above (move footer, correct typos, add alt attributes and basic responsiveness). Say "Apply fixes" and I will prepare the changes.

## License & authorship
- This README doesn't change code licensing. Keep the repository's license file (if any) to indicate reuse terms.
- Author of the original `departments.html` file: repository owner.

## Directorates
# kimone.html — HopeCare Hospital (Directorates) Page

Summary
-------
This repository file (kimone.html) is a static HTML page that presents the "Directorates" section of the HopeCare Hospital website. It uses Bootstrap 5 and Font Awesome (via CDN) and includes hero images, directorate cards, a testimonial carousel, and a footer.

Quick preview
-------------
- Open kimone.html directly in your browser.
- Or run a simple local server from the repo root and visit http://localhost:8000/kimone.html:
  - Python 3: `python -m http.server 8000`
  - Node: `npx http-server .`

If this repo is published as a GitHub Pages site (this repo appears to be a user/organization site), the page will be available at:
`https://<github-username>.github.io/kimone.html` (replace `<github-username>` accordingly).

Dependencies
------------
- Bootstrap 5.3 (CDN included in head)
- Font Awesome 6 (CDN included in head)
- Images:
  - Local: `logo.png`, `machine.jpg` (place in repo root or adjust paths)
  - Several directorate and testimonial images use external Unsplash URLs

Recommended project structure
-----------------------------
- / (repo root)
  - index.html (or home.html)
  - kimone.html
  - departments.html
  - gallery.html
  - about-us.html (recommended to avoid spaces)
  - /assets/
    - /images/ (logo.png, machine.jpg, any local images)
    - /css/ (optional custom CSS)
    - /js/ (optional custom JS)

How to edit / customize
-----------------------
- Change header text, navigation links, or add/remove directorate cards in kimone.html.
- Replace hero and card images by pointing src attributes to files in /assets/images.
- Customize colors: the page references CSS variables like `--mulago-dark-blue` — define them in a :root block or replace with explicit color values.
- Update the testimonial carousel content and add more items (follow Bootstrap carousel markup).

Known issues & suggested fixes
-----------------------------
- Logo img tag contains an extra parenthesis: `<img src="logo.png" width="150" height="100")` — remove the trailing `)`.
- Navigation links: `about us.html` contains a space which may break linking on some systems; rename to `about-us.html` and update all references.
- CSS uses the variable `--mulago-dark-blue` but it is not defined in the document — add a `:root { --mulago-dark-blue: #123456; }` or replace usage with a hex color.
- Some HTML structure may be missing closing tags or have mismatched divs (verify with an HTML validator).
- Accessibility improvements:
  - Provide meaningful alt text for all images.
  - Add landmarks and ARIA attributes as needed (e.g., role="navigation").
  - Ensure color contrast meets WCAG AA for text on backgrounds.
- Carousel text contains truncated testimonial text with `[...]` — replace with full text or proper truncation style.

Accessibility & best practices
------------------------------
- Ensure `alt` attributes are descriptive for all images.
- Use semantic tags where applicable (`<main>`, `<nav>`, `<header>`, `<footer>`).
- Validate HTML (https://validator.w3.org/) and test on mobile/responsive breakpoints.
- Minimize inline styles; move custom CSS to a separate stylesheet for easier maintenance.

Deploying to GitHub Pages
------------------------
- If this repository is the `username.github.io` repository, pushing `kimone.html` to `main` (or default branch) will publish it automatically.
- For project sites (not username.github.io), enable GitHub Pages in repo settings and set the site source to the branch/folder containing kimone.html.

Contributing
------------
- Open a pull request with proposed changes.
- Please include a short description of fixes (e.g., "fix: remove extra parenthesis in logo img tag") and reference relevant issues.

License
-------
Include your preferred license here (e.g., MIT). If you want, add a `LICENSE` file to the repo.

Contact
-------
For questions or updates: info@hopecare.go.ug
