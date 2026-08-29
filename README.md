# recallr-webapp

**Recallr AI** as a developer product — the memory layer you drop into a conversational
AI agent so it stops forgetting.

**Live → [recallr-v1-exp.vercel.app](https://recallr-v1-exp.vercel.app)**

## Brief

Conversational agents lose everything between sessions, and the usual fix — stuff the
transcript into the context window — degrades as the history grows and has no way to
resolve a fact that changed. Recallr's pitch here is persistent memory with **temporal
reasoning** and **conflict resolution**: it knows not just what was said but when, and
what supersedes what.

The page is built around a single hard number — **97.5% on LongMemEval** — and around
the two-line integration. Everything else on the page exists to support one of those
two claims:

| Section | Claim it carries |
|---|---|
| `#hero` | "Your AI finally remembers." |
| `#benchmark` | 97.5% accuracy, best in class |
| `#modes` | Fast when you need it, deep when it matters — the two retrieval loops |
| `#architecture` | Two loops, infinite memory |
| `#integration` | Two lines of code, permanent memory |
| `#pricing` | — |

This is the **earlier positioning**, aimed at developers building agents. The company
later repositioned toward private capital — see
[`recallr-site`](https://github.com/dxny-aep/recallr-site) for that. Both are kept
because the developer framing is sharper and the benchmark section is reusable.

> Naming note: this is a marketing page for the product, not the product's application
> UI. Named `recallr-webapp` to distinguish it from the private-capital site.

## Running

Static HTML, one file, no build step.

```bash
python3 -m http.server 8000
```

```
index.html    the whole page — ~1,760 lines, inline SVG icon sprite
fonts/        Articulat CF
```

## Design language

Follows the Recallr brand guide, which lives in
[`recallr-site/DESIGN-GUIDE.md`](https://github.com/dxny-aep/recallr-site/blob/main/DESIGN-GUIDE.md):
Manrope + DM Mono, radius 0, hairline strokes, ~80% monochrome with one sky-blue accent
moment per surface.

## Note

`fonts/` contains **Articulat CF**, a commercially licensed typeface. Do not
redistribute this repository publicly or ship those files outside the site's own licence.

Vercel link files were stripped during consolidation — deploying from here needs a
fresh `vercel link`. The existing deployment is unaffected.
