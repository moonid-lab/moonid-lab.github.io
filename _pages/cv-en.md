---
layout: archive
title: "CV"
permalink: /en/cv/
lang: en
translation_key: cv
author_profile: true
---

{% include base_path %}

## Education

- Soongsil University Graduate School - M.S. in Network Security (2005-2007)
- Soongsil University - B.S. in Electronics and Information Engineering (2001-2005)

---

## Experience

**Hoseo University** - Assistant Professor (2026.02 - Present)  
Asan, Chungcheongnam-do - AI/SecOps Research

**SK Telecom** - Manager (2018.09 - 2026.02)

- AI Agent (2024-2025): LLMOps platform design and development
- VPS (Visual Positioning System, 2023): 3D spatial DB platform design and development
- Road Learner Service (2020-2022): Hybrid cloud architecture and development
- Tview CCTV Surveillance (2019-2020): Public cloud migration leadership (AWS, Azure)

**Pearl Abyss** - SRE & DevOps (2017.03 - 2018.09)

- Black Desert Mobile Azure public cloud transformation

**SECUI** - Senior Research Engineer (2015.12 - 2017.03)

- SIEM development based on IPS/FW intelligent log correlation analysis

---

## Skills

- **AI/ML**: AI Agent, LLMOps, GraphRAG, RAG, MCP
- **Cloud & DevOps**: Kubernetes, AWS, Azure, Docker, CI/CD
- **Security**: IPS/FW, SIEM, vulnerability analysis, network security
- **Development**: Python, Shell, data platform engineering

---

## Publications

{% assign current_lang = page.lang | default: site.locale | slice: 0,2 %}
{% assign lang_publications = site.publications | where: "lang", current_lang %}
{% if lang_publications.size == 0 %}
  {% assign lang_publications = site.publications %}
{% endif %}
<ul>{% for post in lang_publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
