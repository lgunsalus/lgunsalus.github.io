---
layout: page
title: Blog
permalink: /blog/
---

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'blog' %}
      <div class="list-item">
        <p class="list-post-title">
          <a href="{{ post.url | prepend: site.baseurl }}">
              <ul class="post-list"><li><span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
                      <h3>
                        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                          {{ post.title }}
                        </a>
              </h3></li></ul>
              <hr/>
          </a>
        </p>
      </div>
    {% endif %}
  {% endfor %}
</div>

