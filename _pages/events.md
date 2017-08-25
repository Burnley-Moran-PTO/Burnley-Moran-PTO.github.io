---
title: Events
permalink: /events/
description: The Burnely-Moran PTO sponsors annual fundraising events. Our signature events are the Walk-a-Thon, Sock Hop, Color Run, and Spring Fling!
---

## Upcoming events

{% assign sortedEvents = site.events | sort: 'event_date' %}
{% for event in sortedEvents %}
  * [{{ event.title }}]({{ event.url }})\\
    _{{ event.event_date | date: "%m/%d/%Y" }}_
{% endfor %}

