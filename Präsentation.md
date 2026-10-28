---
marp: true
paginate: true
style: |
  /* ==============================================================
     Vorlage für Marp
     Diese Datei ist dein Gerüst. Ändere Werte, niemals die Namen
     der Klassen – die müssen zum Text passen, sonst passiert nichts.

     Wichtig: Diese Vorlage nutzt HTML (<div class="...">). Marp
     blockiert das standardmäßig. Aktiviere HTML:
       - VS Code: Einstellung "markdown.marp.enableHtml"
       - Marp CLI: Option --html
     ============================================================== */

  /* --- Die Farben ------------------------------------------------
     Jede Farbe steht genau einmal hier. Alle Klassen weiter unten
     benutzen nur noch den Namen. Willst du das Aussehen ändern,
     änderst du nur diese sieben Zeilen – nicht die Klassen. */

  :root {
    --blau:      #17324d;   /* Titel, Balken, Linien */
    --blau-hell: #24527a;   /* Akzente, Rand der Karten */
    --flaeche:   #f7f9fc;   /* Hintergründe von Kästen */
    --flaeche-2: #edf5fb;   /* zweiter Hintergrundton */
    --flaeche-3: #e8f1f8;   /* dritter Hintergrundton */
    --flaeche-4: #eef5f9;   /* Karten */
    --gelb:      #f4d35e;   /* Hervorhebung */
  }

  /* --- Die Folie selbst ------------------------------------------
     Jede Folie wird zu einem <section>. Alles hier gilt für alle. */
  section {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100%;
    padding: 40px;
    font-family: Arial, Helvetica, sans-serif;
  }

  /* --- Der Folientitel ------------------------------------------- */
  .titel {
    width: 100%;
    text-align: center;
    color: var(--blau);
    margin-bottom: 24px;
  }

  /* --- Eine einfache Liste --------------------------------------- */
  .liste {
    width: 80%;
    padding: 18px 24px;
    background: var(--flaeche);
    border-left: 6px solid var(--blau);
    text-align: left;
  }

  /* --- Ein hervorgehobener Satz ---------------------------------- */
  .merksatz {
    width: 80%;
    margin-bottom: 20px;
    padding: 20px;
    background: var(--gelb);
    font-weight: bold;
    border-radius: 20px;
    text-align: left;
  }

  /* --- Ein einzelner Kasten -------------------------------------- */
  .box {
    width: 80%;
    padding: 18px 24px;
    background: var(--flaeche-2);
    border-left: 6px solid var(--blau);
    text-align: left;
  }

  /* --- Zwei Spalten: legt die Aufteilung fest -------------------- */
  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    width: 100%;
  }

  /* Spaltenverhältnisse zum Ausprobieren:
       1fr 1fr  -> zwei gleich breite Spalten
       2fr 1fr  -> links doppelt so breit wie rechts
       1fr 2fr  -> rechts doppelt so breit wie links               */

  /* Eine breite und eine schmale Spalte:
     .grid-2 { grid-template-columns: 2fr 1fr; align-items: center; } */

  /* --- Die Spalte: nur das Aussehen ------------------------------ */
  .spalte {
    padding: 18px;
    background: var(--flaeche-3);
    border-radius: 14px;
    text-align: left;
  }

  /* --- Karten: drei Dinge nebeneinander -------------------------- */
  .karten {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
    width: 100%;
  }

  .karte {
    min-height: 150px;
    padding: 16px;
    background: var(--flaeche-4);
    border-top: 5px solid var(--blau-hell);
    text-align: left;
  }

  /* --- Bilder ---------------------------------------------------- */
  .bild {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

  .bild img {
    width: 320px;
    height: auto;
  }

  /* --- Die Fußzeile ---------------------------------------------- */
  .fusszeile {
    width: 100%;
    margin-top: auto;
    padding-top: 12px;
    border-top: 1px solid var(--blau);
    text-align: center;
    font-size: 0.6em;
  }
---

<div class="titel">

# Meine Auseinandersetzung mit Messengern

</div>

<div class="liste">

- Heutige Bedeutung: Messenger bestimmen unsere Erreichbarkeit in Echtzeit beschützen sie aber auch unsere Privatsphäre?
- Leitfrage: Welcher Messenger passt zu meinen persönlichen Ansprüchen?
- Ziel: Demonstration das man einen Kompromiss aus Sicherheit und Erreichbarkeit eingehen muss
- Ward
- 9B
- 28.10.2026

</div>

<div class="fusszeile">
  Meine Auseinandersetzung mit Messengern · Ward, 9B
</div>

---

<div class="titel">

# Messenger im Alltag:Hohe Nutzung trifft auf Zielkonflikte

</div>

<div class="liste">

- Alltagsrelevanz: wichtige Rolle für private und schulische Kommunikation
- Dilemma: Konflikt zwischen Reichweite, Datenschutz und Kosten
- Ziel:Alltagstauglichkeit vs Datenschutz und Kosten

</div>

<div class="fusszeile">
  Einleitung · Ward, 9B
</div>

---

<div class="titel">

# Drei Dienste im Überblick

</div>

<div class="karten">
  <div class="karte">

  **WhatsApp**

  - Kostenmodell: kostenlos
  - Datenschutz: eingeschränkt
  - Erreichbarkeit im Bekanntenkreis: sehr hoch 

  </div>
  <div class="karte">

  **Signal**

  - Kostenmodell: kostenlos
  - Datenschutz: hoch
  - Erreichbarkeit im Bekanntenkreis: sehr gering (0)

  </div>
  <div class="karte">

  **Threema**

  - Kostenmodell: einmaliger Kauf (6-7 USD)
  - Datenschutz: sehr hoch
  - Erreichbarkeit im Bekanntenkreis: sehr gering (0)

  </div>
</div>

<div class="fusszeile">
  Überblick der Dienste · Ward, 9B
</div>

---
<div class="titel">

# Kostenmodell und Quellcode getrennt betrachten

</div>

<div class="grid-2">
  <div class="spalte">

  **Kostenmodell**

  - kostenpflichtig oder kostenlos?
  - kostenlose Grundfunktionen, Zusatzangebote?

  </div>
  <div class="spalte">

  **Quellcode**

  - öffentlich zugänglich?
  - Lizenz und Beleg prüfen

  </div>
</div>

<div class="fusszeile">
  Überblick · Name, Klasse
</div>

---
<div class="titel">

# Eine breite und eine schmale Spalte

</div>

<div class="grid-2" style="grid-template-columns: 2fr 1fr; align-items: center;">
  <div class="spalte">

  - Erklärung, Aufzählung oder Fließtext
  - Der Text bekommt zwei Teile der Breite

  </div>
  <div class="spalte">

  **Kurzfassung**

  - Ein Satz

  </div>
</div>

<div class="fusszeile">
  Detail und Überblick · Ward, 9B
</div>

---
<div class="titel">

# Merksatz oder Kasten

</div>

<div class="merksatz">
  Ein Satz, den das Publikum behalten soll.
</div>

<div class="box">

- Ein Punkt
- Ein weiterer Punkt

</div>

<div class="fusszeile">
  Merksatz · Name, Klasse
</div>

---

<div class="titel">

# Bild mit Beschreibung

</div>

<div class="bild">

![Kurze Beschreibung des Bildes](bilder/beispiel.png)

</div>

<div class="fusszeile">
  Bild · Name, Klasse
</div>

---

<div class="titel">

# Quellen

</div>

<div class="liste">

- [Titel der Quelle](https://beispiel.de), abgerufen am TT.MM.JJ
- [Titel der zweiten Quelle](https://beispiel.de), vom TT.MM.JJ

</div>

<div class="fusszeile">
  Quellen · Name, Klasse
</div>
