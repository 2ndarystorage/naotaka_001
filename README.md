# 『つくりながら学ぶ！生成AIアプリ＆エージェント開発入門』 サンプルコードリポジトリ
 
このリポジトリは、書籍『つくりながら学ぶ！生成AIアプリ＆エージェント開発入門』のサンプルコードを提供しています。

## ディレクトリ構成

- `.devcontainer`: VS CodeのDevContainerの設定ファイルが含まれています。
  - `Dockerfile`: DevContainerで使用するDockerfileです。
  - `devcontainer.json`: DevContainerの設定ファイルです。
- `.streamlit`: Streamlitの設定ファイルが含まれています。
- `chapter_001`～`chapter_011`: 各章のサンプルコードが格納されています。
- `.env.template`: 環境変数のテンプレートファイルです。
- `.gitignore`: Gitレポジトリの管理対象から外すファイルの設定が記述されています。
- `requirements.txt`: 必要なPythonパッケージが記載されています。


## 使い方

### 環境変数の設定

1. `.env.template`をコピーして`.env`ファイルを作成します。
2. `.env`ファイルに必要な環境変数の値を設定します。以下の環境変数が利用可能です：
   - `OPENAI_API_KEY`: OpenAI APIのAPIキー
   - `ANTHROPIC_API_KEY`: Anthropic APIのAPIキー
   - `GOOGLE_API_KEY`: Google APIのAPIキー
   - `LANGCHAIN_TRACING_V2`: LangChainのトレース機能の有効化設定
   - `LANGCHAIN_ENDPOINT`: LangChainのエンドポイントURL
   - `LANGCHAIN_API_KEY`: LangChainのAPIキー

### 環境変数の読み込み

- このレポジトリでは各章のアプリケーションは`load_dotenv`を利用して`.env`ファイルから環境変数を読み込みます。
  - そのため、事前に環境変数を設定しておく必要があります。
  - `load_dotenv`を利用しない場合は、`from dotenv import load_dotenv; load_dotenv()`の周辺の行を削除してください。

### (オプション) DevContainerの利用

- このリポジトリはVS CodeのDevContainerに対応しています。
  - DevContainerを利用する際はDockerが事前にインストールされている必要があります。
- DevContainerを利用する場合は以下の手順で開発環境を構築できます：
  - ルートディレクトリをVS Codeで開きます。
  - 「コンテナで開く」オプションを選択して開きます。
  - しばらくするとDocker Containerのビルドが実行されます。
  - コンテナ内でStreamlitアプリケーションを起動すると、`local:8501`でアクセスできます
    - 8501ポートをコンテナに開放するようにDockerfileに設定されています

## 注意事項

- 各章のアプリケーションを実行する際は、必要なパッケージがインストールされていることを確認してください。
  - `requirements.txt`に記載されているパッケージは、DevContainerを利用する場合は自動的にインストールされます。

