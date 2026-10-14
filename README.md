# Mine Noter — privat Notes-inspireret webapp

Dette projekt er en selvstændig, mobilvenlig webapp med mapper, søgning, noter, tjeklistepunkter, automatisk lokal lagring og eksport af backup.

## Vigtigt om privatliv og begrænsninger
- Noter gemmes i `localStorage` i den browser/profil, hvor appen bruges. De sendes ikke af appens kode til en server.
- Appen synkroniserer ikke med iCloud og har ikke Apples private funktioner eller originale Notes-motor.
- Browserdata kan slettes af brugeren, iOS eller browseren. Brug **Eksportér noter** regelmæssigt for at lave backup.
- Denne startversion har ikke adgangskode eller kryptering af noter. Brug den ikke til følsomme oplysninger.
- Hvis du offentliggør projektet via GitHub Pages, bliver webappens kode offentligt tilgængelig. Dine noter er ikke i projektfilerne, men ligger lokalt i browseren.
- Tjeklistepunkter indsættes som tekst med `☐`. Du kan markere dem manuelt ved at ændre `☐` til `☑`.

## Test på Windows
1. Pak ZIP-filen ud.
2. Åbn mappen i Visual Studio Code eller en anden teksteditor.
3. Du kan dobbeltklikke på `index.html` for en hurtig test. Browserens lokale lagring virker, men PWA-installation/offline-funktioner kræver en HTTPS-side eller lokal udviklingsserver.
4. For at teste lokalt med en enkel server kan du installere Python og køre i mappen:
   `python -m http.server 8000`
   Åbn derefter `http://localhost:8000`. (Service workers kræver localhost eller HTTPS.)

## Udgiv gratis med GitHub Pages
1. Opret/log ind på GitHub: https://github.com/
2. Opret et nyt repository. Hvis du ønsker, at koden ikke er offentlig, skal du være opmærksom på, at GitHub Pages typisk kræver et offentligt repository på gratisplanen. Du kan i stedet bruge en anden HTTPS-hostingløsning.
3. Upload indholdet af denne mappe (ikke ZIP-filen) til repositoryts rod: `index.html`, `manifest.webmanifest`, `sw.js` og `icons/`.
4. I repository: **Settings → Pages**.
5. Vælg **Deploy from a branch**, vælg `main` og `/ (root)`, og gem.
6. Vent på, at GitHub Pages viser en webadresse. Åbn den på din iPhone i Safari.

## Føj til iPhone-hjemmeskærmen
1. Åbn appens HTTPS-adresse i **Safari**.
2. Tryk på Del-knappen (firkant med pil op).
3. Vælg **Føj til hjemmeskærm**. Hvis valget ikke ses, rul ned i delingsmenuen.
4. Behold navnet “Mine Noter”, og tryk **Tilføj**.
5. Start appen fra det nye ikon. Opret en testnote og luk/åbn appen for at kontrollere, at den er gemt.

## Brug
- **＋** opretter en note.
- **＋ Mappe** opretter en mappe.
- Vælg en mappe for at filtrere noter.
- Brug søgning for at finde tekst i titler og indhold.
- **Flyt** flytter den aktuelle note til en anden mappe.
- **Slet** sletter den aktuelle note efter bekræftelse.
- **Tjekliste** indsætter et `☐`-punkt i teksten.
- **Eksportér noter** downloader en JSON-backup, som du skal opbevare sikkert.

## Import af backup
Import er ikke inkluderet i denne startversion. Eksportfilen er JSON og kan bruges til manuel gendannelse i en senere version. Gem backupfilen et sikkert sted.
