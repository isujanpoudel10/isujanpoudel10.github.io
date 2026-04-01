---
layout: page
title: education
permalink: /education/
description: Academic background and graduate study.
nav: true
nav_order: 4
---

{% assign entries = site.data.cv.cv.sections.Education %}

<div class="cv">
  <div class="card mt-3 p-3">
    <h3 class="card-title font-weight-medium">Education</h3>
    <div>
      {% include cv/education.liquid %}
    </div>
  </div>
</div>
