# Progetto OMNITRIX - High-End Music Player Interface

## 📌 Descrizione
"Omnitrix" è un'interfaccia web per un lettore musicale custom basato su Raspberry Pi 4. Il sistema sostituisce il "cervello" di uno stereo Philips ed è racchiuso in un case di legno elegante con pulsanti fisici.

L'interfaccia (UI) gira in Kiosk Mode su un display Touchscreen da 14 pollici.

## 💻 1. Specifiche Hardware
* **Display:** 14" Touchscreen.
* **Risoluzione Rigida:** `1920x1080` (Full HD). Il layout DEVE usare `100vw` e `100vh` senza breakpoint per schermi più piccoli.
* **Interazione:** Solo Touch. Niente effetti hover o cursori del mouse.

## 🎨 2. Stile e Design ("Morning Blues")
NONOSTANTE IL NOME "OMNITRIX", NON USARE VERDE NEON.
Il design si ispira allo stile "Morning Blues": elegante, retro-futuristico, materiali premium (legno/nero opaco).
* **Sfondo:** Dark mode profondo (`#121212`, `#0a0a0a`) con effetti Glassmorphism (`backdrop-filter: blur`).
* **Colore Accento (Accent Color):** Sostituire tutto il verde con un **Ice Blue/Cyan (#00d2ff)** oppure un **Warm Amber (#ff9800)** o bianco luminoso.
* **Font Orologio:** Tassativamente **`Gelis Teko`** (caricato localmente da `fonts/GelisTeko.ttf`).
* **Font Principale:** Montserrat o simile (sans-serif pulito).

## 📐 3. Struttura Layout (Single Page)
Un singolo `index.html` diviso in 3 sezioni scrollabili orizzontalmente:
1. **HOME:** Orologio digitale gigante e data. Mini-player in basso (visibile solo qui).
2. **MUSIC:** Split screen 50/50. 
   - Sinistra: Cover album grande, controlli, Artist Name (sotto la cover).
   - Destra: Track Title in alto, sotto il testo (Lyrics) o la coda (Queue).
3. **LIBRARY:** Griglia a 2 colonne, card rettangolari (immagine a sinistra, testo a destra).
4. **Header Fisso:** Navigazione a sinistra, Ricerca e Dropdown menù di sistema a destra.

## ⚙️ 4. Regole UI Interattive (Istruzioni AI)
* **Smart "LED Scroller" (Marquee):** I titoli e gli artisti lunghi devono scorrere in loop continuo verso sinistra (e riapparire da destra) SOLO se superano la larghezza del loro contenitore. Se sono corti, restano fermi.
* **Samsung One UI Progress Bar:** Le barre di avanzamento devono avere un effetto onda liquida (due SVG sovrapposti e sfasati) sul bordo superiore della parte riempita. Devono poter essere trascinate/cliccate (scrubbable).
* **Toggle Icons:** Le icone per passare da Testo a Coda devono essere SVG standard e puliti (stile Spotify).
