---
layout: page
title: projects
permalink: /projects/
description: Selected academic, research, and engineering projects.
nav: true
nav_order: 2
---

{% assign sorted_projects = site.projects | sort: "importance" %}

<div class="cv">
  <div class="card mt-3 p-3">
    <h3 class="card-title font-weight-medium">Projects</h3>
    <ul class="card-text font-weight-light list-group list-group-flush">
      {% for project in sorted_projects %}
        <li class="list-group-item">
          <div class="row">
            <div class="col-xs-12 col-sm-3 col-md-3 text-center date-column">
              {% if project.period %}
                <table class="table-cv">
                  <tbody>
                    <tr>
                      <td>
                        <span class="badge font-weight-bold danger-color-dark text-uppercase align-middle" style="min-width: 110px">
                          {{ project.period }}
                        </span>
                      </td>
                    </tr>
                    {% if project.category %}
                      <tr>
                        <td>
                          <p class="location">{{ project.category | capitalize }}</p>
                        </td>
                      </tr>
                    {% endif %}
                  </tbody>
                </table>
              {% endif %}
            </div>
            <div class="col-xs-12 col-sm-9 col-md-9 mt-2 mt-md-0">
              <h6 class="title font-weight-bold ml-1 ml-md-4">
                <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
              </h6>
              {% if project.description %}
                <h6 class="ml-1 ml-md-4" style="font-size: 0.95rem; font-style: italic">
                  {{ project.description }}
                </h6>
              {% endif %}
              {% assign content_parts = project.content | markdownify | split: '</p>' %}
              {% assign first_paragraph = content_parts[1] | default: content_parts[0] %}
              {% if first_paragraph %}
                <div class="ml-1 ml-md-4">
                  {{ first_paragraph | remove: '<p>' | strip }}
                </div>
              {% endif %}
              <div class="ml-1 ml-md-4 mt-2">
                <a href="{{ project.url | relative_url }}">Read more</a>
              </div>
            </div>
          </div>
        </li>
      {% endfor %}
    </ul>
  </div>
</div>
