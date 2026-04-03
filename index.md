---
title: Lachlan Alston
---

# Lachlan Alston

Senior technician at an MSP, FOSS advocate, suckless enthusiast.

I troubleshoot and maintain IT environments for a living, own 3CX deployments end-to-end, and spend too much time scripting things that could probably stay manual. I run Linux, self-host what I can, and believe in not overcomplicating things.

This site is where I write about the things I'm researching, problems I've solved, and software I think is worth using.

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
