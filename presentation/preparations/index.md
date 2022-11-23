---
class:
  - invert
---

# Continuous Integration

---

# Agenda

* Was ist Continuous Integration?
* Was benötige ich zum Starten?
  * Variante: Kostenpflichtig
  * Variante: Kostenfrei
  * Alternative: Eigener Server

---

# Was ist Continuous Integration?

* Kurz: CI
* Jede Änderung vom Spiel (Code, Assets, ...) wird automatisiert getestet und gebaut
* Direkte Rückmeldung vom System, wenn man etwas kaputt gemacht hat
* Build ist standardisiert -> gleiche Eingabe -> gleiche Ausgabe
* Jeder kann einen Build erzeugen
* "Kein Blockieren vom Entwickler-PC"

---

# Was benötige ich zum Starten?

* Source Code muss irgendwo gehostet sein, z.B.
  * GitHub
  * GitLab
  * PlasticSCM
* Privat (closed source) oder öffentlich (open source) möglich

---

# Was benötge ich zum Starten?
## Variante: "Kostenpflichtig"

* Closed Source Projekte
* Unity Cloud Build
  * Beste & einfachste Unity-Integration
* GitHub Actions
  * 2000 Minuten frei, danach kostenpflichtig
  * Unity-Build dauert, je nach Plattform, 30-60 Minuten für leeres Projekt
  * ~33x CI laufen lassen, bei 60 Minuten Build-Zeit
  * Flexibler als Unity Cloud Build

<!--
   Dauer des Unity-Builds bei IL2CPP.
   Bei Mono kürzer.
   Tendenziell dauern Unity-Builds natürlich immer länger, je größer das Projekt wird und je mehr Plattformen man erzeugen möchte.
-->

---

# Was benötge ich zum Starten?
## Variante: "Kostenfrei"

* Open Source Projekte
* GitHub Actions
  * Keine Beschränkung bei Build-Minuten

---

# Alternative: Eigener Server

* Bei riesigen Projekten, die die Limits (freier) Angebote überschreiten
* Bspw. GitHub
  * Limit der Repository-Größe
  * Maximale Dateigröße ohne Git LFS: 100 MB
  * Timeout eines Jobs in einer GitHub Action: 6 Stunden
* Eigener Server notwendig, z.B. mit Jenkins, TeamCity, ...

---

# Plan

* Anlegen eines GitHub-Repositories
* Anlegen eines Unity-Projekts
* Erstellen der GitHub-Actions