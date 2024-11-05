# 英雄联盟电竞赛事直播手册（不含国服）

## 前言
在不久前的Discord服务器LOL比赛中，我独自负责了整个赛事的直播工作，从赛前准备到比赛中的内容呈现，再到赛后的收尾，每个环节都顺利完成，最终将整场直播流畅地呈现给了观众。

为了让之后的直播工作能有一个参考，我整理了这份直播工作复盘，分享了直播过程中的关键思路、操作要点，以及一些实用的资源工具。希望这份指南可以为LOL赛事直播感兴趣的人提供帮助。

## 导播思路

直播过程中，导播（直播员）的核心任务是确保观众能够实时、清晰地看到比赛的关键场面，在合理的限度内为观众呈现当前比赛的各项数据信息，同时保持直播的流畅度和专业性。以下是各阶段的导播思路及操作要点：

1. **赛前准备**
   - **场景设置**：提前在 OBS 中创建不同的场景，以便在比赛的不同阶段快速切换。比如 Warm Up（准备阶段）、Banpick、In-game、After-game（赛后）等场景。将所需的音频、视频、图片、文本等元素添加到各个场景中，并使用颜色标签进行区分，确保每个场景的构成符合直播需求，以及能够快速应对呈现内容的更改以及故障的排除。
   - **音频调控**：使用 VB-Cable 进行多路音频输出，确保解说、游戏声音和背景音乐分开调控，方便在不同场景间进行切换。特别是在 Banpick 和 In-game 阶段，需要将音效以及背景音乐响度控制得当，以保证观众体验。
   - **画面布局**：对直播 UI 进行布局，包括计分板、英雄状态、比赛信息等重要元素，确保各元素可清晰展示给观众。

2. **比赛开始（Banpick 阶段）**
   - **BP 画面切换**：在 Banpick 阶段使用 League Observer Tool 的 Banpick 组件或网页 Banpick 工具，将 BP 画面呈现给观众。同时，通过音频管理，播放背景音乐，保持轻松氛围。
   - **解说互动**：此阶段通常有解说对各队伍的阵容选择进行分析。确保音频来源切换到解说音频，并尽量保持 BP 信息的清晰呈现。

3. **比赛进行中（In-game 阶段）**
   - **关键画面捕捉**：创建多个 In-game 场景，以应对正常OB、团战视角、高光回放等不同情况。使用 League Observer Tool 提供的 In-game 组件实时捕捉游戏内的关键事件（如团战、塔下击杀等），及时切换到对应场景。
   - **多视角切换**：导播需要密切关注场上动态，必要时快速切换镜头，将比赛中的亮点呈现出来。可以利用快捷键设备（如 Stream Deck）辅助场景切换。
   - **音频同步**：确保游戏音效与解说音频同步，并调节背景音乐音量，以避免干扰解说。通过 OBS 的音频混合器及时调整音量，保持现场氛围。

4. **比赛结束（After-game 阶段）**
   - **赛后画面展示**：比赛结束后，切换到 After-game 场景，展示比赛结果、选手数据和赛后面板。可以使用 League Observer Tool 提供的赛后组件直观呈现比赛数据。
   - **解说分析**：此阶段通常会有解说对比赛进行总结分析，确保解说音频清晰，同时适当播放轻松的背景音乐。

5. **场间休息（Interlude）**
   - **信息展示**：在场间休息期间，可以展示比分、下一场比赛的时间和参赛队伍等信息，通过浏览器源加入场间倒计时工具，确保观众清楚下一场比赛的时间。
   - **轻松氛围**：播放适当的背景音乐（如 Riot 官方的 Creator-Safe 播放列表），维持观众的观看体验。

### 关于多路视角以及高光回放
在直播员人数足够，以及网络条件允许的情况下，可以通过线上会议软件以及语音服务进行多路视角OB，并使用官方OB工具进行运镜式的高管回放。或者可以通过采集卡联动多台本地设备进行多视角OB呈现。

## In-game 观赛 UI 设计数据

### 观赛 UI 布局

![观赛 UI 图纸](/assets/stream_ui.png)

### 英雄状态占位

[PNG 下载](/assets/champion-status-placeholder.png)

### 计分板占位

[PNG 下载](/assets/scoreboard-placeholder.png)

### 小地图占位

[PNG 下载](/assets/minimap-placeholder.png)


## 直播工具链

### OBS Studio

OBS Studio 是一款开源的直播工具，支持快速开启直播并推送直播内容。

