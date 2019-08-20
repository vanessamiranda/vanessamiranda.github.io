---
layout: archive
title: "Machine Learning"
permalink: /machine/
author_profile: true
header:
   image: "/images/V4.jpg"
---

I design visualisation to make data interactive, understandable and beautiful.Take a glimpse of some projects I've been working on my [Tableau Public profile](https://public.tableau.com/profile/vanessa.miranda)


---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}