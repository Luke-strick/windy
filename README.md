# 505 Rigging — Business Website

A simple static website for a 505 dinghy rigging business. No build step, no
dependencies — just HTML and CSS, so it can be hosted anywhere (GitHub Pages,
Netlify, Vercel, etc.).

## Pages

| Page | File | Purpose |
|------|------|---------|
| Home | `index.html` | Hero, the four services, about section |
| Past Work | `past-work.html` | Project showcase grid |
| Contact | `contact.html` | Contact details and message form |

## Services listed

- Systems for the 505
- Splicing
- Calibration
- Carbon work

## Adding photos

All images are currently "Photo coming soon" placeholders. When you have
photos:

1. Put them in the `images/` folder.
2. Replace a placeholder block like this:

   ```html
   <div class="placeholder">
     <span class="ph-icon">&#128247;</span>
     Photo coming soon
   </div>
   ```

   with an image tag:

   ```html
   <img src="images/my-photo.jpg" alt="What the photo shows">
   ```

## Adding a past-work project

Copy one of the `<article class="project-card">` blocks in `past-work.html`,
then edit the tag, title, and description. There's a comment in the file
marking where.

## Contact form

The form on `contact.html` uses a `mailto:` action, so submitting opens the
visitor's email app — no server required. For a form that emails you directly
without the visitor's email app, sign up for a free service like
[Formspree](https://formspree.io) and swap the form's `action` attribute for
the URL they give you.

## Previewing locally

Just open `index.html` in a browser, or run a tiny local server:

```sh
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Hosting on GitHub Pages

In the repository settings on GitHub: **Settings → Pages → Deploy from a
branch**, choose the default branch and the root folder. The site will be
published at `https://<username>.github.io/<repo>/`.