[下载地址](https://obsproject.com/)

### League Prod Toolkit

用于英雄联盟电竞直播的 OBS 工具包，提供赛前 BP（Ban & Pick），游戏内事件，赛后面板等功能。

[Github 页面](https://github.com/RCVolus/league-prod-toolkit)

### League Observer Tool

League Prod Toolkit 的本地 OB 工具，用于与 League Prod Toolkit 的 LCU 端点通信，支持游戏内事件监测。

[Github 页面](https://github.com/RCVolus/league-observer-tool)

### Creator Suite Replay / League Director

用于英雄联盟比赛回放的镜头工具，可用于比赛前的空镜头拍摄和赛后高光拍摄。Creator Suite Replay 由 SkinSpotlights 开发，League Director 由英雄联盟官方开发（推荐使用）。

[Creator Suite Replay 下载](https://github.com/SkinSpotlights/CreatorSuite-ReplayAPI/releases)

[League Director 下载](https://github.com/RiotGames/leaguedirector)

### 网页 Banpick 工具

[PentaQ Web BP Tool](https://data.pentaq.com/bp)

### Photoshop（可选）

Adobe Photoshop 是一款图像处理软件，可用于快速制作直播内容。

[下载地址](https://www.adobe.com/cn/products/photoshop.html)

### VB-Cable（可选）

VB-Cable 是一款虚拟音频设备软件，可用于直播中的多路音频输入输出和控制。

[下载地址](https://vb-audio.com/Cable/)

### ReplayBook（可选）

ReplayBook 是一款开源软件，用于查看英雄联盟比赛 Replay（.rofl）文件，可用于赛后高光制作。

[Github 页面](https://github.com/fraxiinus/ReplayBook)

### Riot LOL Creator-Safe 播放列表

Riot 官方提供的创作者安全音乐播放列表，可用于直播音乐播放。

[Spotify Creator-Safe 播放列表](https://open.spotify.com/playlist/5hDYD44imzFZEqTfAoco1N?si=Ik6B1FizS4ewpPlwAxawtQ)

[SoundCloud Creator-Safe 播放列表](https://soundcloud.com/leagueoflegends/sets/riot-games-creator-safe)

### League of Legends Data Dragon（可选）

英雄联盟官方的资料包，包含英雄、物品、阵容及相关插图等资料。

[LOL Data Dragon](https://developer.riotgames.com/docs/lol#data-dragon)

### Stream Deck（可选）

用于直播的可编程快捷键设备，支持快速场景切换及 OB 视角切换。


## OBS 相关设置

参考自 [Meta Business 帮助中心](https://zh-cn.facebook.com/business/help/1968707740106188?id=648321075955172)

### 推流设置

为确保内容安全并满足游戏内 OB 工具的要求，建议以 1080p@60fps 格式推流。

OBS Studio 推流配置流程：

1. 在 OBS 中点击 **Settings（设置）**。
2. 点击 **Output（输出）**。
3. 在 **Output Mode（输出模式）** 下拉菜单中选择 **Advanced（高级）**。
4. 在 **Encoder（编码器）** 下拉菜单中选择 **H264 视频编码器**。
5. 测试网络上传速度（如使用 [Speedtest](http://www.speedtest.net/)）。
6. 计算上传速度的 80%，并将此值作为 **Bitrate（比特率）**。推荐比特率为 7500 Kbps 至 8500 Kbps（7.5 至 8.5 Mbps）。
7. 确保 **Keyframe Interval（关键帧间隔）** 设置为 2。
8. 返回 **Settings（设置）**。
9. 点击 **Video（视频）**。
10. 设置分辨率为 1080p（1920 x 1080），帧率为 60。

### 场景及内容设置

建议标准化直播流程，并为直播的各个阶段（BP、比赛中、赛后等）创建单独的场景，便于内容控制。

#### 场景创建

1. 在 OBS 中右键点击 **Scenes（场景）框**。
2. 选择 **Add（添加）**。
3. 命名场景。
4. 点击 **OK（确定）**。
5. 可创建多个场景，并在直播期间自由切换。

### 为每个场景配置内容来源

建议使用 **VB-Cable** 实现多路音频输出，便于隔离不同的音频信号源（如背景音乐、游戏音效、解说等）。使用 OBS Studio 自带的**颜色标记**功能区分内容来源，以便更好地控制直播内容并应对突发情况。

#### Warm Up

1. 图像源（比赛海报及参赛队伍 logo 等）
2. 文本源（比赛名称、参赛队伍名称等）
3. 音频输出源（背景音乐）
4. 音频输入源（解说）

#### Banpick

1. 浏览器源（League Observer Tool 的 BP 组件或网页 BP 工具）
2. 图像源（比赛海报及参赛队伍 logo 等）
3. 文本源（比赛名称、参赛队伍名称等）
4. 音频输出源（游戏声音、背景音乐）
5. 音频输入源（解说）

#### In-game

建议创建多个场景应对不同比赛情况（如正常、团战、高光回放等）。

1. 浏览器源（League Observer Tool 的 In-game 组件）
2. 图像源（观赛浮层界面）
3. 音频输出源（游戏声音）
4. 音频输入源（解说）

#### After-game

1. 浏览器源（League Observer Tool 的赛后组件）
2. 文本源（比赛名称、参赛队伍名称等）
3. 图像源（比赛海报及参赛队伍 logo 等）
4. 音频输出源（背景音乐）
5. 音频输入源（解说）

#### Interlude（幕间）

1. 文本源（比赛名称、参赛队伍名称及比分等）
2. 浏览器源（场间倒计时工具）
3. 图像源（比赛海报及参赛队伍 logo 等）
4. 音频输出源（背景音乐）