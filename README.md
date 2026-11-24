# mrml labs

Die Studio-Seite „mrml labs“ mit den Spielen Mrml Roll und Murmel, dazu Datenschutzerklärung und Support für Mrml Roll.
Einfaches HTML und CSS, ohne Baukasten, ohne JavaScript und ohne Anfragen an fremde Server. Gedacht für GitHub Pages
aus dem Zweig `main`, Ordner `/`.

## Lokal ansehen

Im Ordner **über** diesem, damit die Seite wie später unter `/mrml-labs/` liegt:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Dann <http://127.0.0.1:8000/mrml-labs/> öffnen. Alle Verweise sind relativ; nur `404.html` nennt `/mrml-labs/` fest, weil
GitHub Pages sie unter jedem Pfad ausliefert.

## Was wo liegt

- `index.html`, `impressum.html`, `404.html`, `stil.css`
- `mrml-roll/`: Seite des Spiels, `datenschutz.html` (gilt auch für diese Webseite), `support.html`
- `bilder/`: Bilder aus der Gestaltung von Mrml Roll, `murmel.svg` ist das Icon von Murmel
- `schrift/`: Fraunces kursiv, SIL Open Font License 1.1 (`Fraunces-OFL.txt`)

Kommt Mrml Roll in den App Store: in `index.html` und `mrml-roll/index.html` das `<span>` in `.store` durch den Verweis
ersetzen. Ändern sich Käufe oder Datenschutz, `impressum.html` und `mrml-roll/datenschutz.html` anpassen.
