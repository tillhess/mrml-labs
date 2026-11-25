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
- `bilder/`: `kugel-*.svg` die Murmeln der Spiele, `schirm-*.jpg` und `karte-*.jpg` Entwurfsbilder auf der Seite von
  Mrml Roll, `icon*` Icon der Seite, `mrml-roll-icon*` Icon der App, `vorschau-*.png` Vorschau für geteilte Links
- `schrift/`: Fraunces kursiv, SIL Open Font License 1.1 (`Fraunces-OFL.txt`)

## Was sich später ändert

- **App Store:** in `index.html` und `mrml-roll/index.html` das `<span class="knopf bald">` durch den Verweis ersetzen.
- **Bildschirmfotos:** unter gleichem Namen ersetzen, dabei `width`, `height` und `alt` in `mrml-roll/index.html` anpassen.
  `schirm-iphone.jpg` hochkant 200 : 432 (mindestens 600 × 1296), `schirm-ipad.jpg` quer 4 : 3 (mindestens 1200 × 900),
  `karte-*.jpg` 3 : 2.
- **Adresse:** `og:image` in jedem Kopf nennt die volle Adresse der Seite.
- **Käufe oder Datenschutz:** `impressum.html` und `mrml-roll/datenschutz.html` anpassen.
- `mrml-roll/support.html` und `mrml-roll/datenschutz.html` behalten ihre Adresse, sie stehen in App Store Connect.
