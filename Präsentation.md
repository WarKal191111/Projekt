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

### 1. Kostenmodell
* **Prüffrage:** Welche Kosten entstehen?
* **WhatsApp & Signal:** Kostenlos (Meta-Daten bzw. Spenden)
* **Threema:** Einmalig kostenpflichtig (iOS/Android Store)

 </div>
  <div class="spalte">
 
### 2. Quellcode
* **Prüffrage:** Ist die Sicherheit unabhängig prüfbar?
* **WhatsApp:** Proprietär / geschlossen (Vertrauen nötig)
* **Signal & Threema:** Open Source (öffentlich geprüft)
  
  </div>
</div>

<div class="fusszeile">
  Kostenmodell und Quellcode · Ward, 9B
</div>

---
<div class="titel">

# Alltagstauglichkeit & Praxis-Check

</div>

<div class="grid-2">
  <div class="spalte">

### 1. Alltagstauglichkeit
* **Prüffrage:** Reale Erreichbarkeit im Umfeld?
* **Eigenes Umfeld:** 0 Personen nutzen Threema
* **Markt:** WhatsApp dominiert; datenschutzfreundliche Dienste bleiben Nische

 </div>
  <div class="spalte">
 
### 2. Zielkonflikt & Fazit
* **Dilemma:** Reichweite vs. Datenschutz
* **WhatsApp:** Max. Alltagstauglichkeit
* **Threema:** Max. Datenschutz & Anonymität
* **Fazit:** Wahl hängt von Prioritäten ab
  
  </div>
</div>

<div class="fusszeile">
  Alltagstauglichkeit & Praxis-Check · Ward, 9B
</div>



---
Vertiefte Prüfung: Threema im Check

* **Prüfung 1: Alltagstauglichkeit & Erreichbarkeit**
  * *Frage:* Wie viele Kontakte nutzen den Dienst im Alltag?
  * *Antwort:* 0 Personen im eigenen Umfeld; geringe Verbreitung im deutschen Gesamtmarkt.

* **Prüfung 2: Datenschutz & Quellcode**
  * *Frage:* Ist der Code unabhängig geprüft und transparent?
  * *Antwort:* Ja, Open Source und durch externe Audits (u. a. belegt durch SoftMaker) positiv bestätigt.

* **Prüfung 3: Kostenmodell**
  * *Frage:* Welches Finanzierungsmodell liegt vor?
  * *Antwort:* Einmalig kostenpflichtig im iOS App Store und Google Play Store (keine Werbe-Finanzierung).
---
Welcher Messenger passt zu welchen Prioritäten?

* **Priorität Reichweite & Bequemlichkeit:**
  * **WhatsApp:** Höchste Erreichbarkeit, aber Abstriche beim Datenschutz.

* **Priorität Balance (Datenschutz + Kostenlos):**
  * **Signal:** Hoher Datenschutz, Open Source, kostenfrei nutzbar.

* **Priorität Maximale Anonymität & Unabhängigkeit:**
  * **Threema:** Höchste Standards, erfordert jedoch Zahlungsbereitschaft und Akzeptanz der geringen Reichweite.
---
<div class="titel">

# Merksatz oder Kasten

</div>

<div class="merksatz">
 Kein Messenger ist perfekt: Die Wahl zwischen WhatsApp, Signal und Threema ist immer ein persönlicher Kompromiss zwischen Alltagstauglichkeit, Kosten und Datenschutz .
</div>

<div class="box">

- WhatsApp: Max. Reichweite und Bequemlichkeit aber geringer Datenschutz
- Signal: Der beste Kompromiss, da er kostenlos, Open Source und datenschutzfreundlich ist
- Threema: maximaler Datenschutz und Anonymität aber es erfordert einen einmaligen Kauf und Akzeptanz der Nische

</div>

<div class="fusszeile">
  Merksatz · Ward, 9B
</div>

---

### Meine Wahl im Alltag: WhatsApp
* **Erreichbarkeit schlägt Theorie:** Da 0 Personen in meinem Umfeld Threema nutzen, nützt mir der beste Datenschutz im Alltag nichts.
* **Pragmatismus:** Für meine tägliche Kommunikation ist die maximale Reichweite der entscheidende Faktor.
* **Mein Fazit:** Ich nutze WhatsApp aus Bequemlichkeit, bin mir der Datenschutz-Problematik durch diese Arbeit aber voll bewusst.
  
  </div>
</div>

<div class="fusszeile">
  Fazit & Entscheidung · Ward, 9B
</div>

---

<div class="titel">

# Quellen

</div>

<div class="liste">

- [Messenger-Vergleich 2026: Signal, WhatsApp, Telegram – wer schützt Ihre Daten wirklich?](https://www.softmaker.de/blog/freitag-punkt-12/blog-messenger-vergleich-datenschutz-2026), abgerufen am 28.10.26
- [Beleg für den Preis von Threema](https://apps.apple.com/us/app/threema-the-secure-messenger/id578665578)
(https://play.google.com/store/search?q=threema&c=apps&hl=enhttps://beispiel.de), vom 28.10.26
- [ARD Studie](https://www.ard-zdf-onlinestudie.de/files/2021/ARD_ZDF_Onlinestudie_2021_Publikationscharts_final.pdf) vom 28.10,26
- [Zusammenfassung der Studie](https://www.ard-zdf-onlinestudie.de/files/2021/PM_ARD_ZDF_Onlinestudie_2021_final.pdf) vom 28.10.26

</div>

<div class="fusszeile">
  Quellen · Ward, 9B
</div>
