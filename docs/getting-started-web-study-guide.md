# 🧠 Getting Started with the Web — Study Guide

## (HTML · CSS · JavaScript · Git · Markdown)

### Note about "directory" versus "folder"

In Computer Science, we tend to use the term `directory` instead of `folder`.

+ **Directory**: A directory is a filesystem concept: a special kind of file that maps names to other files (including other directories). It is defined by the *operating system* and *filesystem*.
For example, here are some common default filesystems for popular operating systems:

| Operating System | Filesystem |
| ---------------- | ---------- |
| Linux            | ext4       |
| Windows          | NTFS       |
| MacOS            | APFS       |

+ **Folder**
A folder is a user-interface metaphor: a visual representation of a directory used by graphical file managers to help humans think about organization.

All folders are directories, but "folder" is a Graphical User Interface (GUI) term; "directory" is the technical file-system term.

However, the terms are often used interchangably.

---

## Big Picture: How the Web Stack Fits Together

| Technology | Main Purpose | Think of it as… |
|----------|-------------|-----------------|
| **HTML** | Structure & content | The *skeleton* of a webpage |
| **CSS** | Look & style | The *clothes* and layout |
| **JavaScript** | Interactivity | The *behavior* and actions |
| **Git** | Track changes | A *time machine* for files |
| **Markdown** | Simple formatting | Easy-to-write text → HTML |

---

## 1️⃣ Git & Repositories

[Git Explained in 100 seconds](https://www.youtube.com/watch?v=hwP7WQkmECE)

### What is a Git repository?
A **Git repository** is:
- A directory where Git tracks changes to files
- It contains a hidden **`.git/` folder** with all history

✔️ True  
- Git tracks changes inside a directory  
- Repository data is stored in `.git/`

❌ False  
- Any folder opened in VS Code is *not automatically* a Git repository

---

## 2️⃣ Default Web Files

### Default homepage filename
When a web server loads a folder, it looks for:

```
index.html
```

---

## 3️⃣ HTML — Structure & Meaning

### What is HTML?
HTML is a **markup language**.

✔️ HTML defines the *structure* of content  
❌ HTML does not style pages or add behavior

---

### Parts of an HTML Element

```html
<p class="sayings">My karma ran over my dogma.</p>
```

| Part | Example |
|----|--------|
| Opening tag | `<p>` |
| Closing tag | `</p>` |
| Content | `My karma ran over my dogma.` |
| Attribute | `class="sayings"` |
| Element | Everything together |

---

### Common HTML Tags

| Tag | Purpose |
|----|--------|
| `<h1>` | Main heading |
| `<h2>` | Level-2 heading |
| `<p>` | Paragraph |
| `<img>` | Image (no closing tag) |
| `<ul>` | Unordered list |
| `<ol>` | Ordered list |
| `<li>` | List item |

---

## 4️⃣ Images & Paths

### `<img>` and `src`

```html
<img src="images/logo.png" alt="School logo">
```

The `src` attribute contains:
- The **path or URL** to the image resource

---

## 📂 Understanding Paths (Relative vs Absolute)

### 1. `/` — Path separator
- `/` separates folders in paths
- Used in **URLs** and **local file paths**

Example:
```
images/logo.png
```

---

### 2. Leading `/` — Root of the site
```html
<img src="/images/logo.png">
```

- Starts from the **root of the website**
- ❗ Not the same as your project folder
- Often **wrong** for local projects unless deployed

---

### 3. `../` — Go *up* one directory
```html
<img src="../images/logo.png">
```

- Means: “go up one folder, then into `images/`”
- Very common when files are in subfolders

---

### 4. `./` — This directory
```html
<img src="./logo.png">
```

- Means: “look in the current folder”
- Often optional, but useful for clarity

---

### 5. URL vs Local Path (Important Concept)

```html
<img src="https://example.com/logo.png">
```

- This is a **URL**
- The image lives *somewhere else on the Web*

```html
<img src="images/logo.png">
```

- This is a **local relative path**
- The image lives **inside your project**

🧠 **Mental model**  
- URL → “out there on the Internet”  
- Relative path → “inside my folder”

---

## 5️⃣ CSS — Styling

CSS:
- Selects HTML elements
- Applies styles (color, size, layout)

```css
p {
  color: red;
}
```

| Term | Meaning |
|----|--------|
| Selector | `p` |
| Property | `color` |
| Value | `red` |

---

### CSS Box Model (Concept)
Every element is a box:

```
margin → border → padding → content
```

---

## 6️⃣ JavaScript — Interactivity

JavaScript:
- Is an **imperative programming language**
- Manipulates the **DOM**
- Responds to **events**

```js
const myHeading = document.querySelector("h1");
myHeading.textContent = "Hello world!";
```

Key ideas introduced:
- Variables
- Functions
- Conditionals
- Events
- DOM selection
- Browser storage

---

## 7️⃣ Markdown

Markdown is:
- A **simple text format**
- Converted into HTML
- Used in `README.md`

```md
# Heading
* List item
```

---

## 8️⃣ Core Match-Ups to Remember

| Purpose | Technology |
|------|------------|
| Change look & style | CSS |
| Track file changes | Git |
| Document structure | HTML |
| Add interactivity | JavaScript |
| Simple text → HTML | Markdown |

---

## 🧩 Final Mental Model

> HTML = what it **is**  
> CSS = what it **looks like**  
> JavaScript = what it **does**  
> Git = what **changed**
