---
layout: page
excerpt_separator: <!--more-->
title: awongh blog
tagline: programming and stuff
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    {% assign excerpt_size = post.excerpt.size %}
    <li>
      <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
      <span>{{ post.date | date_to_string }}</span>

      {% if excerpt_size  > 2 %}
        <p>{{ post.excerpt }}
        <p><a href="{{ post.url }}">Read more...</a></p>
        </p>
      {% else %}
        <h1>hello</h1>
        <p>{{ post.content}}</p>

      {% endif %}
    </li>
  {% endfor %}
</ul>
