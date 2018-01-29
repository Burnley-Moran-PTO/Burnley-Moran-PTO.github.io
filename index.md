---
title: Home
permalink: /

layout: home

hero:
  image: /assets/img/hero.jpg
  callout:
    text: "Help support Burnley-Moran"
  content: Make a donation to the Burnley-Moran Elementary School PTO.
  button:
    href: https://squareup.com/store/burnleymoranpto
    text: Make a donation today

tagline: Welcome Bobcat families!
intro: |
  The funds raised by the PTO go directly back into the school to impact all BME students. The PTO pays for field trips, playground equipment, school landscaping improvements, teacher appreciation events, and many other events, activities, and supplements. PTO-sponsored activities and events not only raise much-needed funds but are also a great way to become a part of the Bobcat family!

  *We welcome all parents of Burnley-Moran students to participate in the PTO. Our meetings take place on the third Thursday of the month and free childcare is provided.*
---

{% assign hero = page.hero %}
{% include components/hero.html %}

{% if page.tagline and page.intro %}
<section class="usa-grid usa-section">
  <div class="usa-width-two-thirds">
    <h2>{{ page.tagline }}</h2>
    {{ page.intro | markdownify }}
  </div>
  <div class="usa-width-one-third">
    <h3>Upcoming events</h3>
    <ul>
      {% assign sortedEvents = site.events | sort: 'event_date' %}
      {% for event in sortedEvents %}
        <li><a href="{{ event.url }}">{{ event.title }}</a><br>
        <em>{{ event.event_date | date: "%m/%d/%Y" }}</em></li>
      {% endfor %}
    </ul>
  </div>
</section>
{% endif %}
