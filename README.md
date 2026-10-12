# Dashain Wishes (static, no database)

Everything runs in the visitor's browser. No server, no Supabase, no login.

- `index.html`  – the page your visitors use
- `admin.html`  – your template builder (place name/message/photo by clicking)
- `templates.json` + `templates/` – the list of designs and their images
- `wish.js`, `style.css` – shared code and styling

## Publish (GitHub + Vercel, both free)
1. Create a repo on github.com (New repository, e.g. `dashain-wishes`, Public).
2. In the repo click **Add file -> Upload files**, drag in everything from this folder
   (keep the `templates` folder), then **Commit changes**.
3. Go to vercel.com, sign in with GitHub, **Add New -> Project**, pick the repo.
   Framework Preset: **Other**. Leave Build Command empty. Click **Deploy**.
   (Alternative: GitHub repo -> Settings -> Pages -> Deploy from branch `main` / root.)

## Add a new design
1. Open `https://your-site/admin.html`.
2. Choose your design image, click Name / Message / Photo then click on the image to place it,
   adjust size and colour, **Save to list**.
3. Click **Download templates.json** and the **Image** button of the new design.
4. In GitHub: upload the image into the `templates` folder, upload `templates.json` to the main
   folder (it replaces the old one). Vercel redeploys in about 30 seconds.

## Test on your computer
Browsers block loading `templates.json` when you double-click the file. Run inside the folder:
`python -m http.server` and open http://localhost:8000
