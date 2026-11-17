# xq95website

Source for [xq95.com](https://xq95.com), the XQ95 company website.

Plain HTML, CSS, and a small amount of JavaScript. No build step and no dependencies.

## Structure

```
index.html              Home
products.html           Private products
open-source.html        Open-source projects
principles.html         Five core principles
about.html              About
contact.html            Contact
blog/index.html         Blog post list
blog/<post>.html        Blog posts
404.html                Not-found page
css/styles.css          All styles and animations
js/main.js              Mobile menu, scroll reveal, card highlight
favicon.png, apple-touch-icon.png  Icons
images/                 Logo files and social preview image
_headers                Security and cache headers (Cloudflare Pages)
sitemap.xml, robots.txt Search engine files
```

## Run locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy (Cloudflare Pages)

- Framework preset: None
- Build command: (leave empty)
- Build output directory: `/`

Every push to the main branch redeploys the site.

## Add a blog post

1. Copy `blog/a-new-direction.html` to `blog/<new-slug>.html` and edit the title, date, description, and body.
2. Add a link to it at the top of the list in `blog/index.html`.
3. Update the "From the blog" card in `index.html`.
4. Add its URL to `sitemap.xml`.

## Header and footer

The header and footer are repeated in every page. When you change one, change it in all pages.
