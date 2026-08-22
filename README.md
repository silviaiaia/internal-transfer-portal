# Internal Transfer Portal

**[→ Live demo](https://silviaiaia.github.io/internal-transfer_website/)**

A bilingual job board for employees looking to transfer between internal
departments. Built during an internship at a mid-sized electronics
manufacturer to replace an email-and-spreadsheet process for circulating
internal openings.

All job data in this repository is synthetic.

## What it does

- **Bilingual by default** — every posting carries parallel EN / ZH fields;
  the language toggle swaps the entire UI without a page reload.
- **Content-driven** — postings live in `jobs.json`, so HR updates openings
  by editing one file rather than touching markup.
- **Filterable listings** — employees narrow by department, grade and
  contract type before opening a full description.
- **Application flow** — each posting links to an embedded Microsoft Form,
  keeping submissions inside the company's existing tooling.
- **Admin view** — `admin.html` renders the same dataset for HR review.

## Screenshots

<p align="center">
  <img src="docs/screenshots/listings.png" width="600" alt="Job listings">
</p>

## Running locally

```bash
git clone https://github.com/silviaiaia/internal-transfer_website.git
cd internal-transfer_website
python3 -m http.server 8000
```

Then open <http://localhost:8000>. A static server is needed because
`jobs.json` is loaded with `fetch()` — opening `index.html` directly from
the filesystem will fail on CORS.

## Built with

Vanilla HTML, CSS and JavaScript. No framework, no build step.

## License

[MIT](LICENSE).
