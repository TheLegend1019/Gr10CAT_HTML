# Gr10CAT_HTML

Grade 10 CAT — HTML Guide (CAPS/NSC)
A start-to-finish, classroom-ready handbook in GitHub-flavoured Markdown. Drop directly into README.md.
Table of Contents
What is HTML?
Tools & Setup
Project Folder Structure
Create Your First Page (index.html)
Essential HTML Elements
Links & Navigation
Images & File Paths
Lists & Tables
Page Layout with Semantic Tags
Forms (Intro)
Mini CSS (Neat Marking)
Accessibility Basics (CAPS-aligned)
Validation & Troubleshooting
Common Errors & Fixes
Practical Tasks
Submission Checklist
Quick Reference Tag Sheet
Complete Example Page
What is HTML?
HTML (HyperText Markup Language) gives structure to web content (headings, paragraphs, images, links, tables, and forms).
Grade 10 focus: HTML structure, with a small amount of CSS for neatness.
Tools & Setup
Editor: Notepad++, VS Code, or any plain text editor (not MS Word).
Browser: Chrome/Edge/Firefox for testing.
Validator: https://validator.w3.org/
Filenames: Lowercase, no spaces (e.g., about_us.html).
Project Folder Structure
MyWebsite/
├─ index.html
├─ about.html
├─ contact.html
├─ images/
│  └─ logo.png
└─ css/
   └─ style.css
Keep relative paths (don’t use C:\Users\...).
Create Your First Page (index.html)
Create index.html and paste:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>My Grade 10 Website</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
    <nav>
      <a href="index.html" aria-current="page">Home</a> |
      <a href="about.html">About</a> |
      <a href="contact.html">Contact</a>
    </nav>
    <hr />
  </header>

  <main>
    <h2>Introduction</h2>
    <p>This is my Grade 10 CAT website. I built it with HTML.</p>
  </main>

  <footer>
    <hr />
    <p>&copy; 2025 My Name. All rights reserved.</p>
  </footer>
</body>
</html>
Essential HTML Elements
Headings & Paragraphs
<h1>Main Title</h1>
<h2>Section</h2>
<h3>Subsection</h3>
<p>Normal paragraph text goes here.</p>
Use one <h1> per page. Structure content with h2–h6.
Emphasis & Inline
<p><strong>Important:</strong> Submit on time.</p>
<p>This is <em>emphasised</em> text.</p>
<p>Line break here<br>without a new paragraph.</p>
Horizontal Rule & Entities
<hr>
<p>&copy; &lt; &gt; &nbsp;</p>
Links & Navigation
Internal (within your site)
<a href="about.html">About</a>
<a href="contact.html">Contact</a>
External (new tab)
<a href="https://www.gov.za" target="_blank" rel="noopener">Government site</a>
Email / Phone
<a href="mailto:me@example.com">Email me</a>
<a href="tel:+27115551234">Call us</a>
Images & File Paths
<img src="images/logo.png" alt="My website logo" width="200">
Always include meaningful alt text.
Figure + Caption:
<figure>
  <img src="images/sunrise.jpg" alt="Sunrise at the beach">
  <figcaption>Figure 1: Sunrise at the beach.</figcaption>
</figure>
Lists & Tables
Lists
<ul>
  <li>Apples</li>
  <li>Bananas</li>
</ul>

<ol>
  <li>Step one</li>
  <li>Step two</li>
</ol>

<dl>
  <dt>HTML</dt><dd>Structures content</dd>
  <dt>CSS</dt><dd>Styles content</dd>
</dl>
Tables (with headers)
<table>
  <caption>Subject Marks</caption>
  <thead>
    <tr><th>Subject</th><th>Term 1</th><th>Term 2</th></tr>
  </thead>
  <tbody>
    <tr><td>CAT</td><td>78%</td><td>82%</td></tr>
    <tr><td>Math</td><td>71%</td><td>74%</td></tr>
  </tbody>
  <tfoot>
    <tr><td>Average</td><td colspan="2">76.25%</td></tr>
  </tfoot>
</table>
Use tables for data, not layout.
Page Layout with Semantic Tags
<header>…</header>
<nav>…</nav>
<main>
  <article>
    <h2>My Article</h2>
    <p>Content…</p>
  </article>
  <aside>
    <p>Sidebar notes or links.</p>
  </aside>
</main>
<footer>…</footer>
Forms (Intro)
<form action="#" method="get">
  <label for="name">Your Name:</label>
  <input id="name" name="name" type="text" required>

  <label for="email">Email:</label>
  <input id="email" name="email" type="email" required>

  <label for="msg">Message:</label>
  <textarea id="msg" name="msg" rows="4"></textarea>

  <button type="submit">Send</button>
