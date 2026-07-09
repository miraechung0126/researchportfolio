# Mirae Research Portfolio Starter

This starter uses **Jekyll + GitHub Pages + Decap CMS**.

## What is included
- Home page based on your temple food portfolio design
- Collection pages for Journal, Interviews, Sources & Notes, and Final Reflection
- Decap CMS admin panel at `/admin`
- Starter entries in each collection

## Before publishing
Edit these placeholders first:
- `_config.yml` → set `url` to your final site URL after Pages is live
- `admin/config.yml`
  - replace `YOUR_GITHUB_USERNAME/YOUR_REPO_NAME`
  - replace `site_url` and `display_url`

## Important caveat about Decap CMS login
Decap's **GitHub backend** works, but the official docs note that GitHub authentication requires a server, and Netlify is the simplest way to facilitate that authentication. If you want the CMS login to work without writing your own OAuth server, the easiest route is:

1. Host the site on **GitHub Pages**
2. Use **Decap CMS** for the admin UI
3. Use **Netlify authentication / OAuth helper** only for the login part

If you skip that step, the site will still publish on GitHub Pages, but `/admin` won't be able to save content yet.

## GitHub Pages setup
1. Create a new GitHub repo
2. Upload all files in this folder
3. In GitHub repo settings → Pages
4. Set source to `Deploy from a branch`
5. Select `main` and `/ (root)`

GitHub Pages supports Jekyll in public repositories on GitHub Free.

## Custom domain
Once the site is live, connect your custom domain in GitHub Pages settings.

## Local test (optional)
If you want to test locally later:
```bash
bundle exec jekyll serve
```

## Folder structure
- `_journal` → journal entries
- `_interviews` → interview entries
- `_sources` → source notes
- `_reflections` → reflection posts
- `admin` → Decap CMS files
- `assets/images` → site images
- `assets/uploads` → CMS uploads

## Best next step
Get the site live on GitHub Pages first. Then decide whether you want:
- Netlify auth helper for Decap login
- or a custom OAuth solution later
