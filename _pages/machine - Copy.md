---
layout: archive
title: "About"
permalink: /about/
author_profile: true
header:
   image: "/images/KL.jpg"
---

I'm Vanessa, a +9 years experienced digital marketing / eCommerce specialist with +4 years proven track record in the data analytics domain. Turning data into insights and turning insights into value; has always been my passion. 

I am skilled in most data-science steps: data pre-processing, application of statistical modeling, data visualization and results communication. 

I have completed LEAD's Data Science 360 program and IBM's Data Science Professional Certificate, a 9 course program covering Machine Learning. I am currently pursing my MicroMasters in *Statistics and Data Science*, a credential program with Massachusetts Institute of Technology (MIT).

Have fun browsing through my data science portfolio and thanks for visiting!



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