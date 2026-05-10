📘 HTML Code Review Rules (for AI)
1. Document Structure
Always use <!DOCTYPE html> at the top of the document.
<html> must include a lang attribute (e.g., lang="en").

The structure must strictly follow:

<html>
  <head></head>
  <body></body>
</html>
No elements outside <html>.
2. Head Section Requirements

Must include:

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>...</title>
<title> must be meaningful (not empty, not "Document").
Avoid duplicate or unnecessary meta tags.
3. Semantic HTML
Prefer semantic tags over generic <div>:
Use: <header>, <main>, <section>, <article>, <nav>, <footer>
Each page must have one <main> only.
Headings must follow hierarchy:
Only one <h1> per page
Do not skip levels (h1 → h3 is invalid)
4. Accessibility (A11y)
All <img> must have alt attribute:
Decorative → alt=""
Informative → meaningful description
Use <label> for all form inputs.
Interactive elements must be accessible:
Use <button> instead of <div> for clicks
Links (<a>) must have meaningful text (no "click here")
5. Valid Attributes & Syntax
All tags must be properly closed.
Use lowercase for tags and attributes.

Attribute values must always be in quotes:

<input type="text">
Avoid deprecated tags:
❌ <font>, <center>
Avoid inline styles:
❌ style="color:red"
6. Class & ID Naming
Use consistent naming convention:
Prefer kebab-case (e.g., main-header, nav-item)
IDs must be unique.
Avoid overly generic names:
❌ class="box"
7. Content Rules
No empty tags unless necessary:
❌ <div></div>
Avoid redundant wrappers (divitis)
Text content must be inside semantic elements (not floating)
8. Links & Resources
All links must be valid:
Use relative paths for internal files

External links should include:

target="_blank" rel="noopener noreferrer"
9. Forms
Every <input> must have:
type
name
Use proper input types:
email, tel, password, etc.
Use <form> properly (no orphan inputs)
10. Validation Compliance
Code must pass validation according to
World Wide Web Consortium (W3C)
No duplicate attributes
No invalid nesting:
❌ <p><div></div></p>
11. Clean Code Style
Proper indentation (2 or 4 spaces, consistent)
No commented-out dead code
Logical grouping of elements
12. Performance Basics
Avoid unnecessary nesting
Use appropriate tags instead of heavy structures
Minimize DOM depth