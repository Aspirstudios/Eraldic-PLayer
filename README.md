# Eraldic-PLayer
May the music guide you through these realms
In the dawn of this century of silicons and algorithms, a herald walks the battlements announcing a new work: Heraldic Player, a YouTube player forged entirely in Python, with its own GUI on pygame and a character drawn directly from medieval heraldry: severe black and white, golden filigree, crossed swords, crowns, castles and fleurs-de-lis.

It is not just another wrapper around the API of the day. It is a handcrafted piece, written line by line, designed to run locally, without foreign accounts, without telemetry, without empty promises. It uses the system user as lord of the castle and saves its profile in ~/.ytmusic_cmd/profiles.json, like a scribe noting each session on his parchment.

I. The castle gate
When you open the application, you are not greeted by a cold menu. You see a heraldic intro: two swords converging over a radiant sun, a golden flash and finally the name of the house: Heraldic Player. The user also receives a random greeting, as if a different herald welcomed them each day: “Greetings, my lord. May the chords guide your day.”, “The troubadour tunes his lute.”, “The castle gates open.”

II. The search, sharp as a blade
The search engine does not settle for a single strategy. It queries YouTube through several cascading paths, respecting the real ranking of the site and not an approximate imitation:

Direct request to the results URL via yt-dlp, with the sp parameter correctly encoded.
Its own InnerTube query using urllib, independent of the extractor.
Reading the results page and decoding ytInitialData.
As a last resort, ytsearchN: from yt-dlp itself.
If yt-dlp fails, the application detects it and updates itself via pip. If everything fails, it leaves an honest record in search_error.log. There is no black magic: there is engineering in armour.

III. Filters, queue and library
Each result is classified with judgement: song, video or podcast, according to channel, duration and title. The queue is shown on the left, like a banner of playback; on the right, the library with favourites, history, saved lists and recent lists. Saved lists are synchronised automatically when the application opens, with a timestamp and cover art taken from the first track.

IV. The equaliser and pitch
Beneath the cover of the playing track, a forty-band equaliser pulses, reading live audio through ffmpeg and decomposing it in real time with numpy. It is not decorative: it breathes with the music.

The speed control goes from x0.50 to x2.00 and is applied by VLC without touching the pitch. The pitch control allows raising or lowering up to twelve semitones, processing the audio with ffmpeg, using rubberband when available and an asetrate trick with atempo when not. Processed files are cached and purged automatically once they exceed 250 MB.

V. Downloads and ffmpeg
Downloading is as simple as pressing O for the current track or W for the whole view. Files land in ~/Music/YTMUSIC_CMD, converted to MP3 if ffmpeg is available, or to M4A otherwise. The application resolves ffmpeg by itself, even if it has to fetch it from imageio-ffmpeg.

VI. The home screen, like a stained-glass window
The home mode is not a list. It is an animated stained-glass window with golden stars that twinkle and drift slowly across the screen. On it, horizontal shelves unfold: saved lists, recent lists, listened tracks, favourites and suggestions — all drawn from the user's history and tastes. Covers are loaded in parallel threads, so the interface never stalls waiting for the network.

VII. No accounts, no noise
There is no Google login, no OAuth, no tokens. The system user is the lord. Everything is saved locally. The application installs its own dependencies if missing (yt-dlp, python-vlc, pygame, pillow, numpy, imageio-ffmpeg) and restarts itself the first time. If VLC is not installed, it tries to install it with winget, brew, apt, dnf or pacman, depending on the kingdom where it runs.

VIII. Knight's shortcuts
Space · pause and resume.
N / P · next and previous.
+ / - · volume.
← / → · rewind or forward ten seconds.
[ / ] · decrease or increase speed.
, / . · lower or raise pitch by one semitone.
S / R · shuffle and repeat.
F · favourite. G · save list.
Y · sync all saved lists.
I · go home. L · library.
/ · search. Q · quit.
IX. A brief manifesto
Heraldic Player does not aim to be the most powerful or the fastest player. It aims to be honest: to use YouTube without intermediaries, to download without asking permission, to equalise without selling data, and to dress everything with the solemnity of a heraldic shield. A program written to last, to be read and to sound.

May music fill your tavern, lord of chords
