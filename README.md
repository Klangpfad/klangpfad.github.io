# klangpfad.github.io – Einstieg für Anfänger

Diese Codebasis ist eine **statische Website** (kein Build-Prozess, kein Framework, kein Backend).
Du kannst die Seiten direkt als HTML-Dateien öffnen oder über GitHub Pages ausliefern.

## 1) Projektaufbau

- `index.html`: Hauptseite mit allen Sektionen (Hero, Projekte, GitHub-Section, Kontakt, Soundtrack).
- `gina.html`: separate Unterseite („Gina Universum“) mit eigener Galerie.
- `style.css`: zentrales Stylesheet für alle Seiten.
- `datenschutz.html`, `impressum.html`, `notizen-datenschutz.html`: rechtliche/inhaltliche Unterseiten.
- `images/`, `audio/`, `video/`, `lyrics/`: statische Assets.
- `sitemap.xml`, `robots.txt`: SEO- und Crawler-Hinweise.

## 2) Technischer Kern

### HTML-first
Die Seiten sind klassisch aufgebaut: semantische Abschnitte, Karten-Layout, Footer/Navigation.
Es gibt keine Komponenten-Dateien wie in React/Vue.

### Ein gemeinsames CSS
`style.css` enthält:
- CSS-Variablen (Farben, Schatten, Abstände)
- globale Typografie-/Layout-Regeln
- wiederverwendbare UI-Pattern (`.card`, `.button`, `.tag`, Grid-Layouts)
- Responsive-Verhalten per Media Queries

### Wenig JavaScript, direkt in `index.html`
Die Hauptseite nutzt Inline-JS für progressive Effekte:
- aktuelles Jahr im Footer
- Laden der letzten Repositories via GitHub API
- Fallback, falls API nicht erreichbar
- kleine Interaktions-Effekte (Scroll-Reveal, Tilt, „runlevel“-Easter-Egg)

## 3) Was ist wichtig zu wissen?

1. **Single Source für Styles:**
   Visuelle Änderungen passieren fast immer in `style.css`.
2. **Inhalte leben in HTML:**
   Texte, Sektionen und Links werden direkt in den `.html`-Dateien gepflegt.
3. **Externe Abhängigkeit GitHub API:**
   Die Repo-Box auf der Startseite ist dynamisch; es gibt aber einen statischen Fallback.
4. **Kein Tooling nötig:**
   Du brauchst anfangs nur HTML/CSS/JS-Grundlagen und einen Browser.

## 4) Lernpfad für Einsteiger

Empfohlene Reihenfolge:

1. **HTML verstehen:**
   - Aufbau von `index.html` lesen
   - eine neue Projekt-Karte duplizieren und Text/Link ändern
2. **CSS verstehen:**
   - in `style.css` eine Farbe in `:root` ändern
   - Card-Abstände oder Button-Stil anpassen
3. **JS verstehen:**
   - den GitHub-Fetch-Block in `index.html` nachvollziehen
   - ein `console.log` ergänzen, um Datenfluss zu sehen
4. **Saubere Änderungen üben:**
   - kleine, klare Commits
   - nach jeder Änderung Browser-Check auf Desktop + mobil

## 5) Typische Aufgaben in diesem Repo

- Neue Projektkarte hinzufügen
- Texte in Hero/About/Projekten aktualisieren
- Links auf externe Projekte anpassen
- neue Bilder/Audio einbinden
- rechtliche Texte aktualisieren

## 6) Stolperfallen

- In `index.html` sind viele Abschnitte hintereinander; beim Editieren auf korrekt geschlossene Tags achten.
- Für neue Assets immer korrekte relative Pfade verwenden (`images/...`, `audio/...`, `video/...`).
- Bei JS-Änderungen an der GitHub-Section immer den Fehlerfall testen (API down/Rate limit).

Wenn du neu bist: arbeite zuerst in sehr kleinen Schritten. Diese Codebasis ist dafür gut geeignet, weil sie bewusst leichtgewichtig gehalten ist.
