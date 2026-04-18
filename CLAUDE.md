# 鉱石のすみか Web制作 作業ルール

## プロジェクト概要
- 店名：鉱石のすみか（パワーストーン・鉱石・アクセサリー専門店）
- 所在地：静岡県富士宮市
- 目的：実店舗への集客（オンライン販売なし）
- 公開URL：https://kousekino-sumika.pages.dev
- ホスティング：Cloudflare Pages（GitHubと自動デプロイ連携済み）
- GitHubリポジトリ：https://github.com/kousekino-sumika/kousekino-sumika
- GAS URL：https://script.google.com/macros/s/AKfycbziitAbrKunsAbSAjDmxc0m42P2hncwTAvlfG0i0NJY8dLh2oj3qo6wLYs60HnAECro/exec
- Gmail：tfg.kousekino.sumika@gmail.com
- Instagram：@tfg_kousekino_sumika
- Facebook：https://www.facebook.com/profile.php?id=100013163796296
- Amebaブログ：https://ameblo.jp/tfg1029/
- GA4測定ID：G-X1NMBB6948
- Microsoft Clarity ID：waj1iaac0q
- SnapWidget ID：1120344（※本番アカウントへ切替要）

## ファイル命名規則
- HTMLファイル（正式ライン）：index0125.html〜（4桁連番）
- HTMLファイル（ベータライン）：b0001.html〜（新デザイン実験用）
- Web台帳：鉱石のすみか_Web台帳_v0043.html（v+4桁）
- Webリサーチ：鉱石のすみか_Webリサーチ_v0002.html（v+4桁）
- 画像ファイル：基本は.jpg形式、img/フォルダに配置
- ファビコン：favicon.ico / favicon_32.png / favicon_180.png（img/フォルダに配置）

## フォルダ構成
- img/：画像ファイル（.jpg）、ファビコン関連ファイル

## 技術スタック
- フォント：Cinzel Decorative、Cormorant Garamond、Noto Serif JP
- カラー：パープル系（CSS変数で管理）
- 動的ニュース：Google Apps Script（GAS）+ Googleスプレッドシート
- Instagramギャラリー：SnapWidget（ID: 1120344）
- アナリティクス：Google Analytics 4（G-X1NMBB6948）、Microsoft Clarity（waj1iaac0q）
- 構造化データ：JSON-LD / Schema.org（Store型）

## スプレッドシート仕様
- A列：投稿日（自動）/ B列：バナー表示 / C列：Web表示 / D列：分類 / E列：タイトル / F列：本文 / G列：リンクURL
- 2〜6行目：テンプレート行（入力欄）
- 7行目以降：データ行（新しい順）
- __auto__フラグ行（緑色）：GAS自動生成行。定休日自動投稿などに使用
- 90日超の行：グレーアウト＋バナー・Web表示自動オフ

## GASデプロイルール
- doGet関数を変更したときのみ新規デプロイが必要
- それ以外の関数はCtrl+Sで保存のみでOK

## 作業ルール
- コードを書く前に必ず「提案 → 確認 → 実装」の順で進める
- 提案前に現状・仕様・前提条件を確認・整理する
- 提案時はメリット・デメリット・影響範囲を明示する
- 指示された箇所以外は勝手に変更しない
- 改善点があれば根拠を明示したうえで提案する
- 不明点は着手前にまとめて質問する
- 同じエラーが3回続いたら別のアプローチを提案する
- コードには必ずコメントをつける
- 説明は結論 → 理由の順で書く
- 選択肢を提示するときはボタン式で表示する
- indexを出力するときは台帳も必ず同時に更新する
