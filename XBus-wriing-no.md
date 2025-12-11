# XBus CAT6 Kobleveiledning

## Par-tabell

| Par  | Farger                     | Funksjon        | Tilordning                    |
|------|-----------------------------|-----------------|-------------------------------|
| Par 2 | Hvit/Oransje + Oransje     | XBus-signaler   | A = Hvit/Oransje<br>B = Oransje |
| Par 1 | Hvit/Blå + Blå             | Strømfeed 1     | +V = Blå<br>0V = Hvit/Blå       |
| Par 3 | Hvit/Grønn + Grønn         | Strømfeed 2     | +V = Grønn<br>0V = Hvit/Grønn   |
| Par 4 | Hvit/Brun + Brun           | Reserve         | Ubrukt / Valgfri referanse     |

---

## Merknader
- Hold A og B sammen på kun par 2.  
- Bruk par 1 og par 3 i parallell for å redusere spenningsfall.  
- Alle paneler skal følge farge-til-farge kontinuitet.  
- Ikke koble skjermen noe sted unntatt ved LZV200-enden.  
- Par 4 brukes ikke med mindre det er et bevisst behov.

---

## 2. Daisy-chain installasjon
- Bruk én sammenhengende CAT6-kabel som XBus-stamme.  
- Alle paneler kobles i serie (ingen stjernekonfigurasjon).  
- Før alle par rett gjennom hvert panel med farge-til-farge.  
- Hold avgreninger (stubs) så korte som mulig.

---

### 2.1 Terminering
- **Basestasjon (LZV200):** Bruk innebygd terminering.  
- **Fjerneste ende:** Monter en **100 Ω** motstand mellom A (Hvit/Oransje) og B (Oransje).

---

### 2.2 Skjerming
- Skjermen på CAT6-kabelen skal gå **uavbrutt gjennom alle paneler**.  
- Skjermen skal **ikke kobles til noe** i mellomliggende paneler eller i enden.  
- Skjermen kobles **kun til jord** ved LZV200-enden.

---

### 2.3 Strømfordeling
- Bruk **par 1 og par 3 i parallell** for strømforsyning.  
- Koble sammen +V-lederne i hvert panel, og gjør det samme for 0V.  
- Matepanelene tar strøm fra disse sammenkoblede punktene for å redusere spenningsfall.

