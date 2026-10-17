# Deploy to Vercel

The site is plain static files, so no config file is needed.

## Folder layout

```
your-repo/
├── index.html
├── DEPLOY.md
└── assets/
    ├── README.txt
    ├── hero.mp4, hero-poster.jpg
    └── <project>.mp4, <project>-poster.jpg
```

## Steps

1. Create a GitHub repo and push the folder above (`index.html` must be at the repo root).
2. Go to [vercel.com/new](https://vercel.com/new) and sign in with GitHub.
3. Click **Import** next to your repo.
4. Set **Framework Preset** to **Other**.
5. Leave **Build Command** empty (turn the override off).
6. Leave **Output Directory** empty (the project root is served).
7. Click **Deploy**. Every push to `main` redeploys automatically.

## Before you go live

- Replace `your-email@example.com` in the `CONFIG` object at the top of the script in `index.html`.
- Add the media listed in `assets/README.txt`.
- Optional: add an `og:image` meta tag pointing to a 1200x630 image in `/assets` for link previews.
- Optional: add a custom domain under **Project → Settings → Domains**.

## Updating content

- Projects, skills and credentials are arrays at the top of the script (`PROJECTS`, `SKILLS`, `CREDS`). Edit data only, never markup.
- Commit and push; Vercel redeploys in about a minute.