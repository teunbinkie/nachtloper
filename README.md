# Nachtloper

Hardlooptimer met aftelring, Nederlandse stem en een 12-wekenschema voor de 10 km.
Alles draait in de browser; gegevens staan alleen op je eigen toestel.

## Op GitHub Pages zetten

1. Maak een nieuwe repository aan op GitHub (bijvoorbeeld `nachtloper`, public).
2. Upload alle bestanden uit deze map naar de hoofdmap van de repository:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-180.png`, `icon-192.png`, `icon-512.png`.
3. Ga naar Settings > Pages, kies bij Source "Deploy from a branch", branch `main`, map `/ (root)` en sla op.
4. Na een minuut staat de app op `https://<jouw-gebruikersnaam>.github.io/nachtloper/`.

## Op je iPhone zetten

1. Open de link in Safari.
2. Tik op Deel > Zet op beginscherm.
3. Open de app vanaf je beginscherm. Daarna werkt hij ook offline.

## Goed om te weten

- Het scherm moet aan blijven tijdens een training. Een webapp stopt met aftellen en praten zodra de telefoon vergrendelt. De app houdt het scherm zelf wakker.
- De timer rekent met de klok, dus als je even naar Strava wisselt loopt hij daarna gewoon goed verder.
- Maak af en toe een back-up via Instellingen > Gegevens.
- Schema aanpassen: de trainingen staan bovenaan het script in `index.html` in de lijst `PLAN`.
- Na een wijziging: verhoog `nachtloper-v1` in `sw.js` naar `v2`, zodat oude cache wordt opgeruimd.

## Account en synchroniseren (v2)

Je voortgang kan via je GitHub-account op telefoon en pc gelijk blijven.

1. Maak een token: github.com/settings/tokens/new?scopes=gist (classic token, alleen het vinkje "gist", vervaldatum naar keuze).
2. Open in de app Instellingen > Account, vul je naam en de token in en tik op Koppelen.
3. Doe op je pc hetzelfde met dezelfde token.

De gegevens staan in een geheime gist met de naam `nachtloper-data.json`. Die gist is niet openbaar vindbaar, maar wie de link heeft kan hem wel lezen.
