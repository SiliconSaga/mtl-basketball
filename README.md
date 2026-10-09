# MTL Basketball — site

The website for **Mountain Top League basketball** (West Orange, NJ). It's a plain, file-based Jekyll site: every page is a simple text file you (or your AI agent) can edit. No logins to a website builder, no waiting on anyone else.

> **The easiest way to change anything: just ask your agent.**
> *"Add the practice gyms."* · *"Change the early-bird deadline."* · *"Put the playoff photo on the home page."*
> Then look over the PR it opens — every PR automatically gets a **preview site link and a visual diff** so you can see exactly what changes before it goes live.

No agent handy? Every content page on the live site has a **Suggest an edit** button (on tablet-width screens and up) that opens the file behind that page in GitHub's editor — the change comes back as a PR for the league to review, same as above. The flyer previews are standalone print artifacts and don't carry it; edit those under `flyers/` directly.

## How the site is laid out

| You want to change… | Edit this file |
|---|---|
| Home page | `index.md` |
| **News posts** (announcements, social posts) | `_posts/` — one file per post, images in `assets/news/<post>/`; see [News posts](#news-posts) |
| Fees, deadlines, season dates | `_data/season.yml` (Home, Register, How It Works, and FAQ update automatically) |
| Leagues, grade ranges, sign-up links | `_data/divisions.yml` |
| Evaluation nights | `_data/evaluations.yml` |
| Register page wording | `register.md` |
| Gym pages (maps, parking) | `gyms/*.md` |
| How It Works | `how-it-works.md` |
| Coach and sponsor forms | `get-involved.md` |
| FAQ questions & answers | `faq.md` |
| Contact info | `contact.md` |
| Menu | `_data/nav.yml` |
| The "Follow" box on News and posts | `_includes/follow.html` |
| The Print / Suggest an edit buttons | `_includes/page-tools.html` (edit-link base in `_config.yml`) |
| The colors and look | `_sass/_base.scss` |
| Site title / description | `_config.yml` |
| Photos and images | `assets/images/` |
| **Flyers** (print/social) | `flyers/basketball-2026/` — edit the HTML and open a PR; the PDFs/PNGs/JPEGs in `exports/` regenerate automatically (locally, with volundr cloned alongside this repo: `bash ../volundr/flyer-kit/export.sh flyers/basketball-2026`, see [volundr's flyer-kit](https://github.com/SiliconSaga/volundr/tree/main/flyer-kit)) |

Anything the coordinators haven't confirmed yet is marked on the page as **Coordinator input needed** — those callouts are the to-do list. `_docs/` holds the trustee question list and the social-post drafts.

## News posts

When a post goes out on Facebook or Instagram, keep it here too: *"Save today's post to the site news."* Each post is one file in `_posts/` named `YYYY-MM-DD-short-title.md`, with the post text as the body (links written as links, no hashtags) and this front matter:

| Field | Holds |
|---|---|
| `title`, `description` | Headline and one-line summary, shown in lists and feeds |
| `image`, `image_alt` | The main picture, usually the image that was posted |
| `downloads` | Other sizes, as a list of `label` and `file` |
| `featured_until` | Optional date; the league-wide site features the post until then |

Images made for one post go in `assets/news/<post file name>/`; a post about the season flyers points at `flyers/basketball-2026/exports/` instead. Posts show on the News page and the home page, and publish two feeds: `/feed.xml` (Atom, for feed readers; the News page has one-click follow buttons) and `/news/feed.json` (JSON Feed, read by the league-wide site).

## Previewing and publishing

- **Every PR gets a live preview**: a comment appears on the PR with a link to a full preview of the changed site, plus a visual diff against the current site. Review those, then merge — the live site updates within a couple of minutes.
- **Local preview** (optional): `bundle install` once, then `bundle exec jekyll serve` and open <http://localhost:4000/>.
- **Live site**: <https://basketball.mountaintopleague.com/> (old `siliconsaga.github.io/mtl-basketball/` links redirect there).
- Publishing is merge-gated: nothing reaches the live site without a human merging a PR.

## The bigger picture

This is one of the Mountain Top League's per-sport sub-sites, alongside [mtl-soccer](https://github.com/SiliconSaga/mtl-soccer) ([soccer.mountaintopleague.com](https://soccer.mountaintopleague.com/)) and [mtl-hockey](https://github.com/SiliconSaga/mtl-hockey) ([hockey.mountaintopleague.com](https://hockey.mountaintopleague.com/)); the [Mountain Top League site](https://mountaintopleague.com/) remains the league-wide primer and [MTL Volunteering](https://volunteering.mountaintopleague.com/) carries the cross-sport volunteer guide. Architecture notes live in `_docs/plans/`. CI (deploy + PR preview + visual diff + flyer export) is shared via [volundr](https://github.com/SiliconSaga/volundr).
