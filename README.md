# 英雄联盟电竞赛事直播指南<br>League of Legends e-sports Streaming Guideline<br> リーグ・オブ・レジェンド eスポーツ配信ガイドライン

[<img src='https://img.shields.io/badge/中文版-点击这里-brightgreen' alt='CI/CD'></img>](/l18n/README_ZH.md)

[<img src='https://img.shields.io/badge/日本語版-こちら-orange' alt='Github'></img>](/l18n/README_JA.md)

## Introduction

Recently, I was responsible for the entire live streaming process of a League of Legends event on a Discord server. From pre-match preparation to in-game content presentation, and finally to post-game wrap-up, I handled every phase and successfully provided a smooth live viewing experience for the audience.

To help with future live streams, I’ve compiled this guide as a reference, sharing key thoughts, operational points, and useful tools that can streamline the process. I hope this guide will be a helpful resource for those interested in League of Legends event streaming.

## Director's Workflow

During the broadcast, the primary task of the director (streamer) is to ensure that viewers can see all the crucial moments in real-time with clear, relevant game data while maintaining a smooth and professional flow. Here’s a breakdown of the director’s workflow and essential points at each stage:

1. **Pre-Match Preparation**
   - **Scene Setup**: Set up different scenes in OBS ahead of time to quickly switch between different stages of the event, such as Warm-Up, Banpick, In-game, and After-game. Add necessary audio, video, images, text, and use color tags to distinguish each scene, ensuring each layout meets streaming needs and allows for quick adjustments in case of issues.
   - **Audio Control**: Use VB-Cable to manage multi-channel audio output, separating commentary, game sounds, and background music. This setup allows for easy adjustments during scene transitions. Especially in the Banpick and In-game phases, make sure sound levels are appropriate to enhance the viewer experience.
   - **UI Layout**: Organize the streaming UI, including the scoreboard, champion status, and other match information, to ensure clarity for the audience.

2. **Match Start (Banpick Phase)**
   - **BP Screen Switching**: Use the Banpick component from League Observer Tool or a web-based Banpick tool to display the BP screen for viewers. Manage audio to include background music, keeping the atmosphere light and engaging.
   - **Commentary Interaction**: During this phase, commentators typically analyze team compositions. Ensure the audio source is switched to commentary and maintain clear BP information display.

3. **In-game Phase**
   - **Key Moments Capture**: Set up multiple In-game scenes to handle different scenarios such as standard OB, teamfight view, and highlight replays. Use the In-game component from League Observer Tool to capture key events (e.g., teamfights, tower dives), switching to the appropriate scene as needed.
   - **Multi-perspective Switching**: Stay attentive to game developments and quickly switch perspectives to showcase highlights. Stream Deck or similar tools can assist in swift scene changes.
   - **Audio Sync**: Ensure game sounds sync with commentary audio and adjust background music volume to avoid overshadowing commentary. Use OBS’s audio mixer to manage levels, keeping the atmosphere immersive.

4. **Post-match (After-game Phase)**
   - **Post-game Screen**: After the match, switch to the After-game scene to display match results, player stats, and post-game panels. Use the League Observer Tool’s post-game component for a clear, data-driven display.
   - **Commentary Analysis**: Commentators usually provide a match recap during this phase; ensure clear commentary audio and play light background music to maintain a relaxed atmosphere.

5. **Interlude (Between Matches)**
   - **Information Display**: Between matches, show scores, upcoming match times, and participating teams. Add a countdown timer via browser source to keep viewers informed about the next match’s timing.
   - **Atmosphere Management**: Play appropriate background music (such as Riot’s Creator-Safe playlists) to maintain a comfortable viewing experience.

### Multi-view Setup and Highlight Replays

If there are enough staff and the network allows, you can use online conferencing and voice services for multi-view OB or use the official OB tool to create cinematic highlight replays. Alternatively, capture cards and multiple local devices can be linked for multi-view OB display.

## In-game Viewer UI Design Data

### Viewer UI Layout

![Viewer UI Layout](../assets/stream_ui.png)

### Champion Status Placeholder

[Download PNG](../assets/champion-status-placeholder.png)

### Scoreboard Placeholder

[Download PNG](../assets/scoreboard-placeholder.png)

### Minimap Placeholder

[Download PNG](../assets/minimap-placeholder.png)


## Streaming Toolkit

### OBS Studio

OBS Studio is an open-source streaming tool, supporting quick setup and streaming.

