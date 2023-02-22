---
title: "react-flow"
emoji: "🌎"
type: "tech"
topics:
  - "javascript"
  - "react"
  - "typescript"
  - "frontend"
  - "設計"
published: false
---

こんにちは、nakamuyuです。

株式会社UPDATAで[DataMage](https://datamage.com/)というサービスを開発してます。

https://zenn.dev/nakamuyu/articles/ae153d023936db

DataMageでは、ノーコードでSQLを組み上げる機能を提供しています。
そこでreact-flowを使ってる
UIはこんな感じです。

・・・・・・画像・・・・・



react-flowを使ったプロダクトを開発しているエンジニアの役に立てれば幸いです。

:::message
DataMageの細かい機能は是非[リリースノート](https://www.notion.so/updata/DataMage-ffa735f1bdb14206a73eda5ac5280128#f6a0313b10e84e9eafaa122e1c481099)をご参照いただければと思います。動画で機能を紹介してるので、イメージしやすいと思います。
:::
:::message
コンポーネント設計に限った話をします。
:::

# 前提
DataMageでは
一つのノードがDBにおける１テーブルを表している。
- 左のSQL機能（WhereとかGroupByとか）をドラッグ&ドロップ

なるべく抽象化して設計する方法を書いてDataMageを参考に実例を示しますが、すべてのドメインに当てはまるかは各人で判断いただけると嬉しい。


# どういった設計を目指すのか
- コアのロジックとノード毎のロジックを切り分ける
  - ノードの動き、エッジの接続

# 設計方針
ノードタイプごとに何が異なるのかを整理する
- Edgeの種類
- Handleの数
- 接続の可否条件
- ノードのデザイン
- ノード内の表示

DataMageの場合
- Edgeの種類は1種類
- Handleの数
  - 可変である必要がある
    - Joinとかは二つのテーブルをくっつける
    - Whereとかは1つのテーブルに対しか実行しないため1つで良い
    
- 接続の

# データベースの構造
- ノード内に

# 終わりに
ここまで読んでいただきありがとうございます。


また共有できることは随時記事にまとめていこうと思います！

どんなことでも良いので、興味を持ってくださった方はお気軽に [TwitterDM](https://twitter.com/yuta_nakamuyu)ください！是非お話ししましょう!!
- もっと詳細に聞きたい
- 幅広くフロントについて
- 新規事業（SaaS）について
- データ活用について
- DataMageについて
- ゴルフ一緒に行きましょう⛳️
- ポーカー行きましょう♤