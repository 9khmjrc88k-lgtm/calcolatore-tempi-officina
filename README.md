# Calcolatore Tempi Officina Brescia

Web app statica responsive per catalogo lavorazioni e tempi.

## Pubblicazione con GitHub Pages
1. Creare un repository GitHub, ad esempio `calcolatore-tempi-officina`.
2. Caricare **tutto il contenuto** di questo pacchetto nella root del repository e usare il branch `main`.
3. In **Settings > Pages > Build and deployment > Source**, scegliere **GitHub Actions**.
4. Aprire **Actions** e attendere il completamento del workflow `Deploy GitHub Pages`.
5. Il link pubblico apparira in **Settings > Pages** e nel job di deploy.

> Attenzione: GitHub Pages pubblica un sito web. Non inserire nel repository o nei CSV distribuiti dati riservati, VIN reali, credenziali o materiale MAN non autorizzato alla pubblicazione.

Il file `index.html` e l'entry point del sito. `.nojekyll` evita elaborazioni Jekyll non necessarie.

## PWA
Include manifest, icone 192/512, splash screen e service worker `sw.js` per cache dell'app shell. Dopo il primo caricamento via HTTPS puo essere installata dal browser.

## Verifica struttura
La root pubblicata contiene `index.html`, `404.html`, `manifest.webmanifest`, `sw.js`, icone e splash. Il workflow usa `actions/upload-pages-artifact@v4` e separa build/deploy con `needs: build`.
