---
layout: page
title: Badrumsrenovering Stockholm Rekommendationer
date: 2016-08-29 15:54:10 +0200
class: testimonial-page
headline: HEADLINE goes here
description: DESCRIPTION goes here
permalink: /rekommendationer/
---
<section class="testimonials section-padding white-bg">
  <h1>Nöjda kunder</h1>
  <div class="flex one two-800">
    {% assign rekommendationer = (site.rekommendationer | sort: 'date') | reverse %}
    {% for rekommendation in rekommendationer %}
      <div class="block">
        <div class="flex one testimonial">
          <h4><a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">{{ rekommendation.title | escape }}</a></h4>
          <blockquote>{{ rekommendation.excerpt markdownify | strip_html | truncatewords: 50 }}</blockquote>
          <div class="testimonial-client">— {{ rekommendation.kund }}</div>
          <a class="post-link" href="{{ rekommendation.url | prepend: site.baseurl }}">Läs mer</a>
        </div>
      </div>
    {% endfor %}
  </div>
</section>
<section class="cta section-padding">
  {% include partials/block_cta.html %}
</section>