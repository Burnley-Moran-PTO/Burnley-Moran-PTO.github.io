---
title: Home
permalink: /
layout: home
hero:
  button:
    href: 'https://squareup.com/store/burnleymoranpto'
    text: Make a donation today
  callout:
    text: Help support Burnley-Moran
  content: Make a donation to the Burnley-Moran Elementary School PTO.
  image: /assets/img/hero.jpg
tagline: Welcome Bobcat families!
intro: >-
  The funds raised by the PTO go directly back into the school to impact all BME
  students. The PTO pays for field trips, playground equipment, school
  landscaping improvements, teacher appreciation events, and many other events,
  activities, and supplements. PTO-sponsored activities and events not only
  raise much-needed funds but are also a great way to become a part of the
  Bobcat family!
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
    {% include events.html %}
  </div>
</section>
{% endif %}
