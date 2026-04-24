---
title: Lachlan Alston
---

# Lachlan Alston

Senior technician at an MSP — Windows infrastructure, 3CX, and the automation that makes it manageable. Fifteen years of Linux at home.

This site is where I write about problems I've solved and tools worth using.

---

## Recent Posts

{% if site.posts.size > 0 %}
{% for post in site.posts limit:5 %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%B %Y" }}
{% endfor %}

[All posts →](/posts)
{% else %}
Nothing yet. Stay tuned.
{% endif %}
