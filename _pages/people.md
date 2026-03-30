---
title: People
layout: default
permalink: /people/
published: true
---

## Principal Investigator

<section class="people-spotlight">
  <div class="people-spotlight__photo">
    <img src="{{ site.data.people.pi.photo | prepend: '/assets/images/' | prepend: site.baseurl | prepend: site.url }}" alt="{{ site.data.people.pi.name }}">
  </div>
  <div class="people-spotlight__content">
    <h2>{{ site.data.people.pi.name }}</h2>
    <p class="people-spotlight__title">{{ site.data.people.pi.title }}</p>
    <p>{{ site.data.people.pi.affiliation }}</p>
    <p>{{ site.data.people.pi.bio }}</p>
    <p><a href="mailto:{{ site.data.people.pi.email }}">{{ site.data.people.pi.email }}</a></p>
    <p><a href="{{ site.data.people.pi.cv_url }}" target="_blank" rel="noopener noreferrer">Curriculum Vitae</a> | <a href="{{ site.data.people.pi.scholar_url }}" target="_blank" rel="noopener noreferrer">Google Scholar</a></p>
    <p><a class="feature-card__link" href="{{ '/people/pi/' | relative_url }}">View detailed PI information</a></p>
  </div>
</section>

## Graduate Students

{% if site.data.people.graduate_students and site.data.people.graduate_students.size > 0 %}
<div class="member-grid">
  {% for person in site.data.people.graduate_students %}
    {% include member-card.html person=person %}
  {% endfor %}
</div>
{% else %}
<p class="empty-state">Graduate student profiles can be added here as the group grows.</p>
{% endif %}

## Undergraduate Students

{% if site.data.people.undergraduate_students and site.data.people.undergraduate_students.size > 0 %}
<div class="member-grid">
  {% for person in site.data.people.undergraduate_students %}
    {% include member-card.html person=person %}
  {% endfor %}
</div>
{% else %}
<p class="empty-state">Undergraduate student profiles can be added here.</p>
{% endif %}

## Visiting Students

{% if site.data.people.visiting_students and site.data.people.visiting_students.size > 0 %}
<div class="member-grid">
  {% for person in site.data.people.visiting_students %}
    {% include member-card.html person=person %}
  {% endfor %}
</div>
{% else %}
<p class="empty-state">Visiting student profiles can be added here.</p>
{% endif %}
