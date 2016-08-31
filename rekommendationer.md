---
layout: page
title: Badrumsrenovering Stockholm Rekommendation
date: 2016-08-29 15:54:10 +0200
class: rekommendation
headline: HEADLINE goes here
description: DESCRIPTION goes here
permalink: /rekommendationer/
---
<h1>Badrumsrenovering Stockholm Rekommendation</h1>
<div class="latest-testimonials">
  <h2>Nöjda kunder</h2>
  {% assign rekommendationer = (site.rekommendationer | sort: 'date') | reverse %}
  {% for rekommendation in rekommendationer %}
    <div class="testimonial">
      <h4><a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">{{ rekommendation.title | escape }}</a></h4>
      <blockquote>{{ rekommendation.excerpt | strip_html | truncatewords: 50 }}</blockquote>

      <div class="testimonial-client">— {{ rekommendation.kund }}</div>
      <a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">Läs mer</a>
    </div>
  {% endfor %}
</div>