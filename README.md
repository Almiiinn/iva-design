# IVA design – Shopify-tema

Skräddarsytt Shopify-tema byggt från grunden för [ivadesign.se](https://ivadesign.se) – en svensk webbutik med silikonskal till iPhone med MagSafe eller inbyggd hållare för AirPods, läppglans och parfym.

Live sedan september 2026.

![IVA design – startsida](screenshot.png)

## Om projektet

Temat är inte baserat på Dawn eller något annat färdigt tema – varje sektion, mall och snippet är handskriven i Liquid, HTML, CSS och vanilla JavaScript. Designen bygger på en creme/svart palett med Cormorant Garamond för rubriker och Jost för brödtext.

Utöver koden omfattade projektet hela uppsättningen av butiken: domän och DNS, e-post via Google Workspace (MX/SPF/DKIM), Shopify Payments, moms, frakt med PostNord via Packrooster, etikettskrivare, returflöde med QR-kod, anpassade kundmejl, GDPR, SEO och Google Search Console.

## Funktioner

**Butik**
- Startsida med full-bleed hero (separat mobil-layout), produktöversikt, jämförelse och kundgalleri
- Kollektionssida med modellfilter, hover-bild, favoritknapp och flytande notis
- Produktsida med galleri, färg-swatches, modellväljare, USP-pills och bevakning vid slut i lager (Notify Me!)
- Varukorgslåda (AJAX) och varukorgssida med frakt- och momsberäkning
- Favoriter sparade i `localStorage` med räknare i header och footer
- Sökning, 404, presentkort

**Kund**
- Kundkonto (`/pages/mitt-konto`) med orderhistorik, adresser och "Begär retur" som förifyller ordernumret på retursidan
- Retursida med QR-flöde via PostNord (ingen skrivare krävs för kunden)
- Hjälpcenter/FAQ, Om oss, Kontakt, Allmänna villkor, Personuppgiftspolicy, Spara order

**Teknik**
- Online Store 2.0 med JSON-mallar och sektioner med `{% schema %}`-inställningar, så att ägaren kan redigera texter i temaredigeraren utan kod
- Svensk lokalisering (`locales/sv.json`)
- Anpassad kassa (färger, typsnitt, "Varav moms (25 %)")
- Anpassade mejlmallar för order- och leveransbekräftelse
- Inga externa JS-bibliotek – all interaktivitet i ren JavaScript


## Stack

Shopify (Online Store 2.0) · Liquid · HTML/CSS · JavaScript · Shopify Checkout · Shopify Payments · Packrooster + PostNord · Google Workspace · Pandectes GDPR · Notify Me! · Google Search Console

## Kör lokalt

```bash
npm install -g @shopify/cli
shopify theme dev --store <din-butik>.myshopify.com
```

## Licens

Koden är publicerad som portfolio. Varumärket IVA design, bilder och texter tillhör 2M Interlokal AB.
