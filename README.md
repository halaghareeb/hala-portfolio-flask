# Hala Ghareeb — Portfolio (Python / Flask)

A light-themed, responsive portfolio website built with Python and Flask.

## Run it

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000

## Edit content

All text, links and images are in **`data.py`**. Change it there; the templates update automatically.

## Project structure

```
app.py                 Flask routes (+ "freeze" command for static export)
data.py                All page content
templates/
  base.html            Shared header, navigation and footer
  _macros.html         Reusable pieces (icons, buttons, project rows)
  index.html           Home
  solutions.html
  dashboards.html
  educational_projects.html
  achievements.html
  training_and_skills.html
  404.html
static/css/style.css   Styling (colors are CSS variables at the top)
static/js/main.js      Mobile menu, image lightbox, scroll animations
```

## Pages

| URL | Page |
|---|---|
| `/` | Home |
| `/solutions` | Solutions |
| `/dashboards` | Dashboards |
| `/educational-projects` | Educational Projects |
| `/achievements` | Achievements |
| `/training-and-skills` | Training and Skills |

## Deploy

- **Free static hosting (GitHub Pages, Netlify, Cloudflare Pages):** run `python app.py freeze`
  and upload the generated `build/` folder.
- **Python hosting (Render, Railway, PythonAnywhere):** deploy as a Flask app
  (for production use a server such as `gunicorn app:app`).

## Images

Images currently load from the original Odoo site. To host them yourself, save them in
`static/images/` and change `IMG` at the top of `data.py` to `"/static/images/"` (keeping the file names).

## Icons

The Explore section uses Lucide icons, distributed under the ISC License. See
[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) for the license text.
