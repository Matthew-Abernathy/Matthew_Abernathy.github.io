---
layout: page
title: Blog
permalink: blog/
---

<p>Nothing too technical, by and about myself.</p>
<div class="posts">

  {% for post in site.categories.blog %}
    {% unless post.path contains '/chin-' %}
    <article class="post">
      <h2 class="post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">
          {{ post.title }}
        </a>
      </h2>

      <time datetime="{{ post.date | date: "%B %-d, %Y" }}" class="post-date">{{ post.date | date: "%B %-d, %Y" }}</time>

      {{ post.excerpt }}
    </article>
    {% endunless %}
  {% endfor %}
</div>

{%comment%}
<hr/>

<h1>Blog Archive</h1>
<div>
  {% for post in site.categories.blog %}
  <article class="post" style="margin-bottom:1.25em;">
    <h3 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h3>
    <time datetime="{{ post.date | date: "%B %-d, %Y" }}" class="post-date">
      {{ post.date | date: "%B %-d, %Y" }}
    </time>
  </article>
  {% endfor %}
</div>
{%endcomment%}