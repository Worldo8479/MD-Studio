# MD Studio

A PyCharm-style Markdown editor that runs entirely in your browser. Write `.md` files on the left, see the rendered result live on the right, and save real Markdown files to your device. It is one self-contained `index.html` with no install, no build step, no CDN, and it works offline.

[Website](https://worldo8479.github.io/MD-Studio)

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

## Mac app

There is also a native macOS version that opens and saves real `.md` files on disk (Cmd+S writes to the actual file). It has a macOS menu bar, Open Recent, unsaved-changes warnings, and you can open files from Finder or by dropping them on the Dock icon. Builds are for Apple Silicon (arm64) and Intel (x64), and need macOS 13 or later.

### Install (Apple Silicon)

The app is too big for one download, so it comes in four parts:

- `MD-Studio-arm64.part0`
- `MD-Studio-arm64.part1`
- `MD-Studio-arm64.part2`
- `MD-Studio-arm64.part3`

1. Download all four parts into your `Downloads` folder.
2. Open Terminal and run:

   ```bash
   cd ~/Downloads && cat MD-Studio-arm64.part0 MD-Studio-arm64.part1 MD-Studio-arm64.part2 MD-Studio-arm64.part3 | tar -xJf - && xattr -dr com.apple.quarantine "MD Studio.app" && open "MD Studio.app"
   ```

   This joins the parts, unpacks `MD Studio.app`, removes the macOS quarantine flag, and launches the app.
3. Drag `MD Studio.app` into your `Applications` folder to keep it.
4. Optionally, delete the four part files.

### Gatekeeper note

The app isn't notarized by Apple. Running the `xattr` command above lets it open normally. If you skip that step and macOS blocks the app, do one of these:

- Right-click `MD Studio.app` and choose **Open**, then **Open** again.
- Go to **System Settings > Privacy & Security** and click **Open Anyway**.

### Make it the default for .md files

In Finder, select any `.md` file and press Cmd+I. Under **Open with**, choose **MD Studio**, then click **Change All…**.

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
