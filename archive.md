---
layout: default
title: Archive
---

# Archive

Browse all posts by month and year.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h2>{{ yearMonth.name }}</h2>
  <ul>
    {% for post in yearMonth.items %}
<<<<<<< HEAD
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
=======
  <!-- Add "{{ site.baseurl }}" -->
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
>>>>>>> 3fa424f131d2e5477ef010870cac02a6bcf8ff92
    {% endfor %}
  </ul>
{% endfor %}
