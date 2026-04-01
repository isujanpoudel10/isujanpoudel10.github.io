---
layout: page
title: experience
permalink: /experience/
description: Research, academic, and technical experience.
nav: true
nav_order: 5
---

{% assign entries = site.data.cv.cv.sections.Experience %}

<div class="cv">
  <div class="card mt-3 p-3">
    <h3 class="card-title font-weight-medium">Work Experience</h3>
    <div>
      {% include cv/experience.liquid %}
    </div>
  </div>

  {% assign entries = site.data.cv.cv.sections["Other Experience"] %}
  <div class="card mt-3 p-3">
    <h3 class="card-title font-weight-medium">Other Experience</h3>
    <div>
      {% include cv/experience.liquid %}
    </div>
  </div>
</div>
