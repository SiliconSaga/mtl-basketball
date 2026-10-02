---
layout: page
title: Middle School Evaluations
edit_path: _data/evaluations.yml
---

Middle school players attend **one** evaluation night before the season so the coordinators can make balanced teams. Elementary players don't need one.

## What to Expect

- Pick **any one** of the dates below — there's no need to attend more than one.
- Arrive **any time between {{ site.data.evaluations.window }}**. The evaluation itself takes {{ site.data.evaluations.duration }}.
- It's a look at where each player is so the teams come out balanced — an inclusive in-house league, not a tryout.

## Dates

All sessions are at [{{ site.data.evaluations.venue }}]({{ site.baseurl }}{{ site.data.evaluations.venue_url }}), {{ site.data.evaluations.window }}.

| Date | Time |
|---|---|
{% for d in site.data.evaluations.dates %}| {{ d }} | {{ site.data.evaluations.window }} |
{% endfor %}

The dates are also listed on the [middle school registration form](https://registration.teamsnap.com/form/81126). Please [register]({{ site.baseurl }}/register/) before coming to an evaluation.

## What to Wear

Gym clothes and sneakers. Basketballs are provided.

> **Coordinator input needed:** which door to use at Edison, and what happens if a player can't make any of the five dates.

## Questions?

Email [basketball.mtl@gmail.com](mailto:basketball.mtl@gmail.com).
