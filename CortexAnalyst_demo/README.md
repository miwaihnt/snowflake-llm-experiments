# Cortex Analyst 検証補助資料

このディレクトリは、以下の記事を補助するための資料です：

- [Snowflake Cortex Analyst徹底検証 #1：Text-to-SQLの基本と単表/マルチターン精度を上げる設計](https://zenn.dev/nttdata_tech/articles/b7e27f17e348a7)  
- [Snowflake Cortex Analyst徹底検証 #2：JOIN編と検証から見えた設計上の考慮事項](https://zenn.dev/nttdata_tech/articles/305a605eac9f61)  

記事ごとに **環境セットアップ Notebook** と **セマンティックビュー定義 YAML** を用意しています。  
手順に沿って進めることで、記事内の検証シナリオを手元で再現できます。

---

## 📘 内容物

- **Cortex Analyst徹底検証 #1**  
  - `cortex_analyst_setup1.ipynb`  
  - `cortex_analyst_semantic_view1.yml`  

- **Cortex Analyst徹底検証 #2**  
  - `cortex_analyst_setup2.ipynb`  
  - `cortex_analyst_semantic_view2.yml`  

---

## 🚀 使い方

### 記事ごとに以下の流れで設定してください

#### 1. 環境セットアップ
1. Snowflake 環境にログインします  
2. 対応する `cortex_analyst_setup*.ipynb` を Snowflake Notebooks にインポートし、上から順に実行してください  
   - データベース / スキーマ / テーブルの作成  
   - サンプルデータ（約3,000件）の投入  
3. Snowsight から Cortex Analyst を設定します  

#### 2. セマンティックビュー定義
- 対応する `cortex_analyst_semantic_view*.yml` には、記事で解説した **最終版の定義** を収録しています  
- まずは Notebook で用意したデータを使って、自分でセマンティックビューを定義・質問を実行してみてください  
- 精度改善の方法がわからない場合は、この収録ファイルを参考にしてください  
  - Snowsight > **AI & ML > Cortex Analyst** > 「Edit YAML Editor」から定義を貼り付けて利用できます  

---

## ⚠️ 注意事項
- 本リポジトリの内容は学習・検証用です  
- 実運用環境で利用する場合は、ロール・権限・データ量などに十分ご注意ください  