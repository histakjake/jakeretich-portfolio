# jakeretich.com

Personal portfolio website — video editing, photography, and creative work.

## Setup

This is a static site — no build step required. Just serve the files.

### Local development

Open `index.html` in a browser, or use a simple local server:

```bash
npx serve .
```

### Deploy to Cloudflare Pages

1. Push this repo to GitHub
2. Go to [Cloudflare Pages](https://dash.cloudflare.com/) → Create a project → Connect to Git
3. Select this repository
4. Set build settings:
   - **Build command:** (leave empty)
   - **Build output directory:** `/` (or `.`)
5. Deploy

Cloudflare will automatically redeploy whenever you push to the main branch.

## Adding Photos

1. Add image files to `images/photos/`
2. Add a new `<div class="photo-item">` entry in `index.html` inside the `.photo-grid`

## Adding Work/Projects

Edit the `.work-grid` sections in `index.html`. Each project is a `.work-card` div. You can replace the placeholder SVG with an actual thumbnail image:

```html
<div class="work-card">
  <div class="work-card-thumbnail">
    <img src="images/work/thumbnail.jpg" alt="Project name">
  </div>
  <div class="work-card-info">
    <h4>Project Title</h4>
    <p>Description of the project.</p>
  </div>
</div>
```

## Contact Form

The contact form uses [FormSubmit](https://formsubmit.co/) — a free service that forwards form submissions to your email. No backend needed. The first submission will require email verification.

## Custom Domain

In Cloudflare Pages → your project → Custom domains → Add `jakeretich.com`. Since your domain is already on Cloudflare, DNS will be configured automatically.
