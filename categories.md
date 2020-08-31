---
layout: default
title: Categories
permalink: /categories/
---

{% for category in site.categories %}

  - [{{category | first}}]({{site.url}}{{site.baseurl}}{{page.url}}{{category | first}})
{% endfor %}
<!---
{% assign cats = (site.categories) %}
 {% for page in cats %}

  - [{{page | first}}]({{site.url}}{{site.baseurl}}{{page.url}}{{page | first}}): {{  page.number | strip_html }}

{% endfor %} --->