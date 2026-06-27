# jpflores.rbind.io

Personal website for JP Flores, built with [Hugo](https://gohugo.io/) and the [hugo-apero](https://hugo-apero-docs.netlify.app/) theme. Deployed via [Netlify](https://www.netlify.com/).

## Stack

- **Framework:** Hugo + [blogdown](https://pkgs.rstudio.com/blogdown/) (R)
- **Theme:** [hugo-apero](https://github.com/hugo-apero/hugo-apero)
- **Hosting:** Netlify (continuous deployment from `master`)

## Local development

**Prerequisites:** R, the `blogdown` package, and Hugo.

```r
# Install blogdown if needed
install.packages("blogdown")

# Install the Hugo version used by this site
blogdown::install_hugo()

# Serve the site locally (live reload at http://localhost:4321)
blogdown::serve_site()
```

Or with Hugo directly:

```sh
hugo server
```

## Project structure

```
content/          # Site content (Markdown / R Markdown)
  about/          # About page
  fromwheredoesitstem/  # Podcast episodes
  marginalia/     # Long-form writing/journal
  project/        # Projects
layouts/          # Custom Hugo layout overrides
assets/           # SCSS and other assets
data/             # Structured data files
static/           # Static files (images, PDFs, etc.)
config.yaml       # Main Hugo configuration
netlify.toml      # Netlify build settings
```

## Adding a marginalia entry

1. Duplicate `content/marginalia/_entry-template/` and rename the folder to your entry's URL slug (e.g. `on-mentorship`).
2. Edit the `index.md` inside:
   - Set `title`, `date`, `excerpt`, and `lead`.
   - Set `draft: false` when ready to publish.
   - Write your entry using `##` headings for sections — the left-margin spine on the reading page builds from these automatically.
3. Optional: drop a `featured.jpg` (200×200) in the folder and add `featured: featured.jpg` to the front matter to show a thumbnail on the index.
4. Commit and push — Netlify deploys automatically.

```sh
git add content/marginalia/your-entry-slug/
git commit -m "Add marginalia entry: your entry title"
git push
```

## Deployment

Every push to `master` triggers an automatic build and deploy on Netlify. No manual steps required.

## License

Content © JP Flores. Theme licensed under [MIT](https://github.com/hugo-apero/hugo-apero/blob/main/LICENSE).
