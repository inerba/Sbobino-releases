# Sbobino

<p align="center">
  <img src=".github/images/cover.png" alt="Sbobino - registra, trascrivi, copia" width="100%">
</p>
Sbobino è un’app desktop per Windows pensata per registrare e trascrivere call, lezioni, webinar, video e contenuti audio senza dover usare strumenti complessi da riga di comando.

Il suo punto forte è il registratore integrato: puoi registrare solo il microfono, solo l’audio del computer tramite loopback, oppure entrambi insieme. In questo modo, durante una call, puoi catturare sia la tua voce sia quella delle altre persone e ottenere una trascrizione unica, pronta da copiare.

Sbobino può anche lavorare su file già esistenti, per esempio una registrazione fatta con OBS Studio, un video salvato, una lezione registrata o un file audio. L’app estrae e prepara l’audio, lo invia a OpenRouter e restituisce il testo trascritto.

## Features

- Registra call e riunioni catturando microfono e audio di sistema insieme.
- Supporta tre modalità di registrazione: microfono, loopback, microfono + loopback.
- Trascrive video e registrazioni già esistenti, anche create con OBS Studio.
- Estrae automaticamente l’audio dai video.
- Converte l’audio in formato adatto alla trascrizione.
- Ottimizza l’audio con rimozione dei silenzi e accelerazione del parlato.
- Divide automaticamente i file audio grandi prima dell’upload.
- Permette la scelta automatica o manuale del modello di trascrizione OpenRouter.
- Mostra la trascrizione nell’app e permette di copiarla negli appunti.
- Controlla la disponibilità di nuove versioni dalla repository pubblica delle release.

## Prerequisiti

Per usare Sbobino servono:

- Windows;
- connessione internet attiva;
- account OpenRouter;
- chiave API personale di OpenRouter;
- `ffmpeg`, necessario per estrarre e convertire l’audio;
- dispositivi audio configurati correttamente, se vuoi registrare microfono o audio di sistema.

OpenRouter supporta API dedicate per la trascrizione audio tramite endpoint speech-to-text.

## Trascrizioni a basso costo

Uno degli obiettivi di Sbobino è rendere la trascrizione accessibile anche per registrazioni frequenti o di lunga durata. I modelli supportati da OpenRouter hanno costi molto bassi e l’app è progettata per scegliere automaticamente quello più conveniente in base alla durata dell’audio.

Questo significa che una breve nota vocale, una call di pochi minuti e una registrazione lunga non vengono trattate allo stesso modo: Sbobino seleziona il modello più adatto per ridurre il costo complessivo della trascrizione.

Indicativamente, la selezione automatica può funzionare così:

- audio brevi: **Qwen3 ASR Flash**;
- audio medi: **Mistral Voxtral Mini Transcribe**;
- audio lunghi: **OpenAI Whisper Large v3 Turbo**.

I costi effettivi dipendono dal listino aggiornato di OpenRouter e dai modelli disponibili al momento dell’utilizzo. Per consultare prezzi, provider e modelli aggiornati, fai riferimento alla pagina ufficiale:

[Modelli di trascrizione disponibili su OpenRouter](https://openrouter.ai/models?output_modalities=transcription)

## Installazione

### 1. Scarica Sbobino

1. Vai nella pagina delle release del progetto.
2. Scarica l’ultima versione disponibile.
3. Estrai il file `.zip` in una cartella a tua scelta.
4. Avvia `Sbobino.exe`.

Sbobino è portable: non richiede installazione tradizionale.

### 2. Installa ffmpeg

Sbobino usa `ffmpeg` per estrarre l’audio dai video e prepararlo alla trascrizione.

Puoi configurarlo in uno di questi due modi:

#### Opzione A: ffmpeg nella cartella di Sbobino

1. Scarica una build Windows di `ffmpeg`.
2. Estrai l’archivio scaricato.
3. Trova il file `ffmpeg.exe`.
4. Copia `ffmpeg.exe` nella stessa cartella di `Sbobino.exe`.

Questa è l’opzione più semplice se vuoi tenere tutto nella stessa cartella.

#### Opzione B: ffmpeg nel PATH di Windows

1. Scarica ed estrai `ffmpeg`.
2. Copia il percorso della cartella che contiene `ffmpeg.exe`.
3. Aggiungi quel percorso alle variabili d’ambiente di Windows, nella voce `Path`.
4. Riavvia Sbobino.

Per verificare che `ffmpeg` sia disponibile, puoi aprire il Prompt dei comandi e scrivere:

```bash
ffmpeg -version
```

Se compare la versione installata, `ffmpeg` è configurato correttamente.

## Uso

### Registrare una call

1. Apri Sbobino.
2. Scegli la modalità di registrazione:
   - microfono;
   - audio di sistema;
   - microfono + audio di sistema.

3. Avvia la registrazione prima o durante la call.
4. Ferma la registrazione quando hai finito.
5. Avvia la trascrizione.
6. Copia il testo ottenuto.

Questa modalità è utile per riunioni online, lezioni in streaming, webinar e conversazioni in cui vuoi registrare sia la tua voce sia quella degli altri partecipanti.

### Trascrivere un video già registrato

Puoi usare Sbobino anche con file creati da OBS Studio o da altri programmi di registrazione.

```text
1. Registra un video con OBS Studio
2. Apri Sbobino
3. Seleziona il file video
4. Sbobino estrae automaticamente l’audio
5. L’audio viene preparato per la trascrizione
6. La trascrizione viene mostrata nell’app
```

## Disclaimer

Sbobino è uno strumento tecnico per registrare, convertire e trascrivere contenuti audio o video. L’utente è l’unico responsabile dell’uso che ne fa.

Prima di registrare, trascrivere o caricare contenuti su servizi esterni, assicurati di avere il diritto di farlo. In particolare, devi verificare che:

- le persone coinvolte siano state informate e, quando necessario, abbiano autorizzato la registrazione;
- il contenuto non violi diritti di terzi, inclusi diritti d’autore, diritti connessi, riservatezza, segreti professionali o obblighi contrattuali;
- l’uso della registrazione e della trascrizione sia conforme alle leggi applicabili in materia di privacy, protezione dei dati personali e copyright;
- eventuali piattaforme, servizi o contenuti registrati consentano questo tipo di utilizzo.

L’autore del progetto non è responsabile per usi impropri, non autorizzati o illeciti dell’applicazione. Sbobino non aggira protezioni tecniche, non concede diritti sui contenuti trattati e non sostituisce una valutazione legale sull’uso delle registrazioni.
