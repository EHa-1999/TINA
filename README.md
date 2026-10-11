# TINA

**Transparent INformation Access.** A demo of the search portal for citizens: what can be found once a municipality has made a document public.

TINA is part of XENA, alongside the demo of records-grade storage and MIRA (the assistant in the office suite). The storage demo ends at *Publish*; TINA shows what a citizen sees afterwards.

> A demo, not a product. The portal, the documents, the people and the numbers are invented.

Nederlandse versie: [README.nl.md](README.nl.md)

## What the demo shows

| Part | What you see |
|---|---|
| **Home** | Search box, browsing by type of information, latest publications, and an explanation of what is and is not there. |
| **Search results** | Search in title, keywords and text, with snippets, filters and terms to refine with. |
| **Document** | A preview of the text with placeholders where something was left out, the reason for it, the attributes, the seal, accessibility and a permanent link. |
| **Woo dossier** | The inventory of a request under the Dutch Open Government Act (Woo): what was made fully, partly or not public, with the reason. |
| **Behind the portal** | How storage, publishing, publication repository and portal fit together, and why the portal does not know the storage. |

The bar *Under the hood* shows what the portal requests at each step.

## Principles

- The portal reads only from a separate publication repository. There is no connection to the storage.
- What is published is a derivative: anonymised, as PDF/A-2b, with attributes rebuilt from the register, and sealed.
- What was left out is visible as a placeholder, with the ground for refusal.
- A document that is not made public still appears in the dossier inventory, with the reason.
- The portal itself can be operated with keyboard and screen reader.
- Which information the municipality publishes beyond the statutory Woo categories has not been filled in yet.

## Use

Open `index.html` in a browser. No server is needed. Languages: Dutch, German, English and French; `#de`, `#en` or `#fr` after the address selects the language for that one link.

## Build

The source is in `src/demo.html`, the translations in `i18n/<language>.json` (the key is the Dutch text).

```
python3 build.py
```

writes `index.html` and `TINA - v<N>.html`. The version number is in `VERSION`.

## Licence

EUPL-1.2, see `LICENSE`.
