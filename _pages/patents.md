---
layout: archive
title: "Patents"
permalink: /patents/
author_profile: true
---

{% include base_path %}

{% for patent in site.patents reversed %}
  <div class="patent-item">
    <h3 class="patent-title">{{ patent.title }}</h3>
    <div class="patent-authors">Inventors: {{ patent.authors | join: ", " }}</div>
    <div class="patent-description">{{ patent.description }}</div>
    <div class="patent-links">
      <a href="{{ patent.link }}" target="_blank">View Patent</a>
      {% if patent.pdf %}
        | <a href="{{ patent.pdf }}" target="_blank">PDF Version</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
