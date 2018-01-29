---
title: Events
permalink: /events/
---

<p class="usa-font-lead">The Burnely-Moran PTO sponsors annual fundraising events. Our signature events are the Walk-a-Thon, Sock Hop, Color Run, and Spring Fling!</p>

## Upcoming events

{% assign sortedEvents = site.events | sort: 'event_date' | reverse %}
{% for event in sortedEvents limit:3 %}
  * [{{ event.title }}]({{ event.url }})
    _{{ event.event_date | date: "%m/%d/%Y" }}_
{% endfor %}

