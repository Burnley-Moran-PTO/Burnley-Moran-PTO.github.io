---
title: Events
permalink: /events/
---

<p class="usa-font-lead">The Burnely-Moran PTO sponsors annual fundraising events. Our signature events are the Walk-a-Thon, Sock Hop, Color Run, and Spring Fling!</p>

## Upcoming events

{% assign _today = site.time | date: '%Y-%m-%d' %}
{% assign _events = site.events | where_exp: 'event', 'event.event_date > _today' %}
{% if _events.size > 0 %}
<ul>
  {% for event in _events limit:3 %}
    <li><a href="{{ event.url }}">{{ event.title }}</a><br>
    <em>{{ event.event_date | date: "%m/%d/%Y" }}</em></li>
  {% endfor %}
</ul>
{% else %}
<p>
  <em>No upcoming events. Check back soon!</em>
</p>
{% endif %}