## 各社のモデルの最新状況
- 各社のモデルは随時更新されています。そのため出版時から状況が変化していることがあります。
- ChatGPT, Claude, Gemini の主要なモデルの最新状況は以下の記事か各社のホームページで確認してください
  - [【随時更新】主要な大規模言語モデル比較表](https://zenn.dev/ml_bear/articles/3c5e7975f1620a)

## 各章のアプリケーション・エージェントの動作例

TODO: 動画を足す

## Program Summary
- 書籍の各章で扱う生成AIアプリ／エージェントのサンプル実装集。
- 主にStreamlitで、チャットUI、Web/YouTube要約、画像認識・生成、PDF QA（ベクトル検索）、Webブラウジングエージェント、カスタマーサポートチャット、データ分析エージェントなどのデモを含みます。

## How to Use
- Not verified
- `requirements.txt` の依存関係をインストール後、実行したい章のスクリプトを `streamlit run <path>` で起動します。
  - 例: `streamlit run chapter_002/main.py`
  - 例: `streamlit run chapter_007/main.py`（PDF QAメニュー）

## Completion Status
- partial
  - 章ごとのデモが揃っている一方、統合されたアプリ構成やテストが見当たらず、学習用のサンプルとしての完成度に留まります。

## Program Summary
- 書籍の各章に対応したStreamlitサンプル集。チャットUI、Web/YouTube要約、画像QAと画像生成、PDFアップロード＋FAISS検索のQA、Webブラウジングエージェント、カスタマーサポートエージェント、データ分析エージェント（Code Interpreter／BigQuery連携）を含みます。
- 各アプリは章ごとに独立したスクリプトとして配置されています。

## How to Use
- Not verified
- 依存関係をインストール: `pip install -r requirements.txt`
- 実行したい章のアプリを起動: `streamlit run <path>`
  - 例: `streamlit run chapter_002/main.py`
  - 例: `streamlit run chapter_007/main.py`
- 章によっては追加の設定が必要です（例: `.env` のAPIキー、`st.secrets["gcp_service_account"]`、LangSmith設定など）。

## Completion Status
- partial
  - 章ごとの単体デモは揃っていますが、統合されたエントリーポイントやテスト、配布用の整備は見当たりません。

## Program Summary
- 書籍の各章に対応したStreamlitサンプル集で、チャット、要約（Web/YouTube）、画像QA（Vision）、画像生成（DALL·E 3）、PDFアップロード＋FAISSベクトル検索のQA、Webブラウジングエージェント、カスタマーサポートエージェント、データ分析（Code Interpreter／BigQuery）などのデモが含まれます。
- 各章は独立したスクリプトとして配置されています。

## How to Use
- Not verified
- 依存関係のインストール: `pip install -r requirements.txt`
- 環境変数の設定: `.env.template` を `.env` にコピーしてAPIキー等を設定
- 章ごとのアプリを起動: `streamlit run <path>`
- 例: `streamlit run chapter_002/main.py`
- 例: `streamlit run chapter_007/main.py`

## Completion Status
- partial — 章ごとのデモは揃っていますが、統合されたエントリーポイントやテスト/配布向けの整備が見当たりません。

## Program Summary
- 書籍各章のStreamlitサンプル集。チャットUI、モデル選択とコスト表示、Web/YouTube要約、画像QA、画像生成、PDFアップロード＋FAISS検索によるQA、Web検索エージェント、カスタマーサポートエージェント、データ分析エージェント（Code Interpreter／BigQuery連携）などを含みます。
- 章ごとに独立したスクリプトとして配置されています。

## How to Use
- Not verified
- 依存関係のインストール: `pip install -r requirements.txt`
- 環境変数の設定: `.env.template` を `.env` にコピーしてAPIキー等を設定
- 起動: `streamlit run <path>`（例: `streamlit run chapter_002/main.py`、`streamlit run chapter_007/main.py`）
- 章によって追加設定が必要な場合があります（例: BigQuery認証、`st.secrets` など）

## Completion Status
- partial
  - 章ごとの単体デモは揃っていますが、統合されたエントリーポイントやテストは見当たりません。

## Program Summary
- 書籍各章のStreamlitサンプル集。章ごとに独立したアプリが配置され、チャット、モデル選択＋コスト表示、Web/YouTube要約、画像認識・画像生成、PDFアップロード＋FAISS検索のQA、Webブラウジングエージェント、カスタマーサポートエージェント、データ分析エージェント（Code Interpreter／BigQuery連携）などが含まれます。
- 一部の章では補助スクリプト（例: FAQベクトルDBの構築）やツール実装があります。

## How to Use
- Not verified
- 依存関係のインストール: `pip install -r requirements.txt`
- 環境変数の設定: `.env.template` を `.env` にコピーしてAPIキー等を設定
- 章ごとのアプリを起動: `streamlit run <path>`（例: `streamlit run chapter_002/main.py`、`streamlit run chapter_007/main.py`）
- 章によって追加設定が必要です（例: `chapter_010` のFAQベクトルDB作成、`chapter_011/part2` の `st.secrets["gcp_service_account"]`）

## Completion Status
- partial
  - 章ごとのサンプルは揃っていますが、統合されたエントリーポイントやテスト、配布向けの整備は見当たりません。
