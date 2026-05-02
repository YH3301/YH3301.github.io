---
layout: page
title: Lecture Notes
permalink: /notes/
---

## Lecture Notes
These are some lecture notes (some of my own and some from graduate courses that I have taken/suffered in NUS), problem sets and expository notes.

## Notes

{% assign notes = site.notes | sort: "title" %}
{% for note in notes %}
- [{{ note.title }}]({{ note.url | relative_url }}){% if note.description %} — {{ note.description }}{% endif %}
{% endfor %}