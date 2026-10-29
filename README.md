<p align="center">
  <img src="frontend/public/images/logo-sudachi.png" alt="sudachi" width="240">
</p>

<p align="center">
  <b>気軽に学習を共有し、同じ目標を持つ仲間とつながれる IT特化型SNS</b>
</p>

<p align="center">
  開発: チームうれし涙
</p>

## 概要

sudachi は、プログラミング初学者向けの IT特化型SNS です。日々の学習内容を気軽に投稿でき、同じ目標を持つ仲間を見つけて一緒に開発を始められます。

## 発表資料
[発表スライドはこちら](https://docs.google.com/presentation/d/13VK5fP5px3VwIceA8hdOcJI5nd5T_rvh/preview)

### 背景

初学者にとって、Qiita などへの技術記事の投稿やコミュニティへの参加は心理的なハードルが高く、同じ目標を持つ仲間と出会う機会が限られています。sudachi は「完成度の高い記事」ではなく「今日学んだこと」を共有する場にすることで、このハードルを下げることを目指しています。

## 主な機能

### 開発メンバー募集

チーム開発のメンバー募集を、通常の投稿とは別の専用ページで扱います。

- 使用技術・希望する学習段階・初心者歓迎かどうかで、自分に合った募集を探せる
- 募集者のプロフィールから過去の学習投稿を確認でき、相手がどんなことを学んでいるかを把握したうえで応募できる
- 気になる募集には「興味あり」を送り、そのまま DM でやりとりを始められる

### 相棒キャラクター

学習を一人で続けるのは難しい、という課題に対する機能です。投稿するたびに経験値がたまり、ユーザーごとの相棒キャラクターが成長していきます。

<p align="center">
  <img src="frontend/public/images/character-egg.png" alt="たまご" width="96">
  <img src="frontend/public/images/character-hatching.png" alt="ふ化中" width="96">
  <img src="frontend/public/images/character-chick.png" alt="ひよこ" width="96">
  &nbsp;…
</p>

- 投稿1回につき経験値 +10
- 経験値が一定量たまると次の段階へ進化する（たまご → ひよこ → …）
- マイページで現在の段階と、次の進化までに必要な経験値を確認できる

### ナイス（いいね）

投稿へのリアクションです。押すとひよこがジャンプしてハートを持ち、♥ と ★ が飛び散るアニメーションが再生されます。

<p align="center">
  <img src="frontend/public/images/chick-idle.png" alt="押す前" width="80">
  &nbsp;→&nbsp;
  <img src="frontend/public/images/chick-cheer.png" alt="押した直後" width="80">
  &nbsp;→&nbsp;
  <img src="frontend/public/images/chick-heart.png" alt="ナイス済み" width="80">
</p>

## 画面と使い方

| 画面 | できること |
|---|---|
| タイムライン | みんなの学習投稿を見て、ナイスを送る |
| 投稿作成 | 学習内容を投稿する（画像は任意）。投稿を終えると相棒キャラクターに経験値が入る |
| 募集 | 開発メンバーの募集を一覧・作成し、気になる募集に「興味あり」を送る |
| メッセージ | ユーザー同士で DM をやりとりする |
| マイページ | 自分の投稿と相棒キャラクターの成長を確認する |

## 技術スタック

| 領域 | 技術 |
|---|---|
| フロントエンド | React / TypeScript / Vite / React Router |
| バックエンド | FastAPI / SQLAlchemy |
| 認証・DB・画像ストレージ | Supabase（Auth / PostgreSQL / Storage） |
| ホスティング | Vercel（フロントエンド）/ Render（バックエンド） |

## 担当箇所

投稿機能・タイムライン

---

## 開発者向け

セットアップ・開発サーバーの起動・デプロイ手順は [docs/development.md](docs/development.md) にまとめています。
