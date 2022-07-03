# League of Legends e-sports streaming handbook<br> 英雄联盟电竞直播手册<br> リーグ・オブ・レジェンド eスポーツ配信手帳

[<img src='https://img.shields.io/badge/中文版-点击这里-brightgreen' alt='CI/CD'></img>](/l18n/README_ZH.md)

[<img src='https://img.shields.io/badge/日本語版-こちら-orange' alt='Github'></img>](/l18n/README_JA.md)

## In-game e-sports UI design data

### e-sports UI Layout

![e-sports UI design](/assets/stream_ui.png)

## Streaming toolchain

### OBS

OBS Studio is a free open-source software that allows you to stream your game to a live stream.

[Download](https://obsproject.com/)

### League prod toolkit

Toolkit for League Productions with overlays for champion select, in-game events, end of game stats, and more.

[Github Page](https://github.com/RCVolus/league-prod-toolkit)

### League observer tool

An addition to the league-prod-toolkit for the observer PC.

[Github Page](https://github.com/RCVolus/league-observer-tool)

### Creator Suite Replay / League Director

Tools for staging and recording videos from League of Legends replays. You can use them for shooting scenery shot before the match begins or highlights in game. Creator Suite Replay is developed by SkinSpotlights(recommend)，League Director is developed by Riot.

[Creator Suite Replay](https://github.com/SkinSpotlights/CreatorSuite-ReplayAPI/releases)

[League Director](https://github.com/RiotGames/leaguedirector)

### Web Banpick tool

[PentaQ Web BP Tool](https://data.pentaq.com/bp)

### Photoshop(optional)

Adobe Photoshop is a software that can be used to edit images for image assets.

[Download](https://www.adobe.com/cn/products/photoshop.html)

### VB-Cable(optional)

VB-Cable is a virtual audio device working as virtual audio cable. You can use it to control multiple audio lines separately in the same time.

[Download](https://vb-audio.com/Cable/)

### ReplayBook(optional)

ReplayBook is a free open-source tool that helps you organize and manage your downloaded replay files, you can use it to make highlights after the match ends.

[Github Page](https://github.com/fraxiinus/ReplayBook)

### Riot LOL Creator-Safe Playlist(optional)

Creator-Safe Playlist from Riot, you can use it for streaming BGM.

[Spotify Creator-Safe Playlist](https://open.spotify.com/playlist/5hDYD44imzFZEqTfAoco1N?si=Ik6B1FizS4ewpPlwAxawtQ)

[SoundCloud Creator-Safe Playlist](https://soundcloud.com/leagueoflegends/sets/riot-games-creator-safe)

### League of Legends Data Dragon(optional)

Data Dragon is our way of centralizing League of Legends game data and assets, including champions, items, runes, summoner spells, and profile icons. All of which can be used by third-party developers.

[LOL Data Dragon](https://developer.riotgames.com/docs/lol#data-dragon)

### Stream Deck(optional)

A macro key device with LCD screen，you can use it for fast scene switching and ob view changing.


## OBS Settings

Reference from[Meta Business Help Centre](https://en-gb.facebook.com/business/help/1968707740106188?id=648321075955172)

### Streaming settings

Because of content safety and in-game ob tool's setting，it's highly recommended that streaming in 1080p@60fps.

OBS Studio streaming setting steps：

1. Click **Settings** in OBS.
2. Click **Output**.
3. Select **Advanced** in the Output mode drop-down menu.
4. Select an **H264 video encoder** in the Encoder drop-down menu.
5. Determine your [upload speed](http://www.speedtest.net/).
6. Subtract 20 per cent from your upload speed and enter that number in **Bitrate**. The recommended bitrate is 7,500 Kbps to 8,500 Kbps (7.5 to 8.5 Mbps).
7. Make sure that the **Keyframe interval** is set to 2.
8. Click **Video**.
9. Set your desired **Resolution**: recommended resolution is 1080p (1920 x 1080) at 60 frames per second.

### Scene and content settings

It's highly recommended that standardize your streaming procedure，for each streaming scene（Banpick，In-game，After-match etc.）, you should set obs scene separately for better streaming experience.

Create a scene.

1. Right-click the **Scenes** box in OBS.
2. Select **Add**.
3. Name your scene.
4. Click **OK**.
5. You can create multiple scenes and switch between them during your stream.

### Setup sources for each scene

It's highly recommended that using **VB-Cable** to control audio signals separately in the same time.

It's highly recommended that using **Set color** in obs to mark different sources for better control of your streaming content.

#### Warm up

1. Image(Match poster, team logo etc.)
2. Text(Match title，team name etc.)
3. Audio output capture(BGM)
4. Audio input capture(Guest)

#### Banpick

1. Browser(League observer banpick tool or web banpick tools)
2. Image(Match poster, team logo etc.)
3. Text(Match title，team name etc.)
4. Audio output capture(Game sound)
5. Audio output capture(BGM)
6. Audio input capture(Guest)

#### In-game

It's recommended that create several scene for each condition(normal, team fight, highlight etc.).

1. Browser(League observer In-game tool)
2. Image(UI Layout)
3. Audio output capture(Game sound)
4. Audio input capture(Guest)

#### After-game

1. Browser(League observer after match tool)
2. Text(Match title，team name etc.)
3. Image(Match poster, team logo etc.)
4. Audio output capture(BGM)
5. Audio input capture(Guest)

#### Interlude

1. Text(Match title，team name, team score etc.)
2. Browser(Interlude countdown tool)
3. Image(Match poster, team logo etc.)
4. Audio output capture(BGM)




