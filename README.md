
**一芸入魂 (Ichigei Nyukon)**

「才能、解き放つ。」 あなたの「一芸」が誰かの「学び」になる。オンライン特化型のスキルシェアリング・プラットフォーム。

🚀 サービス概要

「一芸入魂」は、ニッチな特技からプロレベルのスキルまで、誰もが簡単に講師として教え、受講者として学べるマンツーマン・スキルシェアアプリです。

煩雑な日程調整や連絡を一つのアプリで完結させ、学びの体験を最大化します。

✨ 主要機能

1. 講師向け機能

スキルの多階層登録: カテゴリ（IT、ビジネス、ライフスタイル等）を選択し、詳細なスキル内容、料金、時間を登録。

柔軟な開催日程管理: 自分の空き時間をスロット（1時間単位など）として登録・管理可能。

マイスキル管理: 自分が提供しているスキルの編集や、予約状況の把握。

2. 受講者向け機能

高度なスキル検索: キーワード検索、多階層カテゴリフィルター、新着順・タイトル順のソート機能を搭載。

ワンタップ予約: 講師の空きスロットから希望日時を選び、即時に予約確定（Firestoreトランザクションによる在庫管理）。

マイ予約管理: 自分が申し込んだ予約を「確定済み」「完了」などのステータス別に管理。

3. コミュニケーション機能

リアルタイムチャット: Firebase Firestoreを活用した低遅延チャット。

マルチメディア共有: 画像やドキュメントをチャット内で送受信可能（Firebase Storage連携）。

ビデオ通話連携: チャット画面からワンタップでGoogle Meetを開始。

プライバシー保護: レッスン完了時にチャット履歴を自動削除するクリーンアップ機能。

🛠 技術スタック

カテゴリ

技術

Frontend

React Native (Expo), TypeScript

Backend (BaaS)

Google Firebase (Auth, Firestore, Storage)

Infrastructure

Firebase Hosting (Web版デプロイ)

Navigation

React Navigation (Stack)

UI Components

Expo Vector Icons (Material Community Icons)

Media Handling

Expo ImagePicker, DocumentPicker

📂 ディレクトリ構造

src/
├── components/     # 再利用可能な共通UIコンポーネント<br>
├── screens/        # 各画面コンポーネント<br>
│   ├── LoginScreen.tsx<br>
│   ├── SkillListScreen.tsx<br>
│   ├── BookingScreen.tsx<br>
│   ├── ChatScreen.tsx<br>
│   ├── InstructorAvailabilityScreen.tsx<br>
│   └── ...<br
├── config/         # Firebase設定 (firebaseConfig.ts)<br>
├── hooks/          # カスタムフック<br>
└── types/          # TypeScript 型定義<br>


⚙️ セットアップ・起動方法

1. リポジトリをクローン

git clone <repository-url>
cd MySkillApp


2. 依存関係のインストール

npm install


3. Firebaseの設定

src/config/firebaseConfig.ts を作成し、ご自身のFirebaseプロジェクトのSDK設定を貼り付けてください。

4. アプリケーションの起動

npx expo start


📈 技術的なこだわり

データの整合性: 予約処理に runTransaction を使用し、同一スロットへの同時予約（ダブルブッキング）を厳密に防止。

リアルタイム性: onSnapshot リスナーを多用し、チャットや予約ステータスの変更をリロードなしで反映。

クロスプラットフォーム: Webとネイティブ両方のファイル選択（Image/Document Picker）に対応。

© 2026 一芸入魂 開発チーム
