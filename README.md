# Communication Theory Primer (Jekyll + GitHub Pages)

This repository contains a Jekyll site scaffold for introducing major schools of communication theory to non-technical audiences, with a focus on contemporary communication issues involving AI.

## Site structure

- `index.md` — home page
- `pages/transmission-view.md`
- `pages/meaning-and-culture.md`
- `pages/interpretation-and-power.md`
- `pages/interpretation-and-intention.md`
- `pages/reader-guidance.md`
- `pages/how-i-built-this-site.md`
- `_layouts/default.html` — shared accessible layout and navigation
- `assets/css/style.css` — custom professional Virginia Tech-inspired palette and styles
- `images/` — place your image assets here
- `_config.yml` — Jekyll and GitHub Pages config
- `.github/workflows/jekyll.yml` — build + deploy action on pushes to `main`

## Add or update content

1. Edit any `.md` page in the root or `pages/` directory.
2. Keep front matter at the top of each page:

   ```yaml
   ---
   title: "Your Page Title"
   ---
   ```

3. Use markdown headings (`#`, `##`, `###`) to organize your analysis.
4. Add links with relative paths (example: `/pages/meaning-and-culture.html`).
5. Add images to `images/`, then reference them in markdown:

   ```md
   ![Descriptive alt text](/comm-primer/images/your-image-file.png)
   ```

   If you later change `baseurl` in `_config.yml`, update hardcoded image paths accordingly.

## Accessibility expectations for your content

When you add your own content:

- Use descriptive heading text in logical order.
- Write meaningful link text (avoid “click here”).
- Add clear alt text for every informative image.
- Keep paragraph blocks short for readability.

The shared layout already includes:

- semantic landmark regions (`header`, `nav`, `main`, `footer`)
- ARIA labels for primary regions
- a keyboard-accessible skip link

## Customize site identity and Pages settings

Edit `_config.yml` as needed:

- `title` — site name in header/tab
- `description` — subtitle and metadata
- `url` — GitHub Pages domain (currently `https://abbyduffer12.github.io`)
- `baseurl` — repository path (currently `/comm-primer`)

For this repository, keep `url` and `baseurl` aligned with username/repo so links resolve correctly when published on GitHub Pages.

## Customize CSS variables (color + style basics)

In `assets/css/style.css`, update the variables in `:root`:

- `--vt-maroon`
- `--vt-orange`
- `--vt-white`
- `--vt-gray-100`
- `--vt-gray-700`
- `--vt-gray-900`

You can also tune spacing and typography in:

- `.container`
- `.site-header`
- `.nav-list a`
- `main`

## Local preview

1. Install Ruby + Bundler.
2. Install dependencies:

   ```bash
   bundle install
   ```

3. Start local server:

   ```bash
   bundle exec jekyll serve
   ```

4. Open `http://127.0.0.1:4000/comm-primer/`.

## GitHub Actions behavior

The workflow at `.github/workflows/jekyll.yml` runs on every push to `main` and will:

1. build the Jekyll site
2. upload the build artifact
3. deploy to GitHub Pages

To publish successfully, ensure GitHub Pages is enabled for this repository with **GitHub Actions** as the source.
