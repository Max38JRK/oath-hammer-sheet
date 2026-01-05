# Oath Hammer – Digital Character Sheet

Scheda personaggio digitale **HTML/JavaScript standalone** per il gioco di ruolo **Oath Hammer**, progettata per campagne lunghe, uso condiviso e gestione sia Player che Game Master.

Il progetto è **client-only** (nessun backend proprietario) e funziona via:
- browser locale
- GitHub Pages
- sincronizzazione cloud tramite Supabase

---

## 🌐 Link

- **Scheda Giocatore (Player)**  
  👉 `index.html`

- **Scheda Master (GM)**  
  👉 `gm.html`  
  ⚠️ Richiede login (account autorizzato come Master)

---

## 🎯 Obiettivi del progetto

- Gestione completa del personaggio per campagne lunghe
- Salvataggi multipli per più personaggi
- Sincronizzazione online opzionale
- UX da *character manager*, non da semplice PDF
- Nessuna dipendenza da server custom

---

## 🧙 Scheda Giocatore – Player (`index.html`)

### Funzionalità principali
- Scheda completa del personaggio Oath Hammer
- Autosave locale (localStorage)
- Salvataggi multipli (slot)
- Import / Export JSON
- Sincronizzazione online (Supabase)
- UI responsive stile pergamena fantasy
- Sezioni collapsible con stato persistente

### Sezioni supportate
- Character Info (nome, lineage, class, oaths…)
- Attributes
- Armor
- Skills (con:
  - attributo singolo/doppio
  - rank
  - modifier
  - colore dadi
  - calcolo automatico
  - search & sorting)
- Weapons (dinamiche)
- Item Slots
- Magic & Miracles
- Special Traits
- Background
- Notes
- **Notes from the GM** (sola lettura, sincronizzate online)

---

## 🧠 Scheda Master – GM (`gm.html`)

⚠️ **Accesso riservato**: richiede login Supabase con ruolo `master`.

### Funzionalità Master
- Visualizzazione di **tutti i personaggi online**
- Nessuna modifica ai dati del player (read-only)
- Gestione:
  - GM Notes (private)
  - Public Notes (visibili ai player)
- Reload completo da cloud
- Export JSON
- Nessun import / delete / save online accidentale

### Overview Multi-Personaggio
Vista dedicata per:
- panoramica generale
- combattimenti
- gestione rapida

Mostra (con flag attivabili):
- Name
- Experience (XP)
- Luck
- Grit
- Oaths (1–3)
- Arcane Stress
- Stress Threshold
- Spell Save Modifier
- Current Miracle DV
- Skill:
  - Defense
  - Fighting
  - Shooting
- Armor Value (AV)

Alcuni valori (XP, Luck, Grit, Arcane Stress, Miracle DV) sono:
- **editabili solo nel Master**
- **salvati solo localmente**
- **mai sincronizzati online**

---

## 💾 Salvataggio & Sincronizzazione

### Locale
- localStorage
- slot multipli
- metadata per ogni personaggio
- separazione completa Player / Master (anche stesso browser)

### Online (Supabase)
- tabella `characters`
- JSON completo del personaggio
- RLS attiva
- Player: vede solo i propri personaggi
- Master: vede tutti

> Non è presente un sistema di campagne: il progetto è pensato per gruppi chiusi / playtest.

---

## 🛠️ Stack Tecnico

- HTML5
- CSS3
- JavaScript Vanilla
- Supabase JS client
- Nessuna libreria UI esterna

---

## 📌 Stato del progetto

- ✔ Player: stabile
- ✔ Master: stabile
- ✔ Overview multi-PG: implementata
- ✔ Separazione ruoli: implementata
- ✔ Ready for campaign play

Il progetto è **attivamente mantenuto** e pensato per evolvere senza refactor distruttivi.

---

## ⚠️ Nota di Sicurezza

- accettabile per gruppi chiusi
- non pensato per uso pubblico aperto
- nessuna garanzia di isolamento per campagne multiple

---

## 📜 Licenza

Uso personale e di gruppo.  
Sentiti libero di forkare, adattare e migliorare per il tuo tavolo di gioco.

---

Buona campagna e che gli Oath tengano ✨
