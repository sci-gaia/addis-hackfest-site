---
layout: page
title: Status
permalink: /ci-cd/
author: brucellino
octocat: jenktocat.jpg
contributors: mario
---
<div class="row"></div>
<strong>Continuous Integration</strong>: The hackfest provides <a href="http://ci.sci-gaia.eu:8080">Jenkins instance</a> to help you do continuous integration on your projects. You can also use <a href="https://travis-ci.com">Travis</a>.
<h3>Project Status <a href="{{ site.url }}/project-status/" class="btn">Project Updates</a></h3>
<!-- all the projects table goes here -->
<table class="table text-center">
<thead>
  <td>
    Name
  </td>
  <td>
    Members
  </td>
  <td>
    Stack
  </td>
  <td>
    Project
  </td>
  <td>
    Platform Components
  </td>
</thead>
{% for project in site.data.cases %}
<tr>
  <td>{{ project.name }}</td>
  <td>
    {% if project.members %}
    {% for member in project.members %}
    <a href="https://githuub.com/{{project.member}}">{{ member }}</a>
    {% endfor %}
    {% else %}
    <!-- <span class="text-danger">No members defined</span> -->
    {% endif %}
  </td>
  <td>
    {% if project.stack %}
    <a href="{{ project.stack }}"><img style="height: 1em;" src="{{ site.url }}images/stackshare.png" /></a>
    {% endif %}
  </td>
  <td>
    {% if project.repo %}
    <a href="{{ project.repo }}"><i class="fa fa-github"></i></a>
    {% endif %}
  </td>
  <td>
    {% if project.components %}
    {% for component in project.components %}
    <span class="label label-primary">{{ component }}</span>
    {% endfor %}
    {% else %}
    <!-- No Platform components specified -->
    {% endif %}
  </td>
</tr>
{% endfor %}
</table>

<h3>Stories from the Hack</h3>
Be sure to check the <a href="{{ site.url }}/updates/">Updates</a> page for commentary of the hack and updates on the projects
