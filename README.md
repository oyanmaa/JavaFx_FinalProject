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
src/main/
├── resources/com/example/vtsapp/ (FXMLファイル)
│   ├── login-view.fxml          <-- [画面1] 接続・ログイン画面
│   ├── home-view.fxml           <-- [画面2] メインのホーム画面（ベース枠）
│   ├── emotion.fxml             <-- [子画面] 表情操作パネル
│   ├── clothes.fxml             <-- [子画面] 衣装操作パネル
│   └── accessories.fxml         <-- [子画面] アクセサリー操作パネル
│
└── java/com/example/vtsapp/      (Javaファイル)
    ├── HelloApplication.java    <-- アプリ起動
    ├── VTSClient.java           <-- VTSとのWebSocket通信クラス（接続を維持）
    │
    ├── LoginController.java     <-- login-view.fxml の制御（接続成功でhomeへ遷移）
    ├── HomeController.java      <-- home-view.fxml の制御（ナビゲーションや共通枠）
    ├── EmotionController.java   <-- emotion.fxml の制御（表情ボタン処理）
    ├── ClothesController.java   <-- clothes.fxml の制御（衣装ボタン処理）
    └── AccessoriesController.java <-- accessories.fxml の制御（小物ボタン処理）
## 外部リンク
[Vtube Stadioとは](https://denchisoft.com/)
