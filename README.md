# 𝔥𝔢𝔯𝔞𝔩𝔡𝔦𝔠 𝔭𝔩𝔞𝔶𝔢𝔯

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![pygame](https://img.shields.io/badge/pygame-2.x-green?logo=python&logoColor=white)
![yt-dlp](https://img.shields.io/badge/yt--dlp-latest-red)
![VLC](https://img.shields.io/badge/VLC-required-orange?logo=vlc&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

> **A handcrafted, local-only YouTube player for the medieval soul.**  
> Black-and-white heraldry, golden filigree, and zero telemetry.

---

## 📜 𝕸𝖆𝖓𝖎𝖋𝖊𝖘𝖙𝖔 𝖔𝖋 𝖙𝖍𝖊 𝕸𝖚𝖑𝖙𝖎𝖒𝖊𝖉𝖎𝖆 𝕬𝖗𝖙𝖎𝖋𝖆𝖈𝖙

At the dawn of this century dominated by silicon and algorithms, when men seem to have forgotten the value of craftsmanship, a herald rides along the battlements of the kingdom announcing a new and singular work: **Heraldic Player**. This is a player for the great library of YouTube **forged entirely in the workshops of Python**, endowed with its own graphical interface on the firm foundations of *pygame* and clad in an aesthetic drawn directly from treatises on medieval heraldry: a severe contrast in black and white, subtle gold filigrees, crossed swords, imperial crowns, castle towers, and fleurs-de-lis.

You are not before a crude wrapper nor an imitation of the commercial interfaces that saturate the overseas market. This is a **handcrafted piece of high digital goldsmithing, written line by line**, conceived from its first stroke to run exclusively in your own local fief. Here you will find no foreign accounts, no spies, no telemetry watching your habits, no empty promises from peddlers. The artifact takes the operating system user as the only and legitimate lord of the castle, guarding the records of his profile in the private ledger of the kingdom, just as a faithful scribe would note each session on the sacred parchment.

**Lord’s profile path:**
```bash
~/.ytmusic_cmd/profiles.json
```

---

## 📖 Table of Contents

- [I. The Gates of the Castle](#i-the-gates-of-the-castle)
- [II. The Search, Sharp as a Toledo Blade](#ii-the-search-sharp-as-a-toledo-blade)
- [III. Filters, Banner of Playback and Library](#iii-filters-banner-of-playback-and-library)
- [IV. The Equalizer and the Art of Tone](#iv-the-equalizer-and-the-art-of-tone)
- [V. Logistics of Supplies and Downloads](#v-logistics-of-supplies-and-downloads)
- [VI. The Main Screen: An Animated Stained-Glass Window](#vi-the-main-screen-an-animated-stained-glass-window)
- [VII. No Tributes, No Accounts, No Noise](#vii-no-tributes-no-accounts-no-noise)
- [The Knight’s Shortcuts](#the-knights-shortcuts)


---

<a name="i-the-gates-of-the-castle"></a>
### 𝓘. 𝓣𝓱𝓮 𝓖𝓪𝓽𝓮𝓼 𝓸𝓯 𝓽𝓱𝓮 𝓒𝓪𝓼𝓽𝓵𝓮

When invoking the artifact, your eyes will not be offended by a cold, generic, soulless menu. Instead, you will behold a purely heraldic introduction: **two solemn swords converging over the figure of a radiant sun**, followed by a golden flash that finally reveals the name of the house: *Heraldic Player*. The sovereign also receives a random greeting drawn from the chronicles, as if a different herald came to the staircase to welcome him each morning:

* “Peace and good, my lord! May the chords guide your journey on this new day.”
* “The troubadour tunes the strings of his lute for your delight.”
* “The gates of the fortress open wide before your presence.”

---

<a name="ii-the-search-sharp-as-a-toledo-blade"></a>
### 𝓘𝓘. 𝓣𝓱𝓮 𝓢𝓮𝓪𝓻𝓬𝓱, 𝓢𝓱𝓪𝓻𝓹 𝓪𝓼 𝓪 𝓣𝓸𝓵𝓮𝓭𝓸 𝓑𝓵𝓪𝓭𝓮

The search engine of this artifact does not settle for a single strategy nor trusts its fate to the hazards of the network. It interrogates the great library through **four perfectly ordered cascade paths**, respecting the site’s royal rank and not a defective approximation:

1. It makes a direct request to the results URL using the power of *yt-dlp*, carrying the `sp` parameter correctly encoded in its lines.
2. It executes its own direct query to the entrails of *InnerTube* via *urllib*, remaining independent of any general extractor.
3. It carries out a meticulous reading of the results page to decode the framework of `ytInitialData`.
4. As a last resort in the face of adversity, it summons the `ytsearchN` spell of *yt-dlp* itself.

If the arts of *yt-dlp* were to falter or become outdated before changes in the outside kingdom, the artifact itself detects it promptly and updates itself via *pip*. If the storm were such that everything else failed, the artifact leaves an honest and transparent testimony in the `search_error.log` file. In these lands there is no witchcraft or black magic: what you behold is pure engineering armored in steel.

---

<a name="iii-filters-banner-of-playback-and-library"></a>
### 𝓘𝓘𝓘. 𝓕𝓲𝓵𝓽𝓮𝓻𝓼, 𝓑𝓪𝓷𝓷𝓮𝓻 𝓸𝓯 𝓟𝓵𝓪𝔂𝓫𝓪𝓬𝓴 𝓪𝓷𝓭 𝓛𝓲𝓫𝓻𝓪𝓻𝔂 🇨🇦

Every melody that enters the domains of the castle is classified with strict judgment by the scribes: individual song, detailed video, or long-duration song (podcast), always judging according to its channel of origin, its exact duration, and the words of its title. **On the left of the interface the playback queue unfolds**, rising majestically like the banner that guides your musical march; on the right, the library zealously guards your favorite songs, the history of past days, saved lists, and recently listened tunes. Saved lists synchronize automatically the moment the gates of the artifact open, bearing their corresponding timestamp and the cover of the first song as a coat of arms.

---

<a name="iv-the-equalizer-and-the-art-of-tone"></a>
### 𝓘𝓥. 𝓣𝓱𝓮 𝓔𝓺𝓾𝓪𝓵𝓲𝔃𝓮𝓻 𝓪𝓷𝓭 𝓽𝓱𝓮 𝓐𝓻𝓽 𝓸𝓯 𝓣𝓸𝓷𝓮

Beneath the visual stamp of the song that resounds in the halls, **a forty-band equalizer pulses with a life of its own**, reading the audio live through the threads of *ffmpeg* and decomposing it in real time through the complex mathematics of *numpy*. We are not before a dead or decorative ornament; the equalizer breathes, vibrates, and dances in perfect consonance with the waves of the music.

The speed control allows you to adjust the pace from a slow and ceremonious step of `x0.50` to a full gallop of `x2.00`, ordered directly to the mystic *VLC* without altering at all the pitch of the work. For its part, the pitch control grants you the power to raise or lower the melody by up to twelve exact semitones, processing the audio stream in the workshops of *ffmpeg* using the *rubberband* tool if it is available in your kingdom, or applying the clever trick of *asetrate* with *atempo* otherwise. Processed files are stored temporarily in a sunroom (cache) that is purged automatically as soon as the weight of the supplies exceeds 250 MB.

---

<a name="v-logistics-of-supplies-and-downloads"></a>
### 𝓥. 𝓛𝓸𝓰𝓲𝓼𝓽𝓲𝓬𝓼 𝓸𝓯 𝓢𝓾𝓹𝓹𝓵𝓲𝓮𝓼 𝓪𝓷𝓭 𝓓𝓸𝔀𝓷𝓵𝓸𝓪𝓭𝓼

Provisioning your personal coffers with the best works of the kingdom is as simple as pressing the **O** key for the song that is active, or the **W** key if you wish to capture the entire view of the current inventory. The files disembark safe and without mishaps in the system’s musical armory, converted to the universal MP3 format if *ffmpeg* is working in the workshops, or to M4A if tools are scarce. The artifact itself takes care of resolving the presence of *ffmpeg* by its own means, even if it finds itself in need of importing it from the distant warehouses of *imageio-ffmpeg*.

**Download armory path:**
```bash
~/Music/YTMUSIC_CMD
```

---

<a name="vi-the-main-screen-an-animated-stained-glass-window"></a>
### 𝓥𝓘. 𝓣𝓱𝓮 𝓜𝓪𝓲𝓷 𝓢𝓬𝓻𝓮𝓮𝓷: 𝓐𝓷 𝓐𝓷𝓲𝓶𝓪𝓽𝓮𝓭 𝓢𝓽𝓪𝓲𝓷𝓮𝓭-𝓖𝓵𝓪𝓼𝓼 𝓦𝓲𝓷𝓭𝓸𝔀

The home mode is not an inert list nor a cold index of parchments. It is **a fully animated Gothic stained-glass window with golden stars that twinkle and float slowly** across the length and breadth of the screen. Over this beautiful structure unfolds the organization of your entire fief: your saved lists, the songs of the last hours, the tunes most listened to by your lordship, your indisputable favorites, and the suggestions that the bard offers you based on your history and tastes. The covers of the songs are loaded in parallel execution threads, ensuring that the interface never stops or freezes waiting for responses from external networks.

---

<a name="vii-no-tributes-no-accounts-no-noise"></a>
### 𝓥𝓘𝓘. 𝓝𝓸 𝓣𝓻𝓲𝓫𝓾𝓽𝓮𝓼, 𝓝𝓸 𝓐𝓬𝓬𝓸𝓾𝓷𝓽𝓼, 𝓝𝓸 𝓝𝓸𝓲𝓼𝓮

In this territory there are no mandatory Google logins, nor the intricate OAuth protocols, nor foreign passwords (tokens) that compromise your sovereignty. The operating system user is the only lord, judge, and absolute sovereign of what happens. Everything is stored and protected within your own physical lands.

The artifact has the ability to install its own dependencies if it detects that any are missing in the workshops (*yt-dlp, python-vlc, pygame, pillow, numpy, imageio-ffmpeg*), restarting promptly after the first forging is completed. If the *VLC* environment is not found in the kingdom, the artifact will attempt to summon it immediately through the system’s official heralds (*winget, brew, apt, dnf, or pacman*), rigorously adapting to the laws and customs of the computer territory where it runs.

---

<a name="the-knights-shortcuts"></a>
## 𝕿𝖍𝖊 𝕶𝖓𝖎𝖌𝖍𝖙’𝖘 𝕾𝖍𝖔𝖗𝖙𝖈𝖚𝖙𝖘

| 𝕶𝖊𝖞 | 𝕮𝖔𝖓𝖏𝖚𝖗𝖊𝖉 𝕬𝖈𝖙𝖎𝖔𝖓 |
| :---: | :--- |
| **Space** | Pause the melody or resume the active song. |
| **N / P** | Advance swiftly to the next song or return to the previous one. |
| **+ / -** | Raise or lower the volume of the musical elixir. |
| **← / →** | Rewind or advance ten seconds in the time of the work. |
| **[ / ]** | Decrease or increase the speed of the musical gallop. |
| **, / .** | Lower or raise the pitch by one exact semitone. |
| **S / R** | Toggle shuffle and repeat the song. |
| **F** | Mark the work as favorite within your coffers. |
| **G** | Save the current list in the profile’s parchment. |
| **Y** | Synchronize all saved lists throughout the kingdom. |
| **I** | Return immediately home (the animated stained-glass window). |
| **L** | Display before your eyes the great library. |
| **/** | Invoke the sharp search engine. |
| **Q** | Close the artifact, disarm the workshops, and leave in peace. |

---


