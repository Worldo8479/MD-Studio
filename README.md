# MD Studio

A PyCharm-style Markdown editor that runs entirely in your browser. Write `.md` files on the left, see the rendered result live on the right, and save real Markdown files to your device. It is one self-contained `index.html` with no install, no build step, no CDN, and it works offline.

![MD Studio split view](screenshot.png)

## Features

- **JetBrains / PyCharm look**: Darcula theme, toolbar, Project sidebar, file tabs, and a status bar showing line:col, selection, word count, LF, UTF-8 and Markdown.
- **Editor**: line numbers, monospace font, current-line highlight and Markdown syntax colouring for headings, lists, tasks, quotes, code, links, bold/italic, tables and rules.
- **Three view modes** (top-right icons, like PyCharm): Editor only, Editor + Preview (scroll-synced split), and Preview only.
- **Files**: create, rename (double-click or pencil icon), delete (with confirmation), and reopen tabs. Files autosave to browser storage.
- **Open** `.md`, `.markdown` or `.txt` files from your device (multi-select, or drag and drop on desktop).
- **Save out**: Download a real `.md` file, Share via the Web Share API (Save to Files on iPad), or Copy the raw Markdown.
- **Formatting bar**: bold, italic, strikethrough, inline code, code block, heading, link, bullet and numbered lists, task, quote, table and horizontal rule. It is touch-friendly.
- **Smart editing**: Enter continues lists and task lists, and Tab / Shift+Tab indent.
- **iPad-ready**: a 16 px editor font so Safari doesn't zoom, 42 px buttons, a collapsible sidebar on narrow screens, and safe-area support.
- **Safe preview**: raw HTML is escaped and `javascript:` links are neutralised.

## Getting started

1. Open `index.html` in any modern browser. On iPad, save it to Files and open it in Safari.
2. Pick `welcome.md` in the Project sidebar, or press **New** to make a file.
3. Type Markdown. The preview updates as you go.
4. Use **Download** or **Share** to get the `.md` file out.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| Ctrl/Cmd + S | Save to browser storage |
| Ctrl/Cmd + Shift + S | Download as `.md` |
| Ctrl/Cmd + B | Bold |
| Ctrl/Cmd + I | Italic |
| Ctrl/Cmd + K | Insert link |
| Tab / Shift + Tab | Indent / outdent |
| Enter | Continue the current list |

## Supported Markdown

Headings, bold, italic, strikethrough, inline code, fenced code blocks, ordered, unordered and nested lists, task lists, links and bare URLs, images, blockquotes, tables, and horizontal rules.

## Limitations

- **Save stays in the browser.** Ctrl/Cmd+S saves to browser storage, not to disk. Use Download or Share to get a file.
- **No sync.** Files live in that browser's localStorage, so they don't sync between devices, and Safari may clear storage for sites you rarely visit. Download anything important.
- **Unsupported Markdown.** Footnotes, reference-style links and raw HTML aren't supported.
- **Preview.** Code blocks aren't syntax-coloured, and task checkboxes are display-only.
- **No line wrap.** Editor lines don't wrap, which keeps the line numbers aligned.

## Files

```
md-studio/
├── index.html   # the whole app
├── README.md    # this file
└── screenshot.png
```

## License

MIT. Use it however you like.
