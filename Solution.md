# Assignment 2.3 — Solution: Div, Attributes & Clean Structure

## Steps
1. Take the page from Assignment 2.2 (or use the code below) and save it as `index.html`.
2. Replace the placeholders (**Your Name**, email, university, etc.) with your real details.
3. Open in the browser and press `F12` → **Elements** tab to capture the page structure screenshot.

## index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Personal Introduction</title>
  </head>

  <body>
    <!-- Page wrapper -->
    <div id="page-container" class="container">

      <!-- ===== HEADER SECTION ===== -->
      <div id="header-section" class="section">
        <h1 id="full-name">Your Name</h1>
        <h2 id="job-title" class="subtitle" data-role="web-developer">
          Aspiring Full-Stack Web Developer
        </h2>
      </div>

      <hr />

      <!-- ===== ABOUT SECTION ===== -->
      <div id="about-section" class="section">
        <h2 class="section-title">About Me</h2>
        <p id="about-text" class="text-block">
          Hello! I am <strong>Your Name</strong>, a <em>passionate learner</em>
          focused on building clean, responsive and accessible websites with
          <strong>HTML, CSS, and JavaScript</strong>. I enjoy turning ideas
          into <i>real, working projects</i>.
        </p>
        <!-- New content added -->
        <p id="about-goal" class="text-block">
          <strong>Current goal:</strong> build three portfolio projects and
          contribute to open-source on GitHub.
        </p>
      </div>

      <hr />

      <!-- ===== EDUCATION SECTION ===== -->
      <div id="education-section" class="section">
        <h2 class="section-title">Education</h2>

        <div id="education-university" class="item" data-year-start="2022" data-year-end="2026">
          <h3 class="item-title">Bachelor's Degree in Computer Science</h3>
          <p class="item-detail">
            <strong>Your University Name</strong><br />
            <span class="item-years">2022 – 2026</span>
          </p>
        </div>

        <div id="education-school" class="item" data-year-start="2020" data-year-end="2022">
          <h3 class="item-title">Higher Secondary Education</h3>
          <p class="item-detail">
            <strong>Your School Name</strong><br />
            <span class="item-years">2020 – 2022</span>
          </p>
        </div>
      </div>

      <hr />

      <!-- ===== SKILLS SECTION ===== -->
      <div id="skills-section" class="section">
        <h2 class="section-title">Skills</h2>

        <div id="skills-technical" class="item">
          <h3 class="item-title">Technical Skills</h3>
          <p class="item-detail">
            <span class="skill" data-level="intermediate">HTML5</span>,
            <span class="skill" data-level="intermediate">CSS3</span>,
            <span class="skill" data-level="beginner">JavaScript</span>,
            <span class="skill" data-level="beginner">Git &amp; GitHub</span>
          </p>
        </div>

        <div id="skills-soft" class="item">
          <h3 class="item-title">Soft Skills</h3>
          <p class="item-detail">
            Communication, teamwork, problem solving, time management
          </p>
        </div>
      </div>

      <hr />

      <!-- ===== CONTACT SECTION ===== -->
      <div id="contact-section" class="section">
        <h2 class="section-title">Contact</h2>
        <p class="item-detail">
          <strong>Email:</strong> <span id="contact-email">your.email@example.com</span><br />
          <strong>GitHub:</strong> <span id="contact-github">github.com/your-username</span><br />
          <strong>Location:</strong> <span id="contact-location">Your City, Country</span>
        </p>
      </div>

    </div>
  </body>
</html>
```

## What Changed from Assignment 2.2
| Requirement | How it is met |
|-------------|---------------|
| Header, About, Education, Skills, Contact sections | `#header-section`, `#about-section`, `#education-section`, `#skills-section`, `#contact-section` |
| `div` containers | One `div` per section, inside the `#page-container` wrapper |
| Unique `id` | `full-name`, `job-title`, `about-text`, `contact-email`, etc. — each used once |
| Reusable `class` | `section`, `section-title`, `item`, `item-title`, `item-detail`, `skill`, `text-block` — repeated on many elements |
| `data-*` attribute | `data-role` on the job title, `data-year-start`/`data-year-end` on education items, `data-level` on skills |
| Update a text element | Job title changed from "Aspiring Web Developer" to **"Aspiring Full-Stack Web Developer"** |
| Add new content | New **Contact** section and a new **Current goal** paragraph |
| Indentation & meaningful names | 2-space indentation, descriptive names in kebab-case, comments before each section |

## Key Concepts
- **`id`**: must be unique in the page; identifies one specific element (used by CSS `#id`, JS `getElementById`, and anchor links).
- **`class`**: reusable by many elements; used to group elements for shared styling or behavior (CSS `.class`).
- **`data-*`**: custom attributes that store extra information on an element, readable in JavaScript via `element.dataset` (e.g. `el.dataset.level`).
- **`div`**: a generic block container used to group and structure content.

## Submission
- ✅ Updated `index.html` (attached)
- 📸 Screenshot showing the page structure: browser DevTools (`F12`) → **Elements** tab with the sections expanded (or VS Code showing the indented code side-by-side with the page)
