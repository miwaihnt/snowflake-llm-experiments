# Cortex Analyst 実験環境

このディレクトリは、以下の記事の補助用です：

- [Snowflake Cortex Analyst徹底検証 #1: Text-to-SQLの基本と単表/マルチターン精度を上げる設計](https://zenn.dev/nttdata_tech/articles/b7e27f17e348a7)

記事中で紹介した **検証シナリオを手元で再現できるようにする** ための Notebook と YAML を含んでいます。

---

## 📘 内容物

- CortexAnalyst_L1.yml
- setup_L1.ipynb

---

## 🚀 使い方

### 1. 環境セットアップ
1. Snowflake 環境にログイン
2. `notebook.ipynb` を開き、順に実行してください。  
   - データベース/スキーマ/テーブル作成  
   - サンプルデータ（3000件程度）投入  
3. SnowsightからCortex Analystを設定します

---

### 2. セマンティックビュー定義
- `CortexAnalyst_L1.yml` には、記事内で解説した **最終版の定義** を収録しています。  
- 主な追加項目：
  - **会計年度（FISCAL_YEAR）**
  - **月番号（MONTH_NUM）**
  - **平均注文額（AVG_ORDER_REVENUE）**
- Snowsight の **Cortex Analyst Semantic View Generator** から読み込み、記事の質問例を試してください。

---

## ⚠️ 注意事項
- この環境は学習・検証用です。  
- 実運用環境で利用する場合は、ロール・権限・データボリュームに注意してください。