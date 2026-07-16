---
layout: page
permalink: /grants/
title: Grants & Awards
description: Research funding, fellowships, and selected honors.
nav: true
nav_order: 5
---

{% assign grants = site.grants | sort: "date" | reverse %}

{% if grants.size > 0 %}
  {% for grant in grants %}
### {{ grant.title }}

{{ grant.date | date: "%Y" }}{% if grant.sponsor %} · {{ grant.sponsor }}{% endif %}{% if grant.role %} · {{ grant.role }}{% endif %}

{{ grant.content }}
  {% endfor %}
{% else %}
Funding and award records are being assembled and will be added after verification.
{% endif %}

