#  Full Stack Learning Journal

## About This Repository

This repository contains my notes, projects, and concepts that I learned during my full stack internship. I have documented everything in a simple and organized way so that I can quickly revise the concepts whenever needed.

The goal of this repository is to strengthen my fundamentals and track my learning throughout the internship.

---

##  Table of Contents

* [Projects Built](#-projects-built)
* [How a Website Loads](#-how-a-website-loads)
* [Browser Developer Tools](#-browser-developer-tools)
* [HTML](#-html-hypertext-markup-language)
* [CSS](#-css-cascading-style-sheets)
* [Git & GitHub](#-git--github)
* [GitHub Pages](#-github-pages)
* [Markdown](#-markdown)
* [Tools I Used](#-tools-i-used)
* [Key Learnings](#-key-learnings)

---

#  Projects Built

| Project                 | Skills Practiced                                              |
| ----------------------- | ------------------------------------------------------------- |
| **HTTP Under the Hood** | DNS, HTTP Request & Response, Status Codes, Browser Rendering |
| **Resume (HTML)**       | Semantic HTML, Lists, Images, Links, Tables, Forms            |
| **Resume (HTML + CSS)** | CSS Selectors, Box Model, Flexbox, Grid, Responsive Design    |
| **Personal Portfolio**  | Combining HTML & CSS to build a complete website              |

---

#  How a Website Loads

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

### DNS (Domain Name System)

Computers communicate using **IP addresses**, while humans use domain names like `google.com`.

DNS converts a domain name into an IP address so the browser can locate the correct server.

---

### HTTP Request

The browser sends a request to the server for a resource.

Example:

```http
GET /index.html HTTP/1.1
```

| Method | Purpose              |
| ------ | -------------------- |
| GET    | Retrieve data        |
| POST   | Send new data        |
| PUT    | Update existing data |
| DELETE | Delete data          |

---

### HTTP Response

The server processes the request and returns the requested resource along with a status code.

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

### Common Status Codes

| Code | Meaning               |
| ---- | --------------------- |
| 200  | Success               |
| 301  | Redirect              |
| 400  | Bad Request           |
| 401  | Unauthorized          |
| 403  | Forbidden             |
| 404  | Not Found             |
| 500  | Internal Server Error |

>  **Note**
>
> Opening a webpage doesn't send just one request. The browser makes separate requests for HTML, CSS, JavaScript, images, fonts, and other resources.

---

#  Browser Developer Tools

Developer Tools helped me inspect webpages and debug issues while building projects.

| Tab          | Purpose                        |
| ------------ | ------------------------------ |
| **Elements** | Inspect HTML and CSS           |
| **Network**  | View requests and status codes |
| **Console**  | Check errors and warnings      |
| **Sources**  | View project files             |

Instead of guessing why something wasn't working, I learned to use DevTools to inspect elements, verify file paths, and identify errors more efficiently.

---

##  Quick Revision

* **DNS** → Converts domain name to IP address.
* **HTTP** → Communication between browser and server.
* **GET** → Retrieve data.
* **POST** → Send data.
* **404** → Resource not found.
* **500** → Internal server error.
* **One webpage = Multiple HTTP requests.**
#  HTML (HyperText Markup Language)

HTML is the standard markup language used to create the **structure** of a webpage. It defines what each element represents, while CSS is responsible for its appearance.

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

| Tag               | Purpose                     |
| ----------------- | --------------------------- |
| `<!DOCTYPE html>` | Declares an HTML5 document  |
| `<html>`          | Root element of the webpage |
| `<head>`          | Stores metadata             |
| `<title>`         | Browser tab title           |
| `<body>`          | Visible webpage content     |

---

## Common HTML Elements

| Tag                    | Purpose              |
| ---------------------- | -------------------- |
| `<h1>` - `<h6>`        | Headings             |
| `<p>`                  | Paragraph            |
| `<a>`                  | Hyperlink            |
| `<img>`                | Image                |
| `<ul>`, `<ol>`, `<li>` | Lists                |
| `<table>`              | Display tabular data |
| `<form>`               | Collect user input   |

---

## Semantic HTML

Semantic elements describe the purpose of the content instead of using generic `<div>` elements everywhere.

Example:

```html
<header></header>

<nav></nav>

<main>
    <section></section>

    <article></article>
</main>

<footer></footer>
```

### Common Semantic Elements

| Tag         | Purpose                    |
| ----------- | -------------------------- |
| `<header>`  | Top section of the webpage |
| `<nav>`     | Navigation links           |
| `<main>`    | Main content               |
| `<section>` | Related content            |
| `<article>` | Independent content        |
| `<aside>`   | Sidebar or extra content   |
| `<footer>`  | Bottom section             |

### Why Semantic HTML?

* Improves readability.
* Makes webpages more accessible.
* Helps search engines understand page structure.
* Makes code easier to maintain.

>  **Tip**
>
> Use semantic elements whenever possible. They make your code more meaningful than using `<div>` for everything.

---

## `<div>` vs `<span>`

| `<div>`                  | `<span>`                      |
| ------------------------ | ----------------------------- |
| Block-level element      | Inline element                |
| Used for larger sections | Used for small pieces of text |

---

## HTML Forms

Forms are used to collect information from users.

```html
<form>

    <input type="text">

    <input type="email">

    <input type="password">

    <button>Submit</button>

</form>
```

### Common Input Types

| Type       | Purpose             |
| ---------- | ------------------- |
| `text`     | Text input          |
| `email`    | Email address       |
| `password` | Password            |
| `number`   | Numeric input       |
| `date`     | Date selection      |
| `checkbox` | Multiple selections |
| `radio`    | Single selection    |

---

## Good Practices

* Write clean and properly indented HTML.
* Use semantic elements whenever possible.
* Add meaningful `alt` text to images.
* Use tables only for tabular data.
* Keep file and folder names meaningful.
* Organize HTML before writing CSS.

---

##  Quick Revision

* **HTML** → Webpage structure
* **Semantic HTML** → Meaningful elements
* **`<div>`** → Block element
* **`<span>`** → Inline element
* **`alt`** → Image description for accessibility
* **Forms** → Collect user input
* **Tables** → Only for tabular data
#  CSS (Cascading Style Sheets)

CSS is used to style HTML elements. It controls the colors, fonts, spacing, layout, and responsiveness of a webpage.

---

## Ways to Add CSS

### Inline CSS

```html
<p style="color:red;">Hello</p>
```

Used for small changes but not recommended for larger projects.

### Internal CSS

```html
<style>
    h1 {
        color: blue;
    }
</style>
```

Useful for small webpages.

### External CSS 

```html
<link rel="stylesheet" href="style.css">
```

Best practice because it separates structure (HTML) from styling (CSS).

---

## CSS Syntax

```css
selector {
    property: value;
}
```

Example:

```css
h1 {
    color: royalblue;
    font-size: 32px;
}
```

---

## CSS Selectors

| Selector   | Example   | Purpose                    |
| ---------- | --------- | -------------------------- |
| Element    | `p`       | Selects all `<p>` elements |
| Class      | `.card`   | Reusable styles            |
| ID         | `#header` | Styles one unique element  |
| Universal  | `*`       | Selects every element      |
| Descendant | `nav a`   | Selects child elements     |

>  **Tip**
>
> Use **classes** for reusable styles and **IDs** only for unique elements.

---

## Box Model

Every HTML element is treated as a box.

```text
Margin
┌──────────────────────────┐
│ Border                   │
│ ┌──────────────────────┐ │
│ │ Padding              │ │
│ │ ┌──────────────────┐ │ │
│ │ │ Content          │ │ │
│ │ └──────────────────┘ │ │
│ └──────────────────────┘ │
└──────────────────────────┘
```

| Part    | Purpose                     |
| ------- | --------------------------- |
| Content | Text or image               |
| Padding | Space inside the border     |
| Border  | Boundary around the element |
| Margin  | Space outside the border    |

### Margin vs Padding

| Margin          | Padding        |
| --------------- | -------------- |
| Outside spacing | Inside spacing |

---

## Display Property

| Value          | Purpose                    |
| -------------- | -------------------------- |
| `block`        | Takes full width           |
| `inline`       | Takes only required width  |
| `inline-block` | Inline with width & height |
| `flex`         | Flexible layout            |
| `grid`         | Grid layout                |
| `none`         | Hides the element          |

---

## Flexbox

Flexbox is used to arrange items in a single row or column.

```css
.container {
    display: flex;
}
```

Common properties:

* `justify-content`
* `align-items`
* `flex-direction`
* `gap`

Example:

```text
+-----------------------------+
| Item1   Item2   Item3       |
+-----------------------------+
```

---

## Grid

Grid is useful for layouts with both rows and columns.

```css
.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 20px;
}
```

### Flexbox vs Grid

| Flexbox                  | Grid                           |
| ------------------------ | ------------------------------ |
| One-dimensional layout   | Two-dimensional layout         |
| Best for rows or columns | Best for complete page layouts |

---

## Position Property

| Value      | Purpose                               |
| ---------- | ------------------------------------- |
| `static`   | Default position                      |
| `relative` | Relative to its original position     |
| `absolute` | Relative to nearest positioned parent |
| `fixed`    | Stays fixed while scrolling           |
| `sticky`   | Sticks after reaching a position      |

---

## Responsive Design

Responsive websites adapt to different screen sizes.

Viewport tag:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Media Query:

```css
@media (max-width: 768px) {

}
```

---

## Common Mistakes

* Forgetting to link the CSS file.
* Mixing up margin and padding.
* Using Flexbox properties without `display: flex`.
* Incorrect file paths.
* Missing braces or semicolons.

>  **Common Mistake**
>
> If `justify-content` or `align-items` isn't working, first check whether the parent element has `display: flex`.

---

##  Quick Revision

* **CSS** → Styling
* **Class** → Reusable selector
* **ID** → Unique selector
* **Margin** → Outside spacing
* **Padding** → Inside spacing
* **Flexbox** → One-dimensional layout
* **Grid** → Two-dimensional layout
* **Media Query** → Responsive design
#  Git & GitHub

## Git vs GitHub

Although they are often used together, they are different.

| Git                    | GitHub                                 |
| ---------------------- | -------------------------------------- |
| Version Control System | Cloud platform for Git repositories    |
| Tracks changes locally | Hosts repositories online              |
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

### Workflow Steps

* **Working Directory** → Where I create or modify files.
* **Staging Area** → Selects the changes that will be committed.
* **Local Repository** → Stores commits on my computer.
* **GitHub** → Stores the repository online.

---

## Common Git Commands

| Command                   | Purpose                  |
| ------------------------- | ------------------------ |
| `git init`                | Initialize a repository  |
| `git status`              | Check repository status  |
| `git add .`               | Stage all changes        |
| `git commit -m "message"` | Save a snapshot          |
| `git push`                | Upload commits to GitHub |
| `git pull`                | Download latest changes  |
| `git clone <url>`         | Copy a repository        |
| `git branch`              | List or create branches  |
| `git checkout <branch>`   | Switch branches          |
| `git merge`               | Merge branches           |

>  **Tip**
>
> Writing meaningful commit messages makes it easier to understand the project's history later.

---

## Why Git is Useful

Git helped me:

* Track every change.
* Restore previous versions if needed.
* Experiment without worrying about losing work.
* Maintain a clear history of my projects.

---

#  GitHub Pages

GitHub Pages allows static websites to be hosted directly from a GitHub repository.

### Steps

1. Push the project to GitHub.
2. Open **Repository Settings**.
3. Go to **Pages**.
4. Select the branch.
5. Save the settings.
6. GitHub generates a live website link.

---

## Project Structure

Keeping files organized makes projects easier to manage.

```text
project/
│
├── index.html
├── style.css
├── resume.html
├── images/
├── assets/
└── README.md
```

For GitHub Pages, `index.html` is usually the homepage of the website.

---

#  Markdown

Markdown is a lightweight language used for writing documentation.

I used Markdown to create README files because it is simple, readable, and supported by GitHub.

### Common Syntax

| Syntax       | Output        |
| ------------ | ------------- |
| `# Heading`  | Heading       |
| `**Text**`   | **Bold**      |
| `*Text*`     | *Italic*      |
| `` `code` `` | `Code`        |
| `- Item`     | Bullet List   |
| `1. Item`    | Numbered List |

---

#  Tools I Used

| Tool                | Purpose                                    |
| ------------------- | ------------------------------------------ |
| **VS Code**         | Writing and managing code                  |
| **Chrome DevTools** | Inspecting HTML, CSS, and Network requests |
| **Git**             | Version control                            |
| **GitHub**          | Hosting repositories                       |
| **GitHub Pages**    | Hosting static websites                    |
| **Dillinger**       | Writing and previewing Markdown            |

---

#  Key Learnings

* Understanding concepts is more important than memorizing syntax.
* Writing clean HTML makes CSS easier to manage.
* Git provides confidence to experiment because changes can always be tracked.
* Browser Developer Tools are essential for debugging.
* Building projects is the best way to strengthen fundamentals.
* Clean code, meaningful file names, and proper folder structure make projects easier to maintain.

---

##  Quick Revision

* **Git** → Version control
* **GitHub** → Online repository hosting
* **Commit** → Snapshot of changes
* **Push** → Upload changes
* **Pull** → Download latest changes
* **GitHub Pages** → Host static websites
* **Markdown** → Documentation

---

#  Final Note

This repository documents my learning during the initial phase of my web development internship.

I will continue updating it as I learn new concepts, build more projects, and improve my development skills.
