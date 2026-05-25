# Kleed de Legionair! – Museum Educatief Spel

Een interactief drag-and-drop spel over de uitrusting van een Romeinse legionair, ontwikkeld voor gebruik in een museumomgeving.

---

## Doel van het spel

Spelers leren de zes belangrijkste uitrustingsstukken van een Romeinse legionair kennen – inclusief hun Latijnse namen – door ze naar de juiste plek op de soldaat te slepen. Het spel combineert historische educatie met spelplezier en een licht competitief scorebord.

---

## Doelgroep

Jeugd van **10 tot 15 jaar**, geschikt voor gebruik op een touchscreen of desktop in een museumopstelling.

---

## Uitrusting

| Latijnse naam     | Nederlands        | Positie op soldaat |
|-------------------|-------------------|--------------------|
| Galea             | Helm              | Hoofd              |
| Lorica Segmentata | Borstpantser      | Romp               |
| Scutum            | Schild            | Linkerarm          |
| Pilum             | Werpspeer         | Rechterhand        |
| Gladius           | Zwaard            | Heup               |
| Caligae           | Sandalen          | Voeten             |

---

## Hoe werkt het spel?

1. Het spel opent met een **startscherm** met uitleg en een overzicht van de zes uitrustingsstukken (met Latijnse én Nederlandse namen).
2. De speler sleept elk uitrustingsstuk naar de juiste dropzone op de afbeelding van de legionair.
3. **Groen** = correct geplaatst, **rood** = verkeerde plek.
4. Na afloop verschijnt de score. De speler kan zijn naam invullen in het scorebord.
5. Via het scorebord kunnen meerdere spelers hun resultaten vergelijken.

De hints bij elk voorwerp beschrijven het materiaal en de historische functie – zonder de plaatsingslocatie weg te geven – zodat het spel een echte uitdaging blijft.

---

## Technische opbouw

- **Pure HTML, CSS en JavaScript** – geen frameworks of externe afhankelijkheden
- **SVG-afbeelding** van een Romeinse legionair (`romeins legionair.svg`) als interactief speelveld
- **Drag-and-drop** via de HTML5 Drag and Drop API
- **Volledig schermvullende 3-koloms layout** zonder scrollen, geoptimaliseerd voor museumschermen
- Animaties op dropzones (pulserende cirkels, kleurfeedback bij correct/fout)
- Responsief scorebord met invoerveld voor naam

---

## Beschikbare talen

| Bestand         | Taal       |
|-----------------|------------|
| `index.html`    | Nederlands |
| `index-En.html` | Engels     |

---

## Projectbestanden

```
museum-spellen-legionair/
├── index.html           # Nederlandstalige versie
├── index-En.html        # Engelstalige versie
├── romeins legionair.svg # SVG-afbeelding van de soldaat
└── README.md
```

---

## Lokaal starten

Het spel werkt als een gewoon HTML-bestand en vereist geen server of installatie:

```bash
# Open direct in de browser
open index.html
```

Of sleep `index.html` naar een browservenster.

---

## Achtergrond

Dit spel maakt deel uit van een reeks educatieve museumspellen voor de jeugd. Het combineert historische kennis over het Romeinse leger met een toegankelijke, visuele spelvorm die past bij een museumopstelling.
