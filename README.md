# mrml labs

Die Studio-Seite „mrml labs“ mit den Spielen Mrml Roll und Mrml Sort, dazu Datenschutzerklärung und Support für beide.
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
- `mrml-sort/`: Seite des Spiels mit dem Probespielen, `datenschutz.html` (nur für die App), `support.html`
- `bilder/`: `kugel-*` die Murmeln der Spiele, `spiel-*` die laufenden Bilder der Startseite, `schirm-*.jpg` und `karte-*.jpg` Bilder auf den Seiten der Spiele (bei Mrml
  Roll Entwürfe, bei Mrml Sort, `*-sort-*`, Bildschirmfotos der App), `probespiel.jpg` die Webfassung Murmel, `icon*` Icon
  der Seite, `mrml-*-icon*` Icons der Apps, `vorschau-*.png` Vorschau für geteilte Links
- `schrift/`: Fraunces kursiv, SIL Open Font License 1.1 (`Fraunces-OFL.txt`)

## Startseite

Eine Wand in zwei Farben mit einer Bilderleiste. Auf ihr stehen beide Spiele als Bilder im Holzrahmen; darin läuft das
Spiel selbst, aufgenommen im Simulator (`bilder/spiel-*.mp4`, 752 × 808, Schleife mit weichem Übergang, ohne Ton). Die
Murmeln rollen beim Laden aufeinander zu: Körper oder Streifen drehen sich (`kugel-*-streifen.svg`, `kugel-sort-koerper.webp`),
Glanz und Schatten bleiben stehen. „Bewegung anhalten“ und „Bewegung reduzieren“ zeigen Standbilder (`spiel-*-still.jpg`).

## Probespielen

Im Rahmen auf `mrml-sort/` läuft Murmel von <https://tillhess.github.io/murmel/>. Der Knopf springt zu `#probespielen`,
`:target` blendet den Rahmen ein, und erst dann lädt er (`loading="lazy"`). Auf schmalen oder flachen Bildschirmen führt der
Knopf auf die ganze Seite von Murmel, dort wäre der Rahmen zu klein (`.nur-breit` und `.nur-schmal` in `stil.css`).

## Was sich später ändert

- **App Store:** in `index.html`, `mrml-roll/index.html` und `mrml-sort/index.html` das `<span class="knopf bald">` durch den Verweis ersetzen.
- **Bildschirmfotos:** unter gleichem Namen ersetzen. Bei Mrml Sort: `schirm-sort-ipad.jpg` 1640 : 2292, `karte-sort-*.jpg`
  3 : 2. Bei Mrml Roll dabei `width`, `height` und `alt` in `mrml-roll/index.html` anpassen.
  `schirm-iphone.jpg` hochkant 200 : 432 (mindestens 600 × 1296), `schirm-ipad.jpg` quer 4 : 3 (mindestens 1200 × 900),
  `karte-*.jpg` 3 : 2.
- **Adresse:** `og:image` in jedem Kopf nennt die volle Adresse der Seite.
- **Käufe oder Datenschutz:** `impressum.html` und `datenschutz.html` in beiden Ordnern anpassen.
- `support.html` und `datenschutz.html` behalten in beiden Ordnern ihre Adresse, sie stehen in App Store Connect.
