# Gopika Govindan – Clinical Psychologist website

Single-page Hugo site, published with GitHub Pages:
https://mohan8488.github.io/gopika-psychology/

## Editing content

Almost all text lives in `data/`:

| File | What it controls |
|---|---|
| `data/site.yaml` | Site description, licences and legal notice (`practice`), Impressum, About section, qualifications, experience (CV) |
| `data/hero.yaml` | Top section: badge, headline, buttons, tick list |
| `data/contact.yaml` | Contact details and booking button |

Layouts are in `layouts/`, styles in `static/css/`.

## Preview locally

```bash
hugo server --disableFastRender --poll 700ms
```

Then open the address Hugo prints (it ends in `/gopika-psychology/`).

## Publishing

Every push to `main` builds and deploys the site automatically
(`.github/workflows/publish.yaml`).

## CV (PDF)

`static/cv/Gopika-Govindan-CV.pdf` is generated from the `/cv/` page.
After changing the CV data, regenerate it with the command in
`layouts/_default/cv.html`.

## Before launch

The site is in preview mode (`demo = true` in `hugo.toml`): hidden from
search engines and showing a "Preview" banner. Before setting it to `false`:

- [ ] DHA licence number (`practice.licences` in `data/site.yaml`)
- [ ] RCI registration number, or remove India as a client region
- [ ] Postal address for the Impressum (`impressum.address`)
- [ ] Real email and phone (`data/contact.yaml`)
- [ ] Privacy policy (GDPR)
- [ ] Legal review of titles and cross-border practice
