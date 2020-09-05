---
layout: default
title: All Posts
permalink: /all/
---


Welcome to my blog! This is the feed of <span class="wavy_underline">all posts in my blog.</span> Click on a post's title to see the full post.


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


<!--- alternatively this for only rendering stuf? doesn't work tho 
{% for cat in site.data.frontpgCategories %}
  {% for post in site.categories[cat.name] %}
    <div id="post-short">
      <a href="{{site.url}}{{site.baseurl}}{{post.url}}">
        <h3>{{post.title}}</h3>
      </a>
      <i>posted on {{ post.date | date: "%-d %b %Y" }}</i>
      <p>
        {% if post.excerpt %}
          {{ post.excerpt }}
        {% else %}
          {{ post.content }}
        {% endif %}
      </p>
    </div>
  {% endfor %}
{% endfor %}--->