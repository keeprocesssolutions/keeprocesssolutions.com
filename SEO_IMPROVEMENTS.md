# SEO Improvements

## Technical SEO

- Set the production site URL to `https://keeprocesssolutions.com` in `_config.yml` so canonical URLs, Open Graph URLs, and sitemap URLs render as absolute production URLs.
- Removed duplicate manual `<title>` and meta description tags from `_layouts/default.html`; `jekyll-seo-tag` now owns those tags consistently.
- Added a hand-rolled `sitemap.xml` template that lists generated site pages.
- Added `robots.txt` with a sitemap reference.
- Added language, timezone, logo, default image, author, and location/contact metadata to `_config.yml`.

## Structured Data

- Added JSON-LD `ProfessionalService` schema to `_layouts/default.html`.
- Included business name, founder, email, phone, location, area served, logo, image, description, and service types.
- Marked the contact location as an `<address>` element.

## On-Page SEO

- Rewrote page titles and descriptions to be more specific to the business, services, and location.
- Updated the home page H1 and introductory copy to include clearer process development, process improvement, continuous improvement, Modesto, and Central Valley relevance.
- Refined service and about-page copy to include natural service keywords without keyword stuffing.
- Added page-level images in front matter so social previews and SEO metadata have relevant image context.

## Files Changed

- `_config.yml`
- `_layouts/default.html`
- `index.html`
- `about.html`
- `contact.html`
- `assets/css/style.css`
- `robots.txt`
- `sitemap.xml`
- `SEO_IMPROVEMENTS.md`

## Validation Note

- Attempted to run `bundle exec jekyll build`, but the local environment is pinned to Ruby 2.6.10 while `Gemfile.lock` requires Bundler 4.0.8, which requires Ruby 3.2 or newer. The SEO changes are template/content changes only; a build should be run in the deployment environment or after updating the local Ruby/Bundler setup.
