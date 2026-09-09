# Resume source

`resume.html` is the source the PDF in the repository root is printed from.

## Rebuilding the PDF

Edit `resume.html`, then print it with headless Chrome:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer \
  --print-to-pdf=Vladyslav-Zvezdaiev-Resume.pdf \
  "file://$PWD/resume-source/resume.html"
```

## Layout notes

- Page size is Letter (612 x 792 pt) with 42 pt side margins.
- Each `<div class="page">` is one printed page with a fixed height, so page
  breaks are explicit rather than automatic. Content that no longer fits is
  clipped instead of flowing over - check both pages after editing.
- Accent colour is `#F20B68`, body text is Arial at 7.5 pt.
- Footers are positioned per page and carry their own page number.
