---
layout: page
title: Register
# Fees, dates, and sign-up links render from the data files, so the
# "Suggest an edit" button points there rather than at this page's wording.
edit_path: _data/divisions.yml
---

All MTL Basketball sign-ups for the {{ site.data.season.name }} season in one place. Registration runs through TeamSnap; pick the league that matches your child's grade this school year. Each league has a boys division and a girls division.

<div class="key-dates">
  <div class="key-date"><strong>{{ site.data.season.early_fee }} early bird</strong><small>through {{ site.data.season.early_deadline }}</small></div>
  <div class="key-date"><strong>{{ site.data.season.fee }} regular</strong><small>after {{ site.data.season.early_deadline }}</small></div>
  <div class="key-date"><strong>Registration closes</strong><small>{{ site.data.season.close_date }}</small></div>
  <div class="key-date"><strong>Season</strong><small>{{ site.data.season.season_span }} &middot; practices from {{ site.data.season.practices_start }}, games from {{ site.data.season.games_start }}</small></div>
</div>

{% for d in site.data.divisions %}
## {{ d.name }} {#{{ d.slug }}}

**{{ d.leagues }}**{% if d.grades != "" %} &middot; {{ d.grades }}{% endif %} &middot; **{{ site.data.season.fee }}** ({{ site.data.season.early_fee }} early bird through {{ site.data.season.early_deadline }})

{% for item in d.details %}- {{ item }}
{% endfor %}- Games are usually {{ d.games }}, subject to change based on participation

{% if d.evaluation %}
Middle school players also attend **one** [evaluation night]({{ site.baseurl }}/evaluations/) — about 15–20 minutes, any time between 6:30 and 8:30 pm on one of five dates in October and November. The dates are also listed on the registration form.
{% endif %}
[**Register for {{ d.name }} →**]({{ d.register_url }})
{% endfor %}

## West Orange Travel Team Players

Players who make the West Orange Travel Team and would also like to play in MTL Basketball get a discount code. The code comes directly from West Orange Rec once the travel team is set — you don't need to do anything on our end to claim it.

## Questions?

Email [basketball.mtl@gmail.com](mailto:basketball.mtl@gmail.com) or see the [FAQ]({{ site.baseurl }}/faq/).
