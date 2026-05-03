---
layout: default
title: Lecture Notes
permalink: /notes/
---

These are some lecture notes (some of my own and some from graduate courses that I have taken/suffered in NUS), problem sets and expository notes.

# NUS Lecture Notes

{% assign nus_notes = site.notes | where: "type", "lecture" | where: "institution", "NUS" | sort: "title" %}

{% for note in nus_notes %}
- [{{ note.title }}]({{ note.url | relative_url }}){% if note.description %} — {{ note.description }}{% endif %}
{% endfor %}

# Lecture Notes

{% assign other_lecture_notes = site.notes | where: "type", "lecture" | where_exp: "note", "note.institution != 'NUS'" | sort: "title" %}

{% for note in other_lecture_notes %}
- [{{ note.title }}]({{ note.url | relative_url }}){% if note.description %} — {{ note.description }}{% endif %}
{% endfor %}

# Expository Notes

{% assign expository_notes = site.notes | where: "type", "expository" | sort: "title" %}

{% for note in expository_notes %}
- [{{ note.title }}]({{ note.url | relative_url }}){% if note.description %} — {{ note.description }}{% endif %}
{% endfor %}