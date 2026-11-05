# Drielanden-marktplaats

Zoek tweedehands spullen rond Mheer (Zuid-Limburg) in drie landen tegelijk: Nederland, België en Duitsland.

Je typt één keer in het Nederlands wat je zoekt. De zoekterm wordt vertaald naar het Duits en het Frans (voor Wallonië). Daarna krijg je per site een zoeklink met postcode en straal.

## Sites

| Land | Site | Taal | Middelpunt (standaard) |
|---|---|---|---|
| NL | [Marktplaats](https://www.marktplaats.nl) | NL | 6261 Mheer |
| BE | [2dehands.be](https://www.2dehands.be) | NL | 3790 Voeren |
| BE | [2ememain.be](https://www.2ememain.be) | FR | 3790 Voeren |
| DE | [Kleinanzeigen.de](https://www.kleinanzeigen.de) | DE | 52074 Aachen |
| DE | [eBay.de](https://www.ebay.de) | DE | 52074 Aachen |
| Alle | [Facebook Marketplace](https://www.facebook.com/marketplace) | NL/DE/FR | Maastricht |

De middelpunten zijn aan te passen onder **Instellingen** op de pagina.

## Gebruik

Open `index.html` in een browser. Er is geen build-stap nodig en er zijn geen afhankelijkheden.

Je kunt de pagina ook online zetten met GitHub Pages: Settings → Pages → Deploy from branch → `main`, map `/ (root)`.

## Vertalen

- Voor ongeveer 30 veelgezochte artikelen (tuin- en klusgereedschap, fietsen, meubels) zit er een woordenlijst in de pagina (`DICT` in `index.html`).
- Opent iemand de pagina als Claude-artifact, dan vertaalt Claude onbekende woorden automatisch. Buiten Claude (bijvoorbeeld via GitHub Pages) vul je onbekende woorden zelf in. Er staat een Google Translate-link bij.
- Termen zijn altijd aan te passen. Meerdere termen met komma's ertussen geven elk een eigen zoeklink.

## Bekende beperkingen

- **De zoek-URL's zijn nog niet getest.** Ze zijn gebaseerd op de bekende URL-opbouw van de sites, niet op officiële documentatie. Het minst zeker zijn het postcodeformaat bij Kleinanzeigen (`/s-<PLZ>/<term>/k0r<km>`) en de eBay-parameters `_stpos` en `_sadis`. Naast elke link staat een "via Google"-knop als reserve.
- Buitenlandse sites meten de straal vanaf een postcode in hun eigen land, niet vanaf Mheer.
- De pagina haalt zelf geen advertenties op. Ze opent de zoekresultaten op de sites zelf, omdat scrapen meestal niet is toegestaan in de gebruiksvoorwaarden.

## Ideeën voor later

- Meer sites: Quoka.de, markt.de, Vinted.
- Tweedehands auto's uit BE/DE met een schatting van de importkosten (BPM, RDW-keuring, transport).
