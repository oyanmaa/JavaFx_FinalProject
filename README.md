# JavaFX アプリ開発
### プロジェクト名：FinalProject
## 概要
steam版のVtube StadioをJavaFX側で操作、管理できるようにする
## 🛠開発環境・技術スタック
| 分類 | 技術 / ツール | バージョン |
| :--- | :--- | :--- |
| **言語** | Java | 25 |
| **ビルドツール** | Apache Maven | - |
| **GUI フレームワーク** | JavaFX | 17.0.6 |
| **UI 拡張ライブラリ** | ControlsFX | 11.2.1 |
| **テストフレームワーク** | JUnit | 5.10.2 |
## 手順
1. steam版のVtube Stadioのapiを利用する
2. JavaFX側のGUIでVtube Stadioを操作する
3. JavaFX側での操作をVtube Stadioに反映させる
## 機能
#### 対応しているVtuberのモデルの衣装や表情をJavaFX側で操作できる
- モデルの衣装を着脱できる
- モデルの表情をチェンジできる
- モデルの小物(アクセサリーの着脱ができる)
## 検証
Vtube StadioとJavaFXの両方を立ち上げて確認する
## ファイル構成
## ディレクトリ構成 (Directory Structure)

```text
.
├── src/
│   └── main/
│       ├── java/
│       │   └── com/example/vtsapp/
│       │       ├── HelloApplication.java      # アプリケーション起動エントリポイント (Main)
│       │       ├── VTSClient.java             # VTube StudioとのWebSocket通信・認証管理 (共通)
│       │       │
│       │       ├── LoginController.java        # 接続・ログイン画面の制御 Controller
│       │       ├── HomeController.java         # メインホーム画面（全体フレーム・ナビゲーション）Controller
│       │       │
│       │       ├── EmotionController.java      # [カテゴリ] 表情切り替え操作用 Controller
│       │       ├── ClothesController.java      # [カテゴリ] 衣装切り替え操作用 Controller
│       │       └── AccessoriesController.java  # [カテゴリ] アクセサリー・小物着脱操作用 Controller
│       │
│       └── resources/
│           └── com/example/vtsapp/
│               ├── login-view.fxml             # 接続・ポート指定・ログイン画面レイアウト
│               ├── home-view.fxml              # メインホーム画面（全体フレーム・ヘッダー/フッター）レイアウト
│               │
│               ├── emotion.fxml                # 表情操作パネル用レイアウト
│               ├── clothes.fxml                # 衣装操作パネル用レイアウト
│               ├── accessories.fxml            # アクセサリー・小物操作パネル用レイアウト
│               │
│               └── img/                        # アプリ内で使用する静的画像リソース
│                   └── icon.png
│
├── pom.xml                                     # Maven依存関係設定 (JavaFX, Gson, WebSocket等)
└── README.md                                   # プロジェクトドキュメント
## 外部リンク
[Vtube Stadioとは](https://denchisoft.com/)