[Download](https://obsproject.com/)

### League Prod Toolkit

A toolkit for League of Legends esports broadcasting with OBS, providing pre-game BP, in-game events, and post-game panels.

[GitHub Page](https://github.com/RCVolus/league-prod-toolkit)

### League Observer Tool

A local OB tool for League Prod Toolkit that communicates with the LCU endpoint to monitor in-game events.

[GitHub Page](https://github.com/RCVolus/league-observer-tool)

### Creator Suite Replay / League Director

A tool for match replay camera management in League of Legends, used for pre-game scenery shots and highlight capture. Creator Suite Replay is developed by SkinSpotlights, while League Director is officially developed by Riot (recommended).

[Creator Suite Replay Download](https://github.com/SkinSpotlights/CreatorSuite-ReplayAPI/releases)

[League Director Download](https://github.com/RiotGames/leaguedirector)

### Web-based Banpick Tool

[PentaQ Web BP Tool](https://data.pentaq.com/bp)

### Photoshop (Optional)

Adobe Photoshop is an image editing software, useful for quickly creating streaming assets.

[Download](https://www.adobe.com/cn/products/photoshop.html)

### VB-Cable (Optional)

VB-Cable is a virtual audio device software, useful for managing multi-channel audio input/output during streaming.

[Download](https://vb-audio.com/Cable/)

### ReplayBook (Optional)

ReplayBook is an open-source tool for viewing League of Legends match replays (.rofl files) and is suitable for highlight creation.

[GitHub Page](https://github.com/fraxiinus/ReplayBook)

### Riot LOL Creator-Safe Playlist

A creator-safe music playlist by Riot, available for streaming background music.

[Spotify Creator-Safe Playlist](https://open.spotify.com/playlist/5hDYD44imzFZEqTfAoco1N?si=Ik6B1FizS4ewpPlwAxawtQ)

[SoundCloud Creator-Safe Playlist](https://soundcloud.com/leagueoflegends/sets/riot-games-creator-safe)

### League of Legends Data Dragon (Optional)

An official League of Legends data pack containing champion data, item data, and related illustrations.

[LOL Data Dragon](https://developer.riotgames.com/docs/lol#data-dragon)

### Stream Deck (Optional)

A programmable quick-access device for streaming, supporting rapid scene switching and OB perspective changes.


## OBS Setup

Based on [Meta Business Help Center](https://zh-cn.facebook.com/business/help/1968707740106188?id=648321075955172)

### Streaming Settings

To ensure security and meet in-game OB tool requirements, a streaming format of 1080p@60fps is recommended.

OBS Studio streaming configuration:

1. In OBS, click **Settings**.
2. Go to **Output**.
3. In the **Output Mode** dropdown menu, select **Advanced**.
4. In the **Encoder** dropdown menu, select **H264 Video Encoder**.
5. Test your upload speed (e.g., via [Speedtest](http://www.speedtest.net/)).
6. Use 80% of the upload speed as the **Bitrate**. Recommended bitrate is 7500-8500 Kbps (7.5 to 8.5 Mbps).
7. Set **Keyframe Interval** to 2.
8. Go back to **Settings**.
9. Go to **Video**.
10. Set the resolution to 1080p (1920 x 1080) and frame rate to 60.

### Scene and Content Setup

It is recommended to standardize the streaming process by creating separate scenes for each streaming phase (BP, in-game, post-game, etc.) for easier content control.

#### Scene Creation

1. In OBS, right-click the **Scenes** box.
2. Select **Add**.
3. Name the scene.
4. Click **OK**.
5. Multiple scenes can be created and freely switched during streaming.

### Configure Content Sources for Each Scene

Use **VB-Cable** for multi-channel audio output, isolating audio sources such as background music, game sound effects, and commentary. Use OBS Studio’s **color tag** feature to differentiate content sources, allowing for easier content management and faster troubleshooting during unexpected events.

#### Warm Up

1. Image source (match poster, team logos, etc.)
2. Text source (match name, team names, etc.)
3. Audio output source (background music)
4. Audio input source (commentary)

#### Banpick

1. Browser source (Banpick component of League Observer Tool or web-based BP tool)
2. Image source (match poster, team logos, etc.)
3. Text source (match name, team names, etc.)
4. Audio output sources (game sound, background music)
5. Audio input source (commentary)

#### In-game

Create multiple scenes to address different match scenarios (standard, teamfight, highlight replay).

1. Browser source (In-game component of League Observer Tool)
2. Image source (viewing interface overlay)
3. Audio output source (game sound)
4. Audio input source (commentary)

#### After-game

1. Browser source (post-game component of League Observer Tool)
2. Text source (match name, team names, etc.)
3. Image source (match poster,

 team logos, etc.)
4. Audio output source (background music)
5. Audio input source (commentary)

#### Interlude

1. Text source (match name, team names, score, etc.)
2. Browser source (break countdown tool)
3. Image source (match poster, team logos, etc.)
4. Audio output source (background music) 

This setup will help you smoothly control content presentation at each stage of the match.