# Prompt Assembler 

Prompt Assembler is a simple python script that takes a markdown file in input and outputs the same file but with every link pointing to a local file replaced with a fenced codeblock containing the code itself. 

For instance by providing this snippet:

```md
## Content script JS file:
[content.js](../content/content.js) 
```


It would output:

````md
## Content scripts Swiper JS file:
```js
// === constants ===
const CONTENT_DELAY = 1000;
...
````

including the whole "content.js" file content inside the fenced codeblock

### Example usage:

Place the script inside the same folder where you have the file you want to assemble.
Run the following command in a terminal:

```
python .\assemble.py codebase.md codebase_assembled.md
```