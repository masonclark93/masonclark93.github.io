---
layout: page
permalink: /talks/
title: Talks & Presentations
description: Invited talks, conference presentations, seminars, and posters.
nav: true
nav_order: 4
---

{% assign talks = site.talks | sort: "date" | reverse %}

{% if talks.size > 0 %}
  {% for talk in talks %}
### {{ talk.title }}

{{ talk.date | date: "%B %Y" }}{% if talk.venue %} · {{ talk.venue }}{% endif %}{% if talk.location %} · {{ talk.location }}{% endif %}

{{ talk.content }}
  {% endfor %}
{% else %}
Presentation records are being assembled and will be added after verification.
{% endif %}

