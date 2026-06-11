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
  fromwheredoesitstem/  # Blog posts
  project/        # Projects
layouts/          # Custom Hugo layout overrides
assets/           # SCSS and other assets
data/             # Structured data files
static/           # Static files (images, PDFs, etc.)
config.yaml       # Main Hugo configuration
netlify.toml      # Netlify build settings
```

## Deployment

Every push to `master` triggers an automatic build and deploy on Netlify. No manual steps required.

## License

Content © JP Flores. Theme licensed under [MIT](https://github.com/hugo-apero/hugo-apero/blob/main/LICENSE).
