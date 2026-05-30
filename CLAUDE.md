# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Het spel starten

Geen build-stap of server nodig – open het HTML-bestand direct in de browser:

```bash
open index.html        # Nederlandstalige versie
open index-En.html     # Engelstalige versie
```

## Architectuur

Het project bestaat uit twee zelfstandige, monolithische HTML-bestanden. CSS, JavaScript en HTML-structuur staan volledig in elk bestand – er zijn geen gedeelde externe bestanden (op de SVG na).

### Bestanden

| Bestand | Doel |
|---|---|
| `index.html` | Nederlandstalige versie van het spel |
| `index-En.html` | Engelstalige versie (zelfde structuur, vertaalde teksten) |
| `romeins legionair.svg` | SVG-afbeelding van de soldaat, gedeeld door beide versies |

### Speellogica

Het spel heeft drie schermen die via CSS-klassen worden omgeschakeld:
- **Startscherm** (`#start-overlay`, klasse `hidden` verbergt het) – uitleg + uitrustingsoverzicht
- **Spelscherm** – 3-koloms layout: items-paneel links, soldaat midden, scorebord rechts
- **Victory-modal** (`#modal`, klasse `open` toont het) – score opslaan na voltooiing

**Drop zones** zijn absolute-gepositioneerde cirkels over de SVG heen, geplaatst via `style="top:X%;left:Y%"` op basis van de SVG-verhoudingen (`aspect-ratio: 1920 / 2426`). De coördinaten zijn handmatig afgestemd op de soldaatafbeelding.

**Koppeling item → zone** werkt via `data-item` (unieke itemsleutel) en `data-zone` (correcte doelzone) op elke `.item-card`. De `handleDrop`-functie vergelijkt `correctZone === targetZone`.

**Touch-ondersteuning** gebruikt een aangepaste ghost-element die bij `touchmove` wordt verplaatst; `elementFromPoint` detecteert de drop zone bij `touchend`.

**Scorebord** slaat scores op in `localStorage` onder de sleutel `legionair_scores` (maximaal 10 entries, gesorteerd op tijd in seconden).

### Taalversies synchroniseren

Bij wijzigingen aan spellogica of lay-out moeten beide bestanden handmatig gesynchroniseerd worden – de logica is identiek, alleen de teksten verschillen. Pas altijd beide aan.
