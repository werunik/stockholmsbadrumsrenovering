---
layout: page
title: Stockholms Badrumsrenovering Bloggen
date: 2016-08-29 15:54:10 +0200
class: blog
headline: Besök vår blogg för att få inspiration på badrumsrenovering
description: Besök vår blogg för att få inspiration på badrumsrenovering
permalink: /bloggen/
---
<section class="blog section-padding white-bg">
  <h1 itemprop="name">Stockholms Badrumsrenovering Bloggen</h1>
  <div class="blog flex one two-500 two-800" itemscope="" itemtype="http://schema.org/Blog">
    {% assign posts = (site.posts | sort: 'date') | reverse %}
    {% for post in posts %}
      <article class="post one" itemprop="blogPost" itemscope="" itemtype="http://schema.org/BlogPosting">
        <meta itemprop="description" content="{{ page.description | strip_html | truncatewords: 40 }}">
        <meta itemprop="keywords" content="{{ post.categories | join: ',' }}" />
        <h2>
          <a href="{{ post.url }}" itemprop="url">
            <span itemprop="name">{{ post.title }}</span>
          </a>
        </h2>
        <div class="entry" itemprop="description">
          {{ post.content | strip_html | truncatewords: 40 }}
        </div>
        <a href="{{ post.url }}" itemprop="url" class="read-more">Läs mer</a>
      </article>
    {% endfor %}
  </div>
</section>
<section class="cta section-padding">
  {% include partials/block_cta.html %}
</section>