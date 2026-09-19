# jaylee00.github.io

Personal academic portfolio of **Jaesung Lee** — robotics research at the Center for Humanoid
Research, KIST, and Korea University.

Live at **https://jaylee00.github.io/**

## What this is

A dependency-free static site. The visual language is adapted from the
[al-folio](https://github.com/alshedivat/al-folio) Jekyll theme (MIT), but there is no Jekyll, no Ruby
and no build step here — GitHub Pages serves the files exactly as they are committed. Push to `main`
and the change is live in about a minute.

## Layout

```
index.html           about page: bio, news, selected publications, selected projects
publications.html    full publication list, DexFIT abstract, results table, BibTeX
projects.html        project cards, DexFIT featured first
cv.html              research experience, publications, projects, skills
repositories.html    public GitHub repositories
404.html             not-found page
assets/css/main.css  all styling, light and dark themes
assets/js/main.js    theme toggle and mobile navigation
assets/img/          profile picture and project figures
```

## Editing

**Add a publication.** Open `publications.html`, copy one `<li>` block inside
`<ol class="bibliography">`, and replace the fields. Drop the preview image in `assets/img/`.
Mirror the entry in the `selected publications` list in `index.html` if it belongs on the front page.

**Add a project.** Copy a `<div class="card">` block in `projects.html`. Cards without a photo use
`<div class="card-ph"><i class="fa-solid fa-..."></i></div>` in place of the `<img class="card-img">`.

**Add a news item.** Add a `<tr>` to the news table in `index.html`.

**Complete the CV.** The education block in `cv.html` is commented out because the degrees and dates
were not known when the page was built. Fill in the fields and remove the comment markers.

**Replace the profile picture.** `assets/img/prof_pic.jpg` is a monogram placeholder. Overwrite it
with a photo — square crop, around 720×720, keep the filename.

**Change the accent colour.** Edit `--global-theme-color` in `assets/css/main.css`. It is defined
separately for the light theme, the dark theme, and the `prefers-color-scheme` fallback; change all
three. The current values are al-folio's own purple `#b509ac` and cyan `#2698ba`.

## Local preview

No build needed. Any static server works:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Credits

Design adapted from [al-folio](https://github.com/alshedivat/al-folio) by Maruan Al-Shedivat and
contributors, MIT License. Icons from [Font Awesome](https://fontawesome.com/). Fonts from Google
Fonts. Figures are from the DexFIT project.
