---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Eilleen's Personal Blog
---

Welcome to my blog! This is the feed of all posts. Click on a post's title to see the full post.


{% for post in site.posts %}
  <div id="post-short">
    <a href="{{site.url}}{{site.baseurl}}{{post.url}}">
      <h3>{{post.title}}</h3>
    </a>
    <i>posted on {{ post.date | date: "%-d %b %Y" }} ||&nbsp;
      {% for category in post.categories %}
        <mark><a href="{{site.url}}{{site.baseurl}}/categories/{{category}}/">#{{category}}</a></mark>
          &nbsp;
      {% endfor %}</i>
    <p>
      {% if post.excerpt %}
        {{ post.excerpt }}
      {% else %}
        {{ post.content }}
      {% endif %}
    </p>
  </div>
{% endfor %}
