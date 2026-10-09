---
layout: page
title: MTL Basketball
---

MTL Basketball is part of the [Mountain Top League](https://mountaintopleague.com/), an all-volunteer organization serving the children of West Orange, NJ since 1959. We're an inclusive in-house league for players of all skill levels: local teams, local games, a focus on developing skills and learning the game the right way — and, most of all, making sure everyone has a blast.

<img class="site-photo" src="{{ site.baseurl }}/flyers/basketball-2026/exports/mtl-basketball-hero.png" alt="MTL Basketball — Winter 2026–27 season, registration open">

## {{ site.data.season.name }} Season

Registration is open for both leagues. Each has a boys league and a girls league.

<div class="picker-grid">
{% for d in site.data.divisions %}
  <a href="{{ site.baseurl }}/register/#{{ d.slug }}" class="picker-card">
    {{ d.name }}
    <small>{{ d.grades }} &middot; boys &amp; girls{% if d.evaluation %} &middot; evaluation required{% endif %}</small>
  </a>
{% endfor %}
</div>

<div class="key-dates">
  <div class="key-date"><strong>{{ site.data.season.early_fee }} early bird</strong><small>through {{ site.data.season.early_deadline }}, then {{ site.data.season.fee }}</small></div>
  <div class="key-date"><strong>Registration closes</strong><small>{{ site.data.season.close_date }}</small></div>
  <div class="key-date"><strong>Practices begin</strong><small>{{ site.data.season.practices_start }}</small></div>
  <div class="key-date"><strong>Games begin</strong><small>{{ site.data.season.games_start }} &middot; season runs {{ site.data.season.season_span }}</small></div>
</div>

[**Go to registration →**]({{ site.baseurl }}/register/)

## Latest News

{% include post-list.html limit=2 %}

[All news, and how to follow it →]({{ site.baseurl }}/news/)

## Middle School Players: One Evaluation Night

Middle school players attend one short evaluation so we can make balanced teams. Five dates to choose from at Edison Middle School, any time between 6:30 and 8:30 pm — details on the [Evaluations]({{ site.baseurl }}/evaluations/) page.

## New to MTL Basketball?

Read [How MTL Basketball Works]({{ site.baseurl }}/how-it-works/) for an overview of the leagues, the season, and what to expect, or jump straight to [registration]({{ site.baseurl }}/register/).

## Get Involved

MTL is run entirely by volunteers — every coach is a parent or neighbor who stepped up. We have short forms for anyone interested in [coaching or sponsoring a team]({{ site.baseurl }}/get-involved/), and the cross-sport [MTL Volunteering guide](https://volunteering.mountaintopleague.com/) covers the League House, gear, sportsmanship, and safety.

## Other MTL Sports

Looking for another sport? Start at the [Mountain Top League site](https://mountaintopleague.com/) — soccer and hockey have their own homes at [MTL Soccer](https://soccer.mountaintopleague.com/) and [MTL Hockey](https://hockey.mountaintopleague.com/).
