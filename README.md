# Guowen Zhang — personal homepage

A minimal academic homepage at [lostgreen.github.io](https://lostgreen.github.io/), inspired by [Boshen Xu](https://xuboshen.github.io/) and [Jon Barron](https://jonbarron.info/).

The homepage is plain HTML and CSS. It uses local fonts and images, with no JavaScript or build step needed for previewing it.

## Preview locally

From the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. Refresh the browser after editing.

## Update the homepage

- `index.html`: biography, contact links, research interests, publications, education, and page metadata.
- `stylesheet.css`: typography, spacing, desktop layout, and mobile layout.
- `images/guowen-zhang.jpg`: 600 × 600 crop of the casual photo supplied by the site owner.
- `images/guowen-zhang-full.jpg`: compressed full photo, opened when clicking the portrait. The previous formal portrait is retained at `images/zjz.png`.
- `images/eventlens.png`: Figure 2 of [arXiv:2610.16172v1](https://arxiv.org/html/2610.16172v1).
- `images/larma.png`: publication thumbnail, sourced from Figure 2 of [arXiv:2503.11074v2](https://arxiv.org/html/2503.11074v2).
- `images/libero-pro.png`: Figure 1 of [arXiv:2510.03827v2](https://arxiv.org/html/2510.03827v2).
- `images/badvla.png`: Figure 1 of [arXiv:2505.16640v1](https://arxiv.org/html/2505.16640v1).
- `images/ocdb.png`: Figure 2 cropped from page 6 of [arXiv:2406.04598](https://arxiv.org/pdf/2406.04598).
- `assets/fonts/`: local Lato fonts and their SIL Open Font License.

To add a publication, copy the `<article class="publication">` block in `index.html` and update the image, title, authors, venue, links, and summary. Put the most recent paper first. Only add links to existing resources.

## GitHub Pages

The existing AcademicPages/Jekyll files and routes are retained. The new `index.html` has no Jekyll front matter, so Jekyll copies it as a static file. `_pages/about.md` redirects `/about/` and `/about.html` to `/` and no longer competes for the root URL.

Publish the changes through the branch configured in the repository's **Settings → Pages**, or merge this branch into that publishing branch. Local edits alone do not change the live site.

The remaining legacy pages can still be built with the original Jekyll setup:

```sh
bundle install
bundle exec jekyll serve
```

## Content and credits

The current biography and email were confirmed by the site owner: first-year master's student at Renmin University of China, member of AIM3 Lab, and `gwzhang111@ruc.edu.cn`. Undergraduate Data Science studies at HUST are retained as prior education.

The original four publications were matched against [Guowen Zhang's Google Scholar profile](https://scholar.google.com/citations?user=gTql04YAAAAJ&hl=en) on October 10, 2026. Titles, full author lists, years, and summaries were checked against the linked arXiv records. LaRMA uses its current arXiv title, which differs from the older title still shown on Scholar. BadVLA is listed as NeurIPS 2025, confirmed by the site owner and the [official proceedings](https://proceedings.neurips.cc/paper_files/paper/2025/hash/b94925a92f2271cd60c9f3f7a7d366fe-Abstract-Conference.html); its title and PDF link to the published version. The other three remain arXiv preprints; project and code links are included where verified.

EventLens was added on October 14, 2026. Its title, author list, summary, and thumbnail were checked against [arXiv:2610.16172](https://arxiv.org/abs/2610.16172). Its NeurIPS 2026 venue was verified against the [official conference listing](https://neurips.cc/Downloads/2026), and dataset/model links were checked against the [project page](https://lostgreen.github.io/EventLens/).

The original AcademicPages template is MIT licensed; see `LICENSE`. Lato is distributed under the license in `assets/fonts/OFL.txt`. Paper thumbnails are credited to their respective authors and source papers linked above; see each arXiv record for its license.
