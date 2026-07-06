# Full Stack Learning Journal

## About This Repository

This repository contains my notes, projects, and concepts that I learned during my full stack internship. I have documented everything in a simple and organized way so that I can quickly revise the concepts whenever needed.

The goal of this repository is to strengthen my fundamentals and track my learning throughout the internship.

---

## Table of Contents

- [Projects Built](#projects-built)
- [How a Website Loads](#how-a-website-loads)
- [Browser Developer Tools](#browser-developer-tools)
- [HTML](#html-hypertext-markup-language)
- [CSS](#css-cascading-style-sheets)
- [Git & GitHub](#git--github)
- [GitHub Pages](#github-pages)
- [Markdown](#markdown)
- [Tools I Used](#tools-i-used)
- [Key Learnings](#key-learnings)
- [JavaScript Functions & Events](#javascript-functions--events)

---

# Projects Built

| Project | Skills Practiced |
|---------|------------------|
| **HTTP Under the Hood** | DNS, HTTP Request & Response, Status Codes, Browser Rendering |
| **Resume (HTML)** | Semantic HTML, Lists, Images, Links, Tables, Forms |
| **Resume (HTML + CSS)** | CSS Selectors, Box Model, Flexbox, Grid, Responsive Design |
| **Personal Portfolio** | Combining HTML & CSS to build a complete website |

---

# How a Website Loads

Whenever we open a website, the browser performs several steps before displaying the page.

```text
Enter URL
    │
    ▼
DNS Lookup
    │
    ▼
HTTP Request
    │
    ▼
Server Processing
    │
    ▼
HTTP Response
    │
    ▼
Browser Downloads Files
    │
    ▼
Page Rendered
```

## DNS (Domain Name System)

Computers communicate using IP addresses, while humans use domain names like `google.com`.

DNS converts a domain name into an IP address so the browser can locate the correct server.

---

## HTTP Request

The browser sends a request to the server for a resource.

### Example

```http
GET /index.html HTTP/1.1
```

| Method | Purpose |
|---------|---------|
| GET | Retrieve data |
| POST | Send new data |
| PUT | Update existing data |
| DELETE | Delete data |

---

## HTTP Response

The server processes the request and returns the requested resource along with a status code.

### Example

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

### Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 301 | Redirect |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

> **Note**
>
> Opening a webpage doesn't send just one request. The browser makes separate requests for HTML, CSS, JavaScript, images, fonts, and other resources.

---

## Browser Developer Tools

Developer Tools helped me inspect webpages and debug issues while building projects.

| Tab | Purpose |
|-----|---------|
| Elements | Inspect HTML and CSS |
| Network | View requests and status codes |
| Console | Check errors and warnings |
| Sources | View project files |

Instead of guessing why something wasn't working, I learned to use DevTools to inspect elements, verify file paths, and identify errors more efficiently.

---

## Quick Revision

- DNS → Converts domain name to IP address.
- HTTP → Communication between browser and server.
- GET → Retrieve data.
- POST → Send data.
- 404 → Resource not found.
- 500 → Internal server error.
- One webpage = Multiple HTTP requests.

# HTML (HyperText Markup Language)

HTML is the standard markup language used to create the structure of a webpage. It defines what each element represents, while CSS is responsible for its appearance.

---

## Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>

<body>

</body>
</html>
```

### Common HTML Tags

| Tag | Purpose |
|------|---------|
| `<!DOCTYPE html>` | Declares an HTML5 document |
| `<html>` | Root element of the webpage |
| `<head>` | Stores metadata |
| `<title>` | Browser tab title |
| `<body>` | Visible webpage content |

---

## Common HTML Elements

| Tag | Purpose |
|------|---------|
| `<h1>` - `<h6>` | Headings |
| `<p>` | Paragraph |
| `<a>` | Hyperlink |
| `<img>` | Image |
| `<ul>`, `<ol>`, `<li>` | Lists |
| `<table>` | Display tabular data |
| `<form>` | Collect user input |

---

# Semantic HTML

Semantic elements describe the purpose of the content instead of using generic `<div>` elements everywhere.

## Common Semantic Elements

| Tag | Purpose |
|------|---------|
| `<header>` | Top section of the webpage |
| `<nav>` | Navigation links |
| `<main>` | Main content |
| `<section>` | Related content |
| `<article>` | Independent content |
| `<aside>` | Sidebar or extra content |
| `<footer>` | Bottom section |

### Why Semantic HTML?

- Improves readability.
- Makes webpages more accessible.
- Helps search engines understand page structure.
- Makes code easier to maintain.

---

## `<div>` vs `<span>`

| `<div>` | `<span>` |
|----------|----------|
| Block-level element | Inline element |
| Used for larger sections | Used for small pieces of text |

---

# HTML Forms

Forms are used to collect information from users.

## Common Input Types

| Type | Purpose |
|------|---------|
| `text` | Text input |
| `email` | Email address |
| `password` | Password |
| `number` | Numeric input |
| `date` | Date selection |
| `checkbox` | Multiple selections |
| `radio` | Single selection |

---

## Quick Revision

- HTML → Webpage structure
- Semantic HTML → Meaningful elements
- `<div>` → Block element
- `<span>` → Inline element
- `alt` → Image description for accessibility
- Forms → Collect user input
- Tables → Only for tabular data

---

# CSS (Cascading Style Sheets)

CSS is used to style HTML elements. It controls the colors, fonts, spacing, layout, and responsiveness of a webpage.

---

## CSS Selectors

| Selector | Example | Purpose |
|----------|---------|---------|
| Element | `p` | Selects all `<p>` elements |
| Class | `.card` | Reusable styles |
| ID | `#header` | Styles one unique element |
| Universal | `*` | Selects every element |
| Descendant | `nav a` | Selects child elements |

> **Tip:** Use classes for reusable styles and IDs only for unique elements.

---

## Box Model

Every HTML element is treated as a box.

| Part | Purpose |
|------|---------|
| Content | Text or image |
| Padding | Space inside the border |
| Border | Boundary around the element |
| Margin | Space outside the border |

---

## Display Property

| Value | Purpose |
|-------|---------|
| `block` | Takes full width |
| `inline` | Takes only required width |
| `inline-block` | Inline with width & height |
| `flex` | Flexible layout |
| `grid` | Grid layout |
| `none` | Hides the element |

---

## Flexbox vs Grid

| Flexbox | Grid |
|----------|------|
| One-dimensional layout | Two-dimensional layout |
| Best for rows or columns | Best for complete page layouts |

---

## Position Property

| Value | Purpose |
|-------|---------|
| `static` | Default position |
| `relative` | Relative to its original position |
| `absolute` | Relative to nearest positioned parent |
| `fixed` | Stays fixed while scrolling |
| `sticky` | Sticks after reaching a position |

---

## Quick Revision

- CSS → Styling
- Class → Reusable selector
- ID → Unique selector
- Margin → Outside spacing
- Padding → Inside spacing
- Flexbox → One-dimensional layout
- Grid → Two-dimensional layout
- Media Query → Responsive design

  # Git & GitHub

Although Git and GitHub are often used together, they serve different purposes.

## Git vs GitHub

| Git | GitHub |
|------|---------|
| Version Control System | Cloud platform for Git repositories |
| Tracks changes locally | Hosts repositories online |
| Works without internet | Makes collaboration and sharing easier |

---

## Git Workflow

Whenever I worked on a project, my changes followed this workflow:

```text
Working Directory
        │
     git add
        │
        ▼
  Staging Area
        │
   git commit
        │
        ▼
 Local Repository
        │
    git push
        │
        ▼
     GitHub
```

---

## Common Git Commands

| Command | Purpose |
|----------|---------|
| `git init` | Initialize a repository |
| `git status` | Check repository status |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save a snapshot |
| `git push` | Upload commits to GitHub |
| `git pull` | Download latest changes |
| `git clone <url>` | Copy a repository |
| `git branch` | List or create branches |
| `git checkout <branch>` | Switch branches |
| `git merge` | Merge branches |

> **Tip:** Writing meaningful commit messages makes it easier to understand the project's history later.

---

# GitHub Pages

GitHub Pages allows static websites to be hosted directly from a GitHub repository.

## Steps

1. Push the project to GitHub.
2. Open **Repository Settings**.
3. Go to **Pages**.
4. Select the branch.
5. Save the settings.
6. GitHub generates a live website link.

---

# Markdown

Markdown is a lightweight language used for writing documentation.

I used Markdown to create README files because it is simple, readable, and supported by GitHub.

## Common Syntax

| Syntax | Output |
|---------|--------|
| `# Heading` | Heading |
| `**Text**` | **Bold** |
| `*Text*` | *Italic* |
| `` `code` `` | `code` |
| `- Item` | Bullet List |
| `1. Item` | Numbered List |

---

# Tools I Used

| Tool | Purpose |
|------|---------|
| VS Code | Writing and managing code |
| Chrome DevTools | Inspecting HTML, CSS, and Network requests |
| Git | Version control |
| GitHub | Hosting repositories |
| GitHub Pages | Hosting static websites |
| Dillinger | Writing and previewing Markdown |

---

# Key Learnings

- Understanding concepts is more important than memorizing syntax.
- Writing clean HTML makes CSS easier to manage.
- Git provides confidence to experiment because changes can always be tracked.
- Browser Developer Tools are essential for debugging.
- Building projects is the best way to strengthen fundamentals.
- Clean code, meaningful file names, and proper folder structure make projects easier to maintain.

---
## Quick Revision

- Git → Version control
- GitHub → Online repository hosting
- Commit → Snapshot of changes
- Push → Upload changes
- Pull → Download latest changes
- GitHub Pages → Host static websites
- Markdown → Documentation
---
  # JavaScript Functions & Events

JavaScript is what makes webpages reactive and interactive.

---

# What is a Function?

A function is a reusable block of code that does one job. You write it once, then run it whenever you need it, as many times as you like.

## Why use Functions?

- **Reusability:** Write once, use many times.
- **Maintainability:** Fix a bug in one place rather than in multiple places.
- **Organized code:** Each job lives in its own designated box.
- **Easier debugging:** Problems are much easier to locate.
- **Better readability:** A well-named function explains exactly what it does.
- **Unit testing:** Small pieces of logic are simple to test independently.

> **Rule of Thumb:**  
> A good function has a single responsibility. Keep it short (around 20–30 lines). If you cannot describe what it does in one short sentence, it is probably doing too much and should be split up.

---

# Syntax: Parameters vs Arguments

## Parameters

Parameters are the names in the function definition. They act as placeholders for the values that will be passed later.

## Arguments

Arguments are the actual values you pass when calling the function.

---

# The `return` Statement

The `return` statement sends a value back out of the function so you can use it elsewhere in your program.

Once `return` executes, the function stops immediately.

Functions without a `return` statement automatically return `undefined`.

---

# Pure vs Impure Functions

## Pure Functions

Pure functions always produce the same output for the same input.

They:

- Have no side effects.
- Don't modify anything outside themselves.
- Are easy to test and predict.

## Impure Functions

Impure functions interact with the outside world.

Examples include:

- Modifying the DOM
- Reading or changing global variables
- Using random values
- Accessing the current date or time

---

# Ways to Write a Function

| Style | Syntax |
|--------|--------|
| Function Declaration | `function add(a, b) { return a + b; }` |
| Function Expression | `const add = function(a, b) { ... };` |
| Arrow Function (Full Body) | `const add = (a, b) => { return a + b; };` |
| Arrow Function (Implicit Return) | `const add = (a, b) => a + b;` |

---

# JavaScript Events

An event is something that happens on the webpage, such as a click, key press, or form submission.

You attach a function that runs whenever that event occurs to make the page interactive.

---

# `addEventListener()`

`addEventListener()` is the primary method for handling events.

It requires:

1. The event name.
2. A callback function that runs when the event occurs.

> **Note:** Pass named callbacks **without parentheses**.
>
> ✅ `changeColor`
>
> ❌ `changeColor()`
>
> Using parentheses executes the function immediately instead of waiting for the event.

---

# Common Events

| Event | Fires When... |
|--------|---------------|
| `click` | An element is clicked |
| `mousemove` | The mouse moves over an element |
| `keydown` | A key is pressed |
| `input` | The value of an input field changes |
| `submit` | A form is submitted |

---

# The Event Handling Pattern

Almost every interactive feature on the web follows this simple loop:

1. Select the element using `querySelector()`.
2. Listen with `addEventListener()`.
3. Do something inside the callback function (usually modify the DOM).

To remove an event listener, use `removeEventListener()`. It only works if you pass the **exact same named function** that was originally added.

---

# Graceful Degradation

A webpage should still make sense even without JavaScript.

The core content, navigation, and links should function using plain HTML, while JavaScript enhances the user experience with additional interactivity.

---

# Quick Revision

- Function → Performs one specific task.
- Parameters → Placeholders in the function definition.
- Arguments → Actual values passed to the function.
- Return → Sends a value back.
- Callback → Function passed to another function without parentheses.
- `addEventListener()` → Listens for events.
- Event → User or browser action.
- Interactivity Loop → **Select → Listen → Do**

---

# Final Note

This repository documents my learning during the initial phase of my web development internship.

I will continue updating it as I learn new concepts, build more projects, and improve my development skills.

