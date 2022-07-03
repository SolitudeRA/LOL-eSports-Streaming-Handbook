# リーグ・オブ・レジェンド eスポーツ配信手帳

## In-game e-スポーツUIデザインデータ

### eスポーツUI Layout

![观赛UI图纸](../assets/stream_ui.png)

## 配信ツールチェーン

### OBS

OBS Studioはビデオ録画と生放送用の無料でオープンソースのソフトウェアである。

[Download](https://obsproject.com/)

### League prod toolkit

League prod toolkitはLOLeスポーツ配信用のオープンソースオーバーレイツールである、試合前BP、試合中のイベント、試合終了時のデータなどを提供できる。

[Github Page](https://github.com/RCVolus/league-prod-toolkit)

### League observer tool

League prod toolkitの副属ツールであり、LCU Endpointを通じでLeague prod toolkitと連携し、試合中のイベントを取得できる。

[Github Page](https://github.com/RCVolus/league-observer-tool)

### Creator Suite Replay / League Director

LOL試合リプレイでカメラを自由的移動できるツールである、

[Creator Suite Replay](https://github.com/SkinSpotlights/CreatorSuite-ReplayAPI/releases)

[League Director](https://github.com/RiotGames/leaguedirector)

### Web Banpick tool

ウェブサイトでBanpickできるツールである。

[PentaQ Web BP Tool](https://data.pentaq.com/bp)

### Photoshop(選択)

画像編集ツールである、トーナメントポースタなどの加工・色の調整をしたり、デザインを作ったり、こだわりの画像を作ることができる。

[Download](https://www.adobe.com/cn/products/photoshop.html)

### VB-Cable(選択)

VB-Cableは、複数のオーディオラインを同時に操作するための仮想オーディオデバイスである。

[Download](https://vb-audio.com/Cable/)

### ReplayBook(選択)

ReplayBookは、試合終了後のリプレイを管理するためのオープンソースのツールである。

[Github Page](https://github.com/fraxiinus/ReplayBook)

### Riot LOL Creator-Safe Playlist(選択)

Riot公式サイトで提供されている、Creator-Safe　BGMプレイリストである。

[Spotify Creator-Safe Playlist](https://open.spotify.com/playlist/5hDYD44imzFZEqTfAoco1N?si=Ik6B1FizS4ewpPlwAxawtQ)

[SoundCloud Creator-Safe Playlist](https://soundcloud.com/leagueoflegends/sets/riot-games-creator-safe)

### League of Legends Data Dragon(選択)

League of Legends Data Dragonは、League of Legendsのゲーム自体の画像などのアセットを提供しているウェブサイトである。

[LOL Data Dragon](https://developer.riotgames.com/docs/lol#data-dragon)

### Stream Deck(選択)

Stream Deckは、配信者向けのカスタム可能なLCDキーを搭載したライブコンテンツ作成コントローラである。

## OBS設定

### 配信設定

[Metaビジネスヘルプセンター](https://ja-jp.facebook.com/business/help/1968707740106188?id=648321075955172)を参照した。

1. OBSで<b>[設定]</b>をクリックします。
2. <b>[出力]</b>をクリックします。
3. [出力モード]のドロップダウンで<b>[詳細]</b>を選択します。
4. [エンコーダー]のドロップダウンで**H264の動画エンコーダー**を選択します。
5. [アップロード速度](http://www.speedtest.net/)を測定します。
6. アップロード速度から20%を差し引いた数値を<b>[ビットレート]</b>に入力します。推奨ビットレートは7500〜8500 Kbps(7.5〜8.5 Mbps)です。
7. **キーフレーム間隔**が2に設定されていることを確認します。
8. <b>[設定]</b>をクリックします。
9. <b>[動画]</b>をクリックします。
10. 希望の解像度を設定します。対応している解像度は、1秒当たり60フレームで最大1080ピクセル(1920 x 1080)です。

### シーンとコンテンツの設定

ライブ配信の手順を標準化して、Banpick、試合中、試合終了時のシーンを分けて設定するとは極めて推奨する。

シーンを作成する。

1. OBSの<b>[シーン]</b>ボックスで右クリックします。
2. <b>[追加]</b>を選択します。
3. シーンに名前を付けます。
4. <b>[OK]</b>をクリックします。
5. 複数のシーンを作成し、ストリーミング中にシーンを切り替えることができます。

### 各シーンのソースを設定する

**VB-Cable**使用して、配信のオーディオを分けてコントロールするのは極めて推奨する。

OBSの**カラー**機能を使用して、配信中の各ソースを見やすく設定するのは極めて推奨する。

#### Warm up

1. 画像(試合ポスター, チームロゴ など)
2. テキスト(試合タイトル，チーム名 など)
3. 音声出力キャプチャ(BGM)
4. 音声入力キャプチャ(ゲスト)

#### Banpick

1. ブラウザ(League observer banpick tool 又は web banpick tools)
2. 画像(試合ポスター, チームロゴ など)
3. テキスト(試合タイトル，チーム名 など)
4. 音声出力キャプチャ(ゲームサウンド)
5. 音声出力キャプチャ(BGM)
6. 音声入力キャプチャ(ゲスト)

#### 試合中

試合中の各状況（普通、集団戦、ハイライトなど）に対して、シーンを設定するのは推奨する。

1. ブラウザ(League observer In-game tool)
2. 画像(UI Layout)
3. 音声出力キャプチャゲームサウンド)
4. 音声入力キャプチャ(ゲスト)

#### 試合終了

1. ブラウザ(League observer after match tool)
2. テキスト(試合タイトル，チーム名 など)
3. 画像(試合ポスター, チームロゴ など)
4. 音声出力キャプチャ(BGM)
5. 音声入力キャプチャ(ゲスト)

#### 幕間

1. テキスト(試合タイトル，チーム名、チームスコア など)
2. ブラウザ(幕間カウントダウンツール)
3. 画像(試合ポスター, チームロゴ など)
4. 音声出力キャプチャ(BGM)