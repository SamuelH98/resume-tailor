# Resume Tailor

Browser-based resume tailor that matches job descriptions against your skills and projects, then compiles a tailored one-page PDF using the **Typst compiler running as WebAssembly** — entirely client-side. No server, no API keys, no data ever leaves the browser tab.

## How It Works

1. Paste a job description into the input panel
2. Skills, projects, experience, and coursework are scored against the JD using tag-based matching with synonym expansion
3. The top-matching items are assembled into a Typst document
4. Typst WASM compiles the document to SVG (live preview) and PDF (download) directly in the browser

## Stack

- Vanilla HTML/CSS/JS (no frameworks)
- [Typst](https://github.com/typst/typst) WASM compiler for PDF/SVG generation
- Tag-based matching with regex caching and synonym expansion

## Usage

Open `index.html` in a browser (or serve with any static file server):

```bash
npx serve .
```

Or deploy to GitHub Pages — no build step required.

## Customization

Edit `resume-data.js` to replace the sample data with your own:

- `header` — name, phone, email, LinkedIn, website
- `education` — degrees, dates, metadata
- `skillCategories` — grouped skills with tags for matching
- `experience` — work history with tagged bullets
- `projects` — portfolio projects with stack and tagged bullets
- `coursework` — relevant coursework with tags

## License

MIT
