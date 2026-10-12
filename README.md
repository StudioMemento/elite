# Memento Elite · Vercel

Anteprima del sito di fine dining: immagini morbide, palette avorio, animazioni lente e controllate, galleria, menu, lingua IT/EN e percorsi dimostrativi di prenotazione. React + Vite. Immagini, icone e font vengono serviti dal progetto.

## Pubblicare su Vercel

1. Estrai lo ZIP in una cartella.
2. Carica il contenuto in un repository Git e importalo in Vercel. Seleziona come Root Directory la cartella che contiene `package.json` e `vercel.json`.
3. Avvia il deploy. La configurazione è già inclusa:

| Impostazione | Valore |
| --- | --- |
| Framework | Vite |
| Install Command | `npm ci` |
| Build Command | `npm run build` |
| Output Directory | `dist` |
| Node.js | 24.x |
| Variabili d'ambiente | Nessuna richiesta |

In alternativa, dalla cartella estratta puoi eseguire `npx vercel` per creare una preview. Dopo averla verificata, `npx vercel --prod` pubblica in produzione.

Documentazione: [Vite su Vercel](https://vercel.com/docs/frameworks/frontend/vite) e [configurazione del progetto](https://vercel.com/docs/project-configuration).

## Sviluppo locale

Con Node.js 24:

```sh
npm ci
npm run dev
```

Per generare e verificare la build:

```sh
npm run build
npm run preview
```

Il comando `npm run test:ui` verifica i percorsi principali tramite simulazione DOM: menu, galleria, IT/EN e moduli. Non sostituisce la verifica visiva in un browser.

## Contenuti e prenotazioni

I testi si trovano in `src/copy.js`, i componenti in `src/App.jsx`, gli stili in `src/styles.css` e le otto immagini in `public/assets/`.

Le prenotazioni e le richieste per cene private sono dimostrative: non inviano dati, non riservano tavoli e non generano email. Prima di usarle per un ristorante reale occorre collegare un servizio di prenotazione e aggiornare i contenuti del concept.

Dopo aver scelto il dominio definitivo, aggiorna in `index.html` l'immagine Open Graph con il suo URL assoluto e aggiungi il metadato `og:url` del sito.

Questo archivio contiene i sorgenti e gli asset. Vercel genera la cartella `dist` durante la build; le dipendenze vengono installate dal lockfile.
