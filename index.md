---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: single
author_profile: true
classes: wide
---

Hi! I'm a fifth-year PhD candidate in the Mechanical Engineering department at UC Berkeley. I'm advised by Prof. Kosa Goucher-Lambert in the [Co-Design Lab](https://codesign.berkeley.edu/), where I do research on sustainability and human-centered design processes, helping enable designers to apply sustainability principles in the early stages of design. I am affiliated with the [Berkeley Institute of Design](https://bid.berkeley.edu/) and am generously supported by the [NSF Graduate Research Fellowship](https://www.nsfgrfp.org/). More broadly, I am interested in the intersection of design methods, environmental sustainability, and AI tools.

Previously, I received a B.S. in Mechanical Engineering from MIT, where I worked on ocean acidification research with Dr. Carolina Bastidas at the [MIT Sea Grant](https://seagrant.mit.edu/).

Below you can find my published research projects.

<div class="entries-grid">
  {% assign publications = site.projects | reverse %}
  {% for post in publications %}
    <div class="grid__item">
      <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
        {% if post.header.teaser %}
          <div class="archive__item-teaser">
            <a href="{{ post.url | relative_url }}">
              <img src="{{ post.header.teaser | relative_url }}" alt="">
            </a>
          </div>
        {% endif %}
        <h2 class="archive__item-title" itemprop="headline">
          <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
        </h2>
        <div class="archive__item-excerpt" itemprop="description">
          {{ post.excerpt | markdownify }}
        </div>
      </article>
    </div>
  {% endfor %}
</div>
