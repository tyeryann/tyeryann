# GitHub Profile README - Pipeline Section Refresh (2026-10-15)

Copy-paste replacement for the "What I'm building" section at github.com/tyeryann,
plus the portfolio link fix. Hyphens only, no em-dashes.

---

## 1. Portfolio link fix (line 15)

Replace:
```
📫 [LinkedIn](...) · [Portfolio](https://tye-johnson.carrd.co)
```
With:
```
📫 [LinkedIn](...) · [Portfolio](https://www.tyejohnson.dev/)
```

---

## 2. "What I'm building" section - full replacement

```markdown
### 🛠️ What I'm building

**Rejection Quest HQ** - a Lovable command center wired to two n8n webhooks: one that
scores and triages inbound listings on a 0-100 match scale, one that generates tailored
documents on approval. The app is the source of truth - a Google Sheet keeps an
append-only audit log, written only by the webhooks below. Listings land as Pending by
default; archive and portal auto-detection are built in.

**The Assistant** (n8n webhook) - takes any listing URL, extracts the full posting
content (even from JavaScript-heavy pages), and scores it across six weighted categories
with hard gates on salary floor and location. Unreadable input scores a 0, never a
hallucination.

[Image: Rejection Quest Assistant workflow]

**The Tailor** (n8n webhook) - on approval only, generates tailored documents from a
source profile under a strict fact-lock: rephrase what's true, never invent. Finished
docs land as editable Google Docs; links go back to the log.

[Image: Rejection Quest Tailor workflow]

**Human-in-the-loop, always** - nothing is generated or sent without explicit approval.
The machines do the paperwork; I make the decisions.
```

---

## 3. Screenshot swap

The old section embeds three workflow canvas images (Gatekeeper, Tailor, Green Light).
Replace with the two new canvases:

- `docs/rejection-quest-assistant.png` (currently in the private turbo-umbrella repo)
- `docs/rejection-quest-tailor.png` (same)

Upload both to the tyeryann/tyeryann profile repo (e.g. an `images/` folder) and point
the markdown image links at them. The Green Light image gets dropped entirely -
that workflow is retired.

---

## What changed and why

- Old story: three n8n workflows (Gatekeeper scorer, Tailor, Green Light orchestrator)
  plus spreadsheet orchestration.
- New story: Lovable app (Rejection Quest HQ) as the command center, two n8n webhooks
  (Assistant = score-from-URL, Tailor = generate-docs-on-approval), Google Sheet as
  append-only audit log. Green Light retired Oct 2026.
- Thesis line kept ("The machines do the paperwork; I make the decisions") - it's the
  through-line of the whole project.
