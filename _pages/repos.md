---
layout: page
permalink: /repos/
title: repos
description: >
  The following statistics and repositories offer a glimpse into my technical
  proficiency and contributions on GitHub.
nav: true
nav_order: 3
---

{% if site.data.repos.github_users %}
<div class="repos d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repos.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repos.github_users %}
  {% if site.data.repos.github_users.size > 1 %}
  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repos d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.html username=user %}
  </div>

  ---

{% endfor %}
{% endif %}
{% endif %}

## GitHub repos

{% if site.data.repos.github_repos %}
<div class="repos d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repos.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
