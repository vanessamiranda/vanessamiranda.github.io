---
layout: archive
title: "Data Visualisation"
permalink: /dataviz/
author_profile: true
header:
   image: "/images/V3.JPG"
---

*"When you have mastered numbers, you will in fact no longer be reading numbers, any more than you read words when reading books. You will be reading its meanings." ~ W. E. B. Du Bois*
 
I design visualisation to make data interactive, understandable and pretty too :) A take glimpse of projects I've been working on my Tableau Public profile: https://public.tableau.com/profile/vanessa.miranda

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