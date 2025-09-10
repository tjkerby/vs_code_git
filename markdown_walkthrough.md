# Markdown Walkthrough (GitHub-Flavored Markdown)

This mini-guide shows **how to write Markdown** with examples you can copy/paste. It’s GitHub‑Flavored Markdown (GFM), so it works great in README files, issues, and docs.

---

## Headings

Use `#` for headings (1–6).

```md
# H1 title
## H2 section
### H3 subsection
#### H4
##### H5
###### H6
```

Rendered example:

# H1 title
## H2 section
### H3 subsection
#### H4
##### H5
###### H6

> Tip: Headings auto-generate **anchors** on GitHub. Link to them with `#heading-text` (lowercase, dashes for spaces).

---

## Emphasis: bold, italics, strikethrough

```md
*italics* or _italics_
**bold** or __bold__
***bold and italics***
~~strikethrough~~
```

Rendered: *italics*, **bold**, ***bold and italics***, ~~strikethrough~~

---

## Paragraphs & line breaks

- Blank line = new paragraph.
- Two spaces at end of a line = **line break** (soft wrap).

```md
First paragraph.

Second paragraph with a line break␠␠
still same paragraph line.
```

---

## Code: inline & fenced blocks

Inline code uses backticks: ``Use `pip install` to install packages.``

Fenced blocks use triple backticks. Add a language for **syntax highlighting**:

<details>
<summary>Examples</summary>

```python
def add(x, y):
    return x + y
print(add(2, 3))
```

```bash
# Terminal
git status
git checkout -b feature/hello
```

```json
{
  "name": "project",
  "version": "1.0.0"
}
```
</details>

> Tip: Use ` ```text ` for plain text with no highlighting.

---

## Lists: unordered, ordered, nested, and task lists

**Unordered** (use `-`, `*`, or `+`):

- Item A
- Item B
  - Nested item B.1
  - Nested item B.2

**Ordered** (numbers auto-increment—any number in source is okay):

1. Step one
1. Step two
1. Step three

**Task list** (GFM):

- [x] Set up repo
- [ ] Open a PR
- [ ] Request review

---

## Blockquotes

> A single-level quote  

>> Nested quote

---

## Links

**Inline links:**

[OpenAI](https://openai.com)


**Reference-style links:**

See the [docs][docs-link] for details.

[docs-link]: https://example.com/docs


**Relative links (within your repo):**

[Contributing](CONTRIBUTING.md)
[Images](docs/images/)


**Linking to a section on the same page:**

See [Headings](#headings)


---

## Images

![BYU Football Logo](image.png "BYU Logo")


- Use **relative paths** for repo images (e.g., `images/plot.png`).

---

## Tables (GFM)

Basic syntax with optional **alignment** using colons `:`.

```md
| Feature      | Syntax           | Notes                    |
|--------------|------------------|--------------------------|
| Bold         | **text**       |                            |
| Italics      | *text*         |                            |
| Code         | `code`         | Inline code                |

| Left | Center | Right |
|:-----|:------:|-----:|
| a    | b      |   c  |
| long | mid    |  123 |
```

Rendered:

| Feature      | Syntax           | Notes               |
|--------------|------------------|---------------------|
| Bold         | **text**       |                       |
| Italics      | *text*         |                       |
| Code         | `code`         | Inline code           |

| Left | Center | Right |
|:-----|:------:|-----:|
| a    | b      |   c  |
| long | mid    |  123 |

> Tip: You can put inline code, links, and even images inside table cells.

---

## Horizontal rules

Use three or more `-`, `*`, or `_` on their own line:

```md
---
***
___
```

---

## Footnotes (GFM)

```md
Here is a statement with a footnote.[^1]

[^1]: This is the footnote text.
```

Rendered:

Here is a statement with a footnote.[^1]

[^1]: This is the footnote text.

---

## Checkboxes in issues/PRs

Task lists in issues/PRs are interactive on GitHub.

```md
- [ ] Todo item
- [x] Completed item
```

---

## Escaping special characters

Prefix with a backslash to show literal characters:

\*not italic\*

\_not italic\_

\# not a heading

---

## Math (GitHub supports LaTeX-style math)


Inline: $E = mc^2$

Block:
$$
\int_0^1 x^2 \, dx = \frac{1}{3}
$$

> Not all Markdown renderers support math—GitHub does, some others may not.

---

## Putting it all together


# Project Title

Short description with **bold** highlights and `inline code`.

## Features
- [x] Clear README
- [x] Examples in `examples/`
- [ ] Add CI badge

## Example

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

See the [contributing guide](CONTRIBUTING.md) and the [license](LICENSE).

| Command | Description        |
|:--------|:-------------------|
| `make`  | Build the project  |
| `make test` | Run tests     |

![Screenshot](images/screenshot.png)

---

### Quick Reference

- **Headers:** `#` to `######`
- **Bold/Italics:** `**bold**`, `*italics*`
- **Code:** `` `inline` ``, ` ```lang ... ``` `
- **Lists:** `-` / `1.` / `- [ ]`
- **Tables:** pipes `|` + dashes `-` (+ `:` for alignment)
- **Links/Images:** `[text](url)` / `![alt](url)`
- **Quotes/Rules:** `>` / `---`
- **Footnotes:** `[^1]` + definition
- **Escape:** `\` before special chars

Happy writing!
