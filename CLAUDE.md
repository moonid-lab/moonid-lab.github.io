# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **MOONID LAB** academic website for 호서대학교 AI 융합보안 연구실, built on [Academic Pages](https://github.com/academicpages/academicpages.github.io) — a Jekyll theme for academic portfolios. It is deployed via GitHub Pages at https://moonid-lab.github.io.

## Development Commands

### Local development (Docker — recommended)

```bash
# Build image and start the site at http://localhost:4000
docker compose up --build

# Start without rebuilding the image
docker compose up
```

Docker uses `_config.yml` + `_config_docker.yml` (overrides `url` to `""`).

### Local development (native Ruby)

```bash
bundle install          # install Ruby gems
bundle exec jekyll serve -l -H localhost   # live-reload dev server
```

### JavaScript build

```bash
npm install             # install Node dependencies
npm run build:js        # bundle + minify JS → assets/js/main.min.js
npm run watch:js        # watch assets/js/**/*.js and rebuild on change
```

> The minified `assets/js/main.min.js` bundles jQuery, FitVids, smooth-scroll, Plotly, and the greedy-navigation plugin together with `assets/js/_main.js`.

## Architecture

### Directory roles

| Directory | Role |
|---|---|
| `_pages/` | 직접 노출되는 페이지들 (`/about`, `/cv`, `/publications` 등). 각 파일에 `layout: archive`와 `collection:` 지정이 핵심 |
| `_projects/` | 각 프로젝트 항목 마크다운 파일 (목록 페이지에서 collection으로 렌더링) |
| `_talks/` | 발표 항목 파일들. `talkmap.py`로 위치 데이터를 추출해 Leaflet.js 지도에 출력 가능 |
| `_publications/` | BibTeX 기반 논문 목록. `markdown_generator/`로 자동 생성 |
| `_posts/` | 블로그 글. 파일명은 반드시 `YYYY-MM-DD-title.md` 형식 |
| `_layouts/` | 실제 렌더링 HTML 틀 (`single.html`, `talk.html`, `archive.html` 등). Liquid 문법 사용 |
| `assets/`, `images/`, `files/` | 이미지, 첨부파일(PDF 등) 저장소 |

### Key files

| File | Role |
|---|---|
| `_config.yml` | 사이트 설정의 중심. 어떤 디렉터리를 collection으로 쓸지 지정하고 `defaults:`로 페이지별 기본 layout/author_profile 지정. 라우팅, 테마, 플러그인도 여기서 정의 |
| `_data/navigation.yml` | 상단 헤더 메뉴 구성 (항목 이름, URL 순서 지정) |
| `_config_docker.yml` | Docker 로컬 개발용 오버라이드 (`url: ""`) |

### Content model (Jekyll collections)

Collections are declared in `_config.yml` and determine which directories Jekyll processes into pages:

| Collection | Directory | Default layout |
|---|---|---|
| Publications | `_publications/` | `single` |
| Talks | `_talks/` | `talk` |
| Teaching | `_teaching/` | `single` |
| Portfolio | `_portfolio/` | `single` |

Blog posts live in `_posts/`. Static pages (About, CV, etc.) live in `_pages/` and are included via `include: [_pages]` in `_config.yml`.

### Page rendering flow

1. `_pages/*.md` front matter에서 `layout:` 지정 → `_layouts/` 에서 해당 HTML 템플릿 로드
2. `_layouts/*.html` 내부에서 `_includes/` 파트 조합 (예: `author-profile.html`, `nav.html`)
3. `_sass/` → `assets/css/main.css` 로 컴파일
4. 사이드바 author 정보는 front matter의 `author_profile: true` + `_config.yml`의 `author:` 블록으로 구성

### Navigation menu

`_data/navigation.yml`의 `main:` 목록을 수정해 상단 메뉴를 변경한다. 현재 메뉴:

```
연구(/publications) → 발표(/talks) → 강의(/teaching) → 포트폴리오(/portfolio) → 블로그(/year-archive) → CV(/cv)
```

### Generating content from data

`markdown_generator/` contains Python scripts and Jupyter notebooks to bulk-generate markdown files from TSV/CSV data:

- `talks.py` / `talks.tsv` → individual files in `_talks/`
- `publications.py` / `publications.tsv` (or `.csv`) → individual files in `_publications/`
- `PubsFromBib.ipynb` / `pubsFromBib.py` → generate publications from a `.bib` file
- `OrcidToBib.ipynb` → fetch publications from ORCID and convert to Bib

Run a generator script:
```bash
python3 markdown_generator/publications.py markdown_generator/publications.csv
python3 markdown_generator/talks.py
```

### Talk map

`talkmap_link: false` in `_config.yml` — set to `true` to show the interactive talk map link. The map is rendered by `_pages/talkmap.html` using Leaflet.js. Run `talkmap.py` to regenerate location data from `_talks/` entries.
