# remark-pdf

![npm](https://img.shields.io/npm/v/remark-pdf) ![check](https://github.com/inokawa/remark-pdf/workflows/check/badge.svg) ![demo](https://github.com/inokawa/remark-pdf/workflows/demo/badge.svg)

[remark](https://github.com/remarkjs/remark) plugin to transform markdown to pdf.

### 🚧 WIP 🚧

The goal is to support all nodes in [mdast](https://github.com/syntax-tree/mdast) syntax tree, but currently transformation and stylings may not be well.

If you have some feature requests or improvements, please create a [issue](https://github.com/inokawa/remark-pdf/issues) or [PR](https://github.com/inokawa/remark-pdf/pulls).

## Demo

https://inokawa.github.io/remark-pdf/

## Install

```sh
npm install remark-pdf
```

## Usage

### Browser

```javascript
import { unified } from "unified";
import markdown from "remark-parse";
import pdf from "remark-pdf";

const processor = unified().use(markdown).use(pdf);

const text = "# hello world";

(async () => {
  const doc = await processor.process(text);
  doc.result.download();
})();
```
