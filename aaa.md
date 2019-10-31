---
layout: page
title: aaa
sidebar_link: true
---

<p class="message">
  Hey there! This page is included as an example. Feel free to customize it
  for your own use upon downloading. Carry on!
</p>

To make pages show up in the sidebar, add `sidebar_link: true` to the front
matter.

<div id="sidebar">
  <header>
    <{% if page.layout == "index" %}h1{% else %}div{% endif %} class="site-title">
      <a href="{{ "/" | relative_url }}">
        {% unless page.url == "/" %}
          <span class="back-arrow icon">{% include svg/back-arrow.svg %}</span>
        {% endunless %}
        {{ site.title }}
      </a>
    </{% if page.layout == "index" %}h1{% else %}div{% endif %}>
    <p class="lead">{{ site.description }}</p>
  </header>
  {% include sidebar-nav-links.html %}

  {% if site.version %}
    <span class="site-version">Currently v{{ site.version }}</span>
  {% endif %}

  {% include sidebar-icon-links.html %}
  {% include copyright.html %}
</div>
