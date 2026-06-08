# Sbobino

<p align="center">
  <img src=".github/images/cover.png" alt="Sbobino - record, transcribe, copy" width="100%">
</p>

Turn videos, recordings, online audio, meetings, lessons, interviews, webinars, and voice notes into clean text with a simple Windows app.

Sbobino is made for people who need a transcript without fighting with complicated tools. Pick a file, record your audio, or paste a YouTube link. Sbobino prepares the sound, sends it to the transcription service you choose, and gives you readable text you can copy, save, search, edit, share, or turn into notes.

## Download

Get the latest Windows installer from GitHub:

[Download the latest Sbobino release](https://github.com/inerba/Sbobino-releases/releases/latest)

Open the release page, download the `Sbobino-...-Setup.exe` file, run it, and start Sbobino from the Start menu.

## What Sbobino Is For

Sbobino helps when you have spoken content and you want the words.

Use it for:

- meetings and calls;
- university lessons and online courses;
- webinars and tutorials;
- interviews and research recordings;
- podcasts and voice notes;
- screen recordings;
- YouTube videos;
- audio playing from your computer;
- microphone recordings;
- video files where you only need the audio or transcript.

Instead of opening different apps for downloading, converting, recording, and transcribing, Sbobino brings the whole flow into one small desktop window.

## The Main Idea

Sbobino works in three simple steps:

1. Choose where the audio comes from.
2. Let Sbobino prepare it.
3. Get the transcript.

The source can be a local video, a local audio file, a YouTube link, your microphone, your computer audio, or both microphone and computer audio together.

When the source is a video, Sbobino extracts the audio first. When the source is already an audio file, it can transcribe it directly. When the audio is long or heavy, Sbobino handles it in smaller parts so the job is easier to complete.

## What You See When You Open It

The app is intentionally direct.

At the top, you choose the source:

- **Record** starts a live recording.
- **Browse** lets you choose a video or audio file from your computer.
- **YouTube** lets you paste a video link and prepare its audio.

After a source is ready, Sbobino shows the actions that make sense for that source. If you choose a video, you can extract audio. If transcription is configured, you can transcribe. If recording is active, you see the timer, pause button, stop button, and sound levels.

The status bar at the bottom tells you what is happening: downloading, converting, recording, uploading, transcribing, saving, or waiting.

## Local Files

Sbobino accepts both video and audio files.

For videos, it can:

- extract the audio only;
- convert the audio into a compact format that is good for transcription;
- automatically start transcription after conversion.

For audio files, it can:

- transcribe directly;
- optionally optimize the audio before transcription;
- save the resulting transcript next to the audio file.

Supported video files include:

`MP4`, `MKV`, `AVI`, `MOV`, `WMV`, `FLV`, `M4V`, `TS`, and `MTS`.

Supported audio files include:

`MP3`, `WAV`, `M4A`, `FLAC`, `OGG`, `OPUS`, `WEBM`, `MPGA`, `MPEG`, and `AIFF`.

## YouTube Audio

The YouTube button is for people who want a transcript from a video without manually downloading audio first.

Paste a YouTube link, and Sbobino downloads the audio, converts it into its compact audio format, and makes it ready for transcription.

This is useful for:

- lectures;
- public talks;
- tutorials;
- interviews;
- long videos you want to summarize or quote.

After the YouTube audio is ready, it behaves like any other audio source in the app.

## Recording

Sbobino can record audio directly from your computer.

You can record:

- **Microphone** - your voice or anything captured by your input device.
- **Loopback** - the sound playing through your computer, such as a meeting, browser video, music player, or webinar.
- **Both** - microphone and computer audio together, mixed into one file.

While recording, Sbobino shows:

- a recording timer;
- pause and resume;
- stop;
- live sound level meters for microphone and computer audio.

When you stop, Sbobino prepares the recording as an audio file and makes it immediately ready for transcription.

This is especially useful for online meetings where you want your own voice and the other speakers in one transcript.

## Audio Extraction

If you only want the audio from a video, use **Extract audio only**.

Sbobino creates an audio file in the folder you chose in Settings. If a file with the same name already exists, Sbobino creates a new name instead of overwriting it.

This is useful when you want to keep the audio, send it elsewhere, archive it, or transcribe it later.

## Transcription

The **Transcribe** button sends your prepared audio to the transcription provider you choose in Settings.

Sbobino currently supports:

- **OpenRouter**
- **Blip AI**

With OpenRouter, you can choose the transcription model from the app. Sbobino can also show model pricing when that information is available, and after a transcription it may show the cost reported by the provider.

With Blip AI, Sbobino uses your Blip AI token. If the token expires, the app asks for a fresh one and can continue the transcription flow after you paste it.

The transcript appears inside the app as soon as it is available. For long files, partial text appears progressively while the work continues.

When transcription finishes, Sbobino automatically saves a text file next to the audio source and also lets you copy the transcript to the clipboard with one click.

## Optimize And Transcribe

Some recordings are long because they contain pauses, silence, slow speech, or empty sections. **Optimize & transcribe** prepares the audio before sending it for transcription.

It can:

- remove silent parts;
- speed up spoken audio;
- make long recordings lighter and faster to process.

This can help with long meetings, classes, calls, and recordings where only the spoken content matters.

In Settings, you can choose:

- how much the audio should be sped up;
- how quiet a part must be before Sbobino treats it as silence;
- how long the silence must last before it is removed.

This option is available for OpenRouter transcription.

## Long Files

Large audio files can be difficult for transcription services. Sbobino handles this automatically.

When a file is too large, the app splits it into smaller parts, transcribes them in order, and joins the text back together. You do not have to do anything manually.

Very tiny empty parts are skipped, because they usually contain no speech and can cause useless errors.

## Transcript Output

Sbobino gives you the transcript in two ways:

- visible inside the app;
- saved as a `.txt` file.

The **Copy text** button copies the transcript to your clipboard, ready to paste into Word, Notion, Google Docs, email, chat, a summary tool, or your note system.

The saved text file is created automatically after a successful transcription. If a transcript file already exists, Sbobino creates a numbered filename instead of replacing your previous work.

## Settings

The Settings screen is split into clear areas.

### AI

Here you choose the transcription provider and enter the API key or token.

For OpenRouter, Sbobino links you to the key page and lets you choose the transcription model.

For Blip AI, Sbobino links you to the dashboard and reminds you that tokens can expire.

Your key is saved locally on your computer. Sbobino does not run its own transcription server and does not collect your files.

### Audio

Here you choose how Sbobino prepares audio.

You can set:

- audio quality;
- mono or stereo;
- sample rate;
- the default folder for saved audio;
- the location of FFmpeg if Sbobino cannot find it automatically;
- recording source;
- microphone device;
- computer audio device;
- optimization settings.

The app recommends compact audio settings because transcription usually does not need studio-quality sound. Smaller files upload faster and may cost less, depending on the provider.

### Application

Here you can choose:

- interface language;
- visual theme.

The interface supports Italian, English, French, Spanish, German, and Polish.

Themes are applied immediately so you can preview them before saving.

## What You Need

Sbobino is a Windows desktop app.

For transcription, you need:

- an internet connection;
- an API key or token for the provider you want to use.

For audio conversion and recording finalization, Sbobino needs FFmpeg. If it is not found, the app tells you what to do. You can place `ffmpeg.exe` next to Sbobino, install it normally on Windows, or select its exact location in Settings.

For recording computer audio, your Windows audio devices must support loopback recording. Most normal Windows systems do, but the exact available devices depend on your machine.

## Updates

Sbobino checks GitHub for new public releases when it starts. If a newer version is available, it shows a download link.

You can always get the latest installer here:

[https://github.com/inerba/Sbobino-releases/releases/latest](https://github.com/inerba/Sbobino-releases/releases/latest)

## Why People Use It

Sbobino is useful because it keeps the boring parts out of the way.

You do not need to manually extract audio from a video. You do not need to prepare a recording in another program. You do not need to split a long file by hand. You do not need to hunt for the saved transcript. You choose the source, press the right button, and get text.

It is built for people who have real spoken material to process and want a fast path from sound to words.

## Start Here

Download the latest release, install Sbobino, add your transcription provider key in Settings, and try it with a short audio or video file.

[Download Sbobino from GitHub Releases](https://github.com/inerba/Sbobino-releases/releases/latest)
