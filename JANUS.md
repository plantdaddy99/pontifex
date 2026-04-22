# JANUS

### *The Manual of Thresholds, Gates, and Permissions Granted (or Withheld) to Non-Human Readers*

---

> *Iane biceps, anni tacite labentis origo, / solus de superis qui tua terga vides…*
> "Two-faced Janus, source of the silently slipping year, / alone of the gods who sees your own back…"
> — Ovid, *Fasti* I.65–66

---

**Liber inceptus:** 22 April 2026
**Custos:** [your name / handle]
**Sister volumes:** README · TASKS · WORDYWORDS · AIPsy · COLLEGIUM (et alia)

---

## Praefatio Editoris

This manual takes its name from Janus — the Roman god of doorways, thresholds, and transitions, who looks both inward and outward at once. It is a fitting patron for the subject at hand: the architecture of *who may enter*, *what they may read*, *under what terms*, and *with what consequence* — when the would-be visitor is not a human being but a machine, an agent, a model, or some entity that belongs to none of the categories the early web was built to imagine.

JANUS collects documents, configurations, protocols, and editorial commentary on the *threshold layer* of the modern web: the `robots.txt` files, the meta directives, the WAF rules, the API gates, the consent declarations, the licensing flags, and the emerging norms (`ai.txt`, C2PA, model cards as access tokens, etc.) that together constitute the diplomatic protocol between human-built infrastructure and non-human readers.

It is **not** a manual of AI cognition (see `AIPsy.md`).
It is **not** a manual of pedagogy or scholarship (see `COLLEGIUM.md`).
It is the manual of the *door*.

---

## Tabula Capitum *(Table of Chapters — to be filled as entries arrive)*

| № | Liber | Subject | Source | Date Filed |
|---|-------|---------|--------|------------|
| I | *De Hospitalitate Robotica* | Robotic Hospitality on AWS-Hosted Research Sites | AmazonQ | 22 Apr 2026 |
| II | *(reserved)* | — | — | — |
| III | *(reserved)* | — | — | — |

---

## § I — *De Hospitalitate Robotica*

### Of `robots.txt`, Meta Tags, and the Welcoming of Machine Readers

#### Argumentum

A `robots.txt` file is, properly understood, a **social contract written in plaintext** — a declaration nailed to the door of a website, addressed to readers who are not human, written in a dialect they have agreed (more or less) to honor. It is one of the oldest pieces of web etiquette still in active use, and it has lately been pressed into a new role: not merely "keep search engines tidy," but "*declare your stance toward AI*."

The document filed under this chapter (an AmazonQ advisory output) treats the question from the host's side: *how does one constitute a website as a welcoming environment for AI models and research crawlers, particularly when hosted on AWS infrastructure?*

#### Distilled Doctrine

Five strata of welcome, in ascending order of formality:

1. **The Plaintext Welcome** — a permissive `robots.txt` at site root, naming each major AI crawler (`GPTBot`, `ChatGPT-User`, `CCBot`, `anthropic-ai`, `Claude-Web`, `Google-Extended`, `Bingbot`, et al.) and granting `Allow: /` with a courteous `Crawl-delay: 1`.
2. **The Meta Declaration** — HTML `<meta>` tags within the document head explicitly authorizing AI training, data mining, and research use; supplemented by JSON-LD structured data declaring the site's audience as *"AI researchers, machine learning models, academic institutions."*
3. **The Dedicated Vestibule Page** — an `ai-info.html` or `/robots/` landing page addressed *to the bots themselves*, enumerating permissions, supported models, recommended crawl behavior, and contact information for the human stewards.
4. **The Infrastructure Layer** — CloudFront distributions with WAF rules tuned to *whitelist* known AI user-agents while filtering hostile traffic; CloudWatch dashboards to observe the visiting fauna.
5. **The Structured Door** — an API Gateway exposing endpoints (`/api/data`, `/api/experiments`, `/api/metadata`) that serve content in machine-native form, sparing the visitor the work of parsing HTML.

#### Editorial Notes

- The AmazonQ doc is **AWS-flavored throughout**. Equivalent recipes exist for Cloudflare, Vercel, Netlify, and self-hosted nginx — those will be filed as future entries (§ I.b, § I.c, etc.) when collected.
- The doc predates the still-coalescing `ai.txt` standard and the proposed `Robots Exclusion Protocol v2`. When those crystallize, this chapter will need a *codicil*.
- Note the moral asymmetry baked into the recommended config: it *welcomes* GPTBot, anthropic-ai, Claude-Web, Google-Extended (research/AI agents) while *blocking* `SemrushBot` and `AhrefsBot` (commercial SEO scrapers). The criterion is not "is it a bot" but "*what does it want, and is its want compatible with mine?*"

#### Cross-References

- See `AIPsy.md` for the cognitive/behavioral side of why AI agents do (and do not) honor `robots.txt`.
- See `COLLEGIUM.md / Vestibulum` for the parallel framing of this material as research-college infrastructure.

---

## Fons Primus *(Source Document, preserved verbatim)*

The original AmazonQ output is appended below in full. Editorial scaffolding lives above this line; the source itself is preserved without alteration so future editors can re-interpret it.

> *[Append the raw AmazonQ document here, beginning with "is there a way to allow ai/robots to visit some sites?" and continuing through the closing AmazonQ disclaimer. For length, omitted from this scaffold; paste in when filing.]*

---

*Fin. § I*
