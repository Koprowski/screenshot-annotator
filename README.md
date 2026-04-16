# Screenshot Annotator

A single-file browser tool for annotating screenshots with numbered highlights and generating structured feedback prompts for AI coding assistants.

**[Try it live](https://koprowski.github.io/screenshot-annotator)** — no install, no signup, runs entirely in your browser.

## What it does

1. Drop a screenshot onto the page
2. Draw numbered highlights, arrows, or shapes on the areas you want to call out
3. Add notes for each annotation
4. Export a structured markdown prompt with all your feedback, ready to paste into Claude Code, Cursor, ChatGPT, or any LLM

Everything runs client-side. Your screenshots never leave your browser.

## Why

Describing visual bugs and UI feedback in text is slow and imprecise. "The button in the upper right is misaligned" could mean five different things. A numbered screenshot with "fix #1, #2, #3" is unambiguous.

This tool bridges the gap between "I can see what's wrong" and "the AI knows exactly what to fix."

## Usage

### Option 1: Use it online
Visit **[koprowski.github.io/screenshot-annotator](https://koprowski.github.io/screenshot-annotator)**

### Option 2: Run it locally
Download `index.html` and open it in any browser. That's it. No build step, no dependencies, no server.

```
curl -O https://raw.githubusercontent.com/Koprowski/screenshot-annotator/main/index.html
open index.html
```

## Features

- Drag and drop or paste screenshots
- Draw rectangles, highlights, and shapes with auto-numbered labels
- Color-coded annotation types (improvements, bugs, questions)
- Add descriptive notes per annotation
- Context field for overall session description
- Export as structured markdown prompt optimized for LLM consumption
- Export annotated image as PNG
- Dark theme UI
- Fully client-side (zero network requests, zero data collection)

## Designed for AI-assisted development

The exported prompt is structured so an AI coding assistant can parse it immediately:

```
I've annotated a screenshot with 3 notes. Please apply the following feedback:

  #1: Move this button 10px to the right
  #2: This text should be centered
  #3: Increase the font size of this heading

Please make all changes in the file, keeping the same overall structure.
```

Pair it with the annotated screenshot and the AI has everything it needs to make precise edits.

## License

MIT