</form>
label for must match input id for accessibility.
Mini CSS (Neat Marking)
Create css/style.css:
* { box-sizing: border-box; }
body { font-family: system-ui, Arial, sans-serif; line-height: 1.5; margin: 16px; }
header, footer { padding: 8px 0; }
nav a { margin-right: 8px; text-decoration: none; }
main { max-width: 900px; }
img { max-width: 100%; height: auto; }
table { border-collapse: collapse; width: 100%; }
th, td { border: 1px solid #ccc; padding: 8px; text-align: left; }
caption { font-weight: 600; margin-bottom: 6px; }
Link it in each page:
<link rel="stylesheet" href="css/style.css">
Accessibility Basics (CAPS-aligned)
Provide alt text for meaningful images.
Heading order: <h1> then <h2>… (don’t skip levels for styling).
Labels for form controls, use required where appropriate.
Ensure readable contrast and font sizes.
Make link text descriptive (avoid “click here”).
Validation & Troubleshooting
Use W3C Validator to catch errors/warnings.
Fix missing tags, incorrect nesting, wrong attributes, and missing alt.
Typical Fixes:
Add <!DOCTYPE html> and a <title>.
Check image paths & filename case.
Close all tags and avoid putting block elements inside <p>.
Common Errors & Fixes
Error	Why	Fix
Missing <!DOCTYPE html>	Quirks mode rendering	Add HTML5 doctype
No <title>	Poor usability/SEO	Add a descriptive title
Broken image	Wrong path/name	Verify images/ & case
Overusing <b>	Not semantic	Prefer <strong>
Layout table	Bad accessibility	Use CSS + semantic tags
No alt	Inaccessible images	Describe the image’s meaning
Practical Tasks
Task A — Two-Page Site
Requirements:
index.html, about.html
Working navigation both ways
At least one image with alt
One ordered list and one table
0 validator errors
Extension: Add css/style.css.
Task B — Topic Page with Media & Lists
Header, main, footer
A <figure> with <figcaption>
One unordered list + one definition list
Links: internal, external (new tab), mailto
Correct heading order + alt text
Task C — Simple Contact Form
Name, Email, Message, Submit
label ↔ id pairs
required where appropriate
Submission Checklist
 Folder structure uses images/ and css/
 index.html opens; links work on all pages
 Each page has a meaningful <title>
 Proper headings, paragraphs, and lists used
 Table uses <th> for headers
 Images display and include good alt
 Mini CSS applied (optional but preferred)
 W3C Validator shows 0 errors
 Accessibility basics followed
Quick Reference Tag Sheet
Structure: <!DOCTYPE html>, <html>, <head>, <meta>, <title>, <body>, <header>, <nav>, <main>, <article>, <section>, <aside>, <footer>
Text: <h1>…<h6>, <p>, <strong>, <em>, <br>, <hr>, <span>, <div>
Links & Media: <a href>, target="_blank", rel="noopener", <img>, <figure>, <figcaption>
Lists: <ul>, <ol>, <li>, <dl>, <dt>, <dd>
Tables: <table>, <caption>, <thead>, <tbody>, <tfoot>, <tr>, <th>, <td>
Forms: <form>, <label>, <input>, <textarea>, <button>, attributes: type, id, name, required
Meta: <meta charset="UTF-8">, <meta name="viewport" content="width=device-width, initial-scale=1">
Complete Example Page
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Healthy Living: Home</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <h1>Healthy Living</h1>
    <nav>
      <a href="index.html" aria-current="page">Home</a> |
      <a href="about.html">About</a> |
      <a href="contact.html">Contact</a>
    </nav>
    <hr>
  </header>

  <main>
    <article>
      <h2>Eat Well, Move More</h2>
      <p>Small daily choices add up. Start with simple goals.</p>

      <figure>
        <img src="images/fruit-bowl.jpg" alt="Bowl of fresh fruit">
        <figcaption>Figure 1: A colourful fruit bowl.</figcaption>
      </figure>

      <h3>Three Quick Tips</h3>
      <ol>
        <li>Drink water first.</li>
        <li>Add a fruit or veg to each meal.</li>
        <li>Take a 10-minute walk.</li>
      </ol>

      <h3>Weekly Plan</h3>
      <table>
        <caption>Starter Plan</caption>
        <thead>
          <tr><th>Day</th><th>Goal</th><th>Notes</th></tr>
        </thead>
        <tbody>
          <tr><td>Mon</td><td>2L water</td><td>Carry a bottle</td></tr>
          <tr><td>Tue</td><td>Walk 10 min</td><td>After school</td></tr>
        </tbody>
      </table>

      <p>More info at <a href="https://www.who.int/" target="_blank" rel="noopener">WHO</a>.</p>
    </article>
  </main>

  <footer>
    <hr>
    <p>&copy; 2025 Healthy Living | <a href="mailto:student@example.com">Email me</a></p>
  </footer>
</body>
</html>
Teacher Notes (Optional)
Assess structure, working links, alt text, semantic tags, and 0 validator errors.
Allow CSS as enrichment for fast finishers.
Require local images/ (no hot-linking) to encourage proper file management.
