# Drielanden-marktplaats

Zoek tweedehands spullen rond Mheer (Zuid-Limburg) in drie landen tegelijk: Nederland, België en Duitsland.

**Direct gebruiken:** https://bartbellefroid.github.io/drielanden-marktplaats/

Je typt één keer in het Nederlands wat je zoekt. De zoekterm wordt vertaald naar het Duits en het Frans (voor Wallonië). Daarna krijg je per site een zoeklink met postcode en straal.

## Sites

| Land | Site | Taal | Middelpunt (standaard) |
|---|---|---|---|
| NL | [Marktplaats](https://www.marktplaats.nl) | NL | 6261 Mheer |
| BE | [2dehands.be](https://www.2dehands.be) | NL | 3790 Voeren |
| BE | [2ememain.be](https://www.2ememain.be) | FR | 3790 Voeren |
| DE | [Kleinanzeigen.de](https://www.kleinanzeigen.de) | DE | 52074 Aachen |
| DE | [eBay.de](https://www.ebay.de) | DE | 52074 Aachen |
| DE | [markt.de](https://www.markt.de) | DE | geen (heel Duitsland) |
| DE | [Quoka](https://www.quoka.de) | DE | geen (zoekt via Google) |
| Alle | [Facebook Marketplace](https://www.facebook.com/marketplace) | NL/DE/FR | Maastricht |

De middelpunten zijn aan te passen onder **Instellingen** op de pagina.

## Gebruik

Open de [online versie](https://bartbellefroid.github.io/drielanden-marktplaats/), of open `index.html` lokaal in een browser. Er is geen build-stap nodig en er zijn geen afhankelijkheden.

De online versie draait op GitHub Pages (Settings → Pages → Deploy from a branch). Na een push duurt het meestal een paar minuten voordat de wijziging online staat.

## Vertalen

De pagina probeert een zoekterm in deze volgorde te vertalen:

1. **Ingebouwde woordenlijst** (`DICT` en `ALIAS` in `index.html`): ongeveer 120 veelgezochte artikelen, met de woorden die verkopers in advertenties gebruiken (bijv. bosmaaier → *Freischneider, Motorsense* / *débroussailleuse*). Andere schrijfwijzen zoals "robot grasmaaier" verwijzen naar hetzelfde woord.
2. **Claude**, alleen als de pagina als Claude-artifact geopend wordt.
3. **[MyMemory](https://mymemory.translated.net/)**, een gratis vertaaldienst zonder account. Alleen de zoekterm wordt daarheen gestuurd. Dit is een letterlijke vertaling, dus controleer hem.
4. Lukt niets, dan vul je Duits en Frans zelf in. Er staat een Google Translate-link bij.

Onder de zoekbalk staat altijd waar de vertaling vandaan komt. Termen zijn altijd aan te passen. Meerdere termen met komma's ertussen geven elk een eigen zoeklink.

## Bekende beperkingen

- **De zoek-URL's zijn nog niet getest.** Ze zijn gebaseerd op de bekende URL-opbouw van de sites, niet op officiële documentatie. Het minst zeker zijn het postcodeformaat bij Kleinanzeigen (`/s-<PLZ>/<term>/k0r<km>`) en de eBay-parameters `_stpos` en `_sadis`. Naast elke link staat een "via Google"-knop als reserve.
- **markt.de en Quoka** filteren nog niet op straal. markt.de krijgt een zoeklink met alleen de zoekterm (`/suche/<term>/`). Voor Quoka is de directe zoeklink nog onbekend, dus die zoekt via Google op quoka.de. Bij beide staat een knop "site openen" om zelf met straal te zoeken.
- Buitenlandse sites meten de straal vanaf een postcode in hun eigen land, niet vanaf Mheer.
- De pagina haalt zelf geen advertenties op. Ze opent de zoekresultaten op de sites zelf, omdat scrapen meestal niet is toegestaan in de gebruiksvoorwaarden.

## Ideeën voor later

- Meer sites, zoals Vinted.
- De woordenlijst uitbreiden met woorden die Yves vaak zoekt.
- Straal en postcode in de links van markt.de en Quoka, zodra de URL-opbouw bekend is.
- Tweedehands auto's uit BE/DE met een schatting van de importkosten (BPM, RDW-keuring, transport).
