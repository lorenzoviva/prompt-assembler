# Prompt Assembler

**Prompt Assembler** is a Python script that takes a Markdown file as input and produces a new Markdown file where every link to a **local file** is replaced with a fenced code block containing the contents of that file.

---

### Example

Input (`README.md`):

```md
## Content script JS file:
[content.js](../content/content.js)
```

Output:

````md
## Content script JS file:
```js
// === constants ===
const CONTENT_DELAY = 1000;
...
```
````

The script automatically detects the file type (based on extension) and sets the correct language tag for the code fence.

---

### Usage

1. Place the script in the same folder as the Markdown file you want to process.
2. Run the script from the terminal:

```bash
python assemble.py input.md output.md
```

This will create `output.md` where all local file links have been replaced with embedded code blocks.
