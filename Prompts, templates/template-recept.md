---
meta:
  type: recept-template
  doel: "Recepten genereren én aanpassen in Markdown, strikt volgens de regels."

proces:
  stappen:
    - "Stap 1: Lees en interpreteer de YAML volledig als set van verplichte regels."
    - "Stap 2: Voer de gevraagde wijziging uit (nieuw recept of aanpassing)."
    - "Stap 3: Controleer alleen het gewijzigde deel strikt tegen de regels en corrigeer dat. Ongewijzigde tekst blijft exact gelijk."
  regels_toepassing: "altijd en strikt"

regels:
  - "Alle hoeveelheden uitsluitend in grammen."
  - "Secties moeten exact overeenkomen met de lijst onder 'hoofdstukken'."
  - "Als informatie ontbreekt: gebruik {invullen}."
  - "Ingrediënten sorteren per groep (bodem, vulling, topping, etc.)."
  - "Consistentie afdwingen tussen secties (bijv. totaalgewicht ↔ ingrediëntenlijst)."
  - "Tabellen in standaard Markdown-formaat."
  - "Geen dubbele of overbodige lijsten."
  - "Bij wijzigingen: alleen het relevante hoofdstuk controleren en corrigeren, rest blijft ongewijzigd."

inhoud:
  - Titel: "{titel van het recept}"
  - Beschrijving: "{korte beschrijving eindresultaat, incl. gewicht en aantal personen}"
  - Ingrediënten:
      - "{hoofdingrediënt en hoeveelheden in grammen}"
      - "{extra ingrediënten in logische groepen}"
  - Benodigdheden: "{lijst benodigdheden en mogelijke alternatieven}"
  - Bereiding: "{stap-voor-stap instructies in logische volgorde}"
  - Opmerkingen: "{extra tips, consistenties, waarschuwingen}"
  - Varianten: "{mogelijke varianten en aanpassingen}"
---

# Algemene template-instructies
template_instructies:
  - alle placeholders {…} worden door mij ingevuld of geüpdatet op basis van jouw vraag of voorbeeld
  - volgorde van ingredienten en stappen blijft synchroon
  - hoeveelheden ingredienten altijd consistent met eindgewicht
  - vaktermen en jargon worden waar nodig toegevoegd en uitgelegd
  - markdown formatting (lijsten, tabellen, koppen) wordt consistent gehouden
  - YAML kan aangepast worden, ik pas invullingen en updates direct aan

hoofdstukken:
  inleiding:
    - inleiding volgt op de {titel}
    - korte beschrijving van het eindresultaat
    - hoeveelheid van eindresultaat aangeven:
        a: gewicht (grammen)
        b: aantal personen
        c: bakvorm(en) (en maten in cm)
        d: lagen en hoogte van lagen afgerond op halve cm
        e: totale hoogte afgerond op halve cm
    - extra context: smaakprofiel, gebruiksmoment, moeilijkheidsgraad
  ingredienten:
    - groeperen volgens de volgorde van gebruik in de bereiding
    - volgorde binnen een groep = volgorde van gebruik
    - hoeveelheden altijd in grammen
    - praktische hoeveelheden tussen haakjes (bijv. "1 M-ei", "1 zakje gist")
    - optionele ingredienten duidelijk markeren
    - som van alle ingredienten = eindgewicht
  bereiden:
    - genummerde stappen in sync met ingredientengroepen
    - concreet en meetbaar
    - korte tips om fouten te voorkomen
    - expliciete toetsen toevoegen waar nodig (proeven, ruiken, zien, horen)
    - benoem positieve indicatoren en veelgemaakte fouten
    - vermeld specifieke consistentie (bijv. half-opgesteven)
  visueel_overzicht:
    - tabel: Stap | Positief teken | Veelgemaakte fout | Extra tip
    - overzicht per stap, visueel of sensorisch
  bakken_koelen_overige:
    - tijd, temperatuur, consistentie duidelijk vermelden
    - benoem speciale tussenstaten (half-opgesteven, lobbig, zacht, etc.)
  tips:
    - praktische tips voor ingrediënten, timing, vouwtechnieken, bewaring
    - speciale tips voor veelvoorkomende valkuilen
  als_het_is_misgegaan:
    - tabel: Probleem | Herkenning | Redding | Herbestemming
    - beschrijf veelgemaakte fouten, oorzaken, oplossingen
  bewaren:
    - bewaarmethode, temperatuur, luchtvochtigheid, licht/donker, luchtdicht
    - tijdsduur per methode
    - instructies hoe het product gebruiksklaar te maken na opslag
  later_verwerken:
    - instructies voor verwerking uit koelkast of vriezer
  terminologie:
    - elke vakterm of bakkersjargon wordt beschreven
    - concreet en waar mogelijk meetbaar/toetsbaar

markdown:
  - '#' voor koppen, '-' voor lijsten
  - tabelcellen uitlijnen voor nette scheiding
  - lege regels tussen paragrafen en na koppen
  - lijsten niet voorafgegaan door lege regel tenzij na kop
  - geen enkele regel eindigt met een spatie of tab

consistentie:
  - volgorde ingredienten == volgorde stappen
  - hoeveelheden ingredienten == eindgewicht
  - alle in het recept gebruikte vaktermen beschreven in 'terminologie'
  - veelgemaakte fouten, oorzaken, remedies beschreven
  - positieve indicatoren en toetsmomenten consistent

---

# {titel}

{beschrijving_eindresultaat}
- **Hoeveelheid**: {gewicht} g, {personen} personen, bakvorm: {bakvorm}, lagen: {lagen}, totale hoogte: {hoogte} cm
- **Bewaren**: {bewaarwijze}
- **Gebruik**: {gebruik}

## Ingrediënten

- {Groepsnaam 1}
  - {Ingrediënt 1} ({hoeveelheid})
  - {Ingrediënt 2} ({hoeveelheid})

- {Groepsnaam 2}
  - {Ingrediënt 3} ({hoeveelheid})
  - {Ingrediënt 4} ({hoeveelheid})

- <!-- Som van ingrediënten moet overeenkomen met eindgewicht -->

## Benodigdheden
- {Benodigdheid 1}
- {Benodigdheid 2}

## Bereiding
1. {Stap 1, concreet en meetbaar}
2. {Stap 2, concreet en meetbaar}
3. {Stap 3, enz.}
- <!-- Voeg proefmomenten, positieve indicatoren en tips toe volgens YAML -->

### Visueel overzicht
| Stap | Positief teken | Veelgemaakte fout | Extra tip |
|------|----------------|-----------------|-----------|
| {Stap 1} | {Positief teken} | {Fout} | {Tip} |
| {Stap 2} | {Positief teken} | {Fout} | {Tip} |

## Bakken / Koelen / Andere noodzakelijke stappen
- {Tijd, temperatuur, consistentie, speciale tussenstaten}

## Tips
- {Tip 1}
- {Tip 2}

## Als het is misgegaan
| Probleem | Herkenning | Redding | Herbestemming |
|----------|------------|---------|---------------|
| {Probleem 1} | {Herkenning} | {Redding} | {Herbestemming} |
| {Probleem 2} | {Herkenning} | {Redding} | {Herbestemming} |

## Bewaren
- {Bewaarmethode, temperatuur, luchtvochtigheid, licht/donker, luchtdicht}
- {Tijdsduur per methode}
- {Klaarmaken na opslag}

## Later verwerken
- {Verwerking_instructies}

## Vaktermen
- {Vakterm 1}: {Uitleg}
- {Vakterm 2}: {Uitleg}
