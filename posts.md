---
title: Posts
---

# Posts

{% if site.posts.size > 0 %}
{% for post in site.posts %}
**[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%B %Y" }}
{{ post.excerpt | strip_html | truncatewords: 30 }}

---

{% endfor %}
{% else %}
Nothing yet. Stay tuned.
{% endif %}
