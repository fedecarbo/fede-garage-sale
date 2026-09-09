# The move — London to Escazú

Status of the household move, kept so a new session can pick it up without being
told the story again. **Last updated 9 September 2026.**

No addresses, phone numbers, email addresses or document numbers live in this
file: the repository is public. Names are first names, companies are companies.

## Where it stands

Two pallets of household goods travel from London to San Rafael de Escazú, Costa
Rica. The quote is approved and a collection date is tentatively booked. What is
left is a handful of answers, three measurements and the documents.

| | |
|---|---|
| Movers | Allianz Moving CRC, arranged through Dinia at ASEAL Costa Rica |
| Quote | **DE-26-022-2**, 3 September 2026, door to door, consolidated |
| Price | **2.5 m³ — US$5,495 · 5 m³ — US$5,595**, so extra volume runs about **$40/m³** |
| Booked | The **two-pallet** quote, approved by Dinia with the shipping line on 9 September |
| Collection | **7 October 2026, tentative** — movable at no cost; the date only reserves space before high season |
| Transit | 35–45 days, plus about 2 weeks nationalisation in Costa Rica |
| Delivery | Roughly **25 November – 5 December**, counting from 7 October |
| Extras in CR | ~$2,100: tax $800, bonded warehouse $500, inspections and permits $250, electronic seal $100 (random), shipping-line THC $450. Two further $550 lines exist in the quote whose labels could not be read from the PDF |
| Insurance | Optional, **3.5% of declared value** — not yet answered |
| Validity | The written quote carried 30 days, so it lapsed 3 October on paper; the 7 October date was agreed after that, verbally |

## Decisions already taken

- **Two pallets, not one.** At $40 a cubic metre beyond the first 2.5 m³, volume is
  cheap and the service is what costs.
- **No exoneración.** Dinia's advice, from the shipping company: the exemption
  takes longer, and the tax saved is spent on bonded-warehouse storage while it
  processes. This runs against the *Certificado de Residencia en el Exterior*
  process opened with the Costa Rican consulate on 8 September — that consular
  route existed to obtain exactly this exemption.
- **The movers pack everything**, materials included, and **they write the packing
  list.** The list in this repository is for planning and for pricing, not the
  customs document.
- **Nothing with refrigerant gas** — no fridges, no air conditioners. Nothing on
  the list has any.
- **A second virtual survey before collection is optional.** Offered, not booked.

## Open, and on Fede

1. **Insurance** — yes or no, and the declared value if yes.
2. **Passport copy** to Dinia.
3. **Tenancy agreement** to Dinia, as proof of time lived in the UK. The consulate
   asked for a contract too.
4. **Three measurements**: one transparent Iris box, one black box, and the bike
   (which depends on whether it travels boxed).
5. **Zudik** — the Joseph Joseph laundry basket was reserved for them and is now
   on the shipping list. It has been removed from the sale; the reservation only
   exists in that conversation.
6. **Whether to take the second virtual survey.**

## The shipping list

Lives in two places, both generated from a `SHIP` constant that is **duplicated in
each file and must be edited in both**:

- `index.html` — the last slide of the public deck, reached from the "Shipping"
  pill on the Everything slide, or with End.
- `desk-202c4b072d9f.html` — the Shipping screen in the private listing desk,
  from the queue hero or the `#shipping` hash. Rows there link back to their lot.

Both carry the same two exports: **Copy for Dinia** (Spanish plain text, ready to
paste into an email) and **CSV** (with a volume column, for the article-by-article
file the insurance value comes from).

**24 items, ≈1.80 m³ of the 5 m³ quoted, 263.8 kg**, with three lots still to
measure and left out of the cube rather than guessed at.

Sizes are recorded **as each lot travels**, not as it stands in the flat — the
metal desk and the ceramic table in pieces, the bench with its weights inside,
the boxes closed. Two lots are longer than a 120 cm pallet edge: the 150 cm
desktop and a boxed bike at about 140 cm.

Nothing under "not counted yet" is in that figure — clothes, bedding,
kitchenware, books, suitcases, the Nespresso machine. That is the number most
likely to move the price, since the tariff is *sujeta a volumen*.

In the Spanish export the metal desk is called **"mueble de casa"**, not
*escritorio*, for how it is classified on arrival.

## The sale

`index.html` is the public sale deck; **17 lots** remain. Lots that moved to the
shipping list were removed from it, which is why the count keeps falling: TM6,
Technogym bench, MAGNUS desk, Vesper coffee table, pocket ironing board,
simplehuman bin, Tota laundry basket, EZ curl bar, Balolo stand, Herman Miller
Aeron, Ellipse ceramic table.

Neither shipping nor selling, currently in limbo: **Thermomix TM7, Sonos Arc,
EIZO ColorEdge CS2740, Alienware AW2721D**. All four are marked "unavailable" in
the sale and were dropped from the shipping list. The two monitors have a real
obstacle — Dinia warned in May that used screens need Costa Rican permits that
are hard to get.

## Repository gotchas

- `index.html` is **generated by `build.mjs` from the listing desk**, which lives
  outside this repository. Every commit named "Publish …" is such a regeneration.
  **A republish overwrites the file**, taking the shipping slide and the lot
  removals with it. Those changes exist only in the published HTML, not in the
  generator.
- The desk's lot data sits in an **encrypted vault** (PBKDF2 + AES-GCM, password
  known only to Fede). The shipping sizes were deliberately kept in the file
  rather than read from the vault, so the screen still works for lots that have
  left the sale — which most of them have.
- The deck and the desk each hold their own copy of the shipping data. Change one,
  change the other, or they drift.
- GitHub Pages publishes `main`. The sandbox this was built in cannot reach
  `fedecarbo.github.io` — egress policy — so deployments were verified through the
  Actions run and the file's blob hash instead.

## How the numbers were arrived at

- Lot dimensions and weights come from the sale catalogue in `index.html`, which
  is Fede's own record.
- The IKEA KUGGIS boxes (54 × 37 × 21 cm) and Iris Ohyama TB-30 boxes (30 L) were
  identified from Amazon and IKEA order confirmations in Gmail.
- Sonos One at 16.1 × 12 × 12 cm and 1.85 kg, and the Boardman HYB 8.8 at 10.4 kg,
  are manufacturer figures found on the web, marked as such on the list — there
  are no receipts for either.
- The black storage boxes appear in no receipt at all; they were bought in a shop.
- The bike is insured with Laka; its model, frame size and insured value are on
  the policy in their app, not in any email.
