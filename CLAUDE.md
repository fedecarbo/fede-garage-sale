# fede-garage-sale

Fede is leaving London for San Rafael de Escazú, Costa Rica. This repository is
two things: the sale of what stays behind, and the list of what travels.

**Read [MOVE.md](MOVE.md) first.** It holds the state of the move — the quote, the
dates, what has been decided and what is still open — so it does not have to be
retold at the start of a session. Keep it current when any of that changes.

## What is here

| File | What it is |
|---|---|
| `index.html` | The public sale deck: a cover, one slide per lot, an "Everything" list, and a Shipping slide at the end. Published to GitHub Pages from `main`. |
| `desk-202c4b072d9f.html` | The private listing desk, password-locked. Marketplace forms per lot, plus a Shipping screen. Its lot data is an encrypted vault; the password is Fede's. |
| `products/<slug>/` | Photos per lot. `products/shipping/` holds drawn placeholders for things that were never lots. |

Both HTML files are standalone: no build step, no dependencies, everything inline.

## Things worth knowing before editing

- **`index.html` is generated.** A tool outside this repository (`build.mjs`, driven
  from the listing desk) regenerates it wholesale — every "Publish …" commit is one
  of those. Manual edits to it, the Shipping slide included, are overwritten by the
  next publish.
- **The shipping list is duplicated.** Both HTML files carry their own `SHIP`
  constant. Edit one and you must edit the other, or the two pages disagree.
- **The repository is public.** No addresses, phone numbers, email addresses or
  document numbers in any file. The Shipping pages carry measurements only; Fede
  signs his own emails.
- **Verify in a browser.** Both pages are plain HTML with inline script — Chromium
  and Playwright are available, and a syntax check plus a render at desktop and
  phone widths catches what reading the diff does not. The desk needs its vault to
  boot; a throwaway vault with a known password is the way to exercise it without
  touching the real one.
