# 問題点

このプロジェクトで見つかったいくつかの問題点を以下に記載します。

## 1. TypeScriptソースファイルの欠落
`antigravity_extension` ディレクトリ内の `package.json` には TypeScript のビルドスクリプト (`"compile": "tsc -p ./"`) や `devDependencies` が含まれていますが、ソースとなる `.ts` ファイルがリポジトリ内に見当たりません。また、`lint` スクリプトは `src` ディレクトリを参照していますが、このディレクトリも存在しません。現在はコンパイル済みの `extension.js` のみが存在しているようです。

## 2. 拡張機能の命名の不整合
`antigravity_extension/package.json` において、拡張機能の名前が以下のように設定されていますが、プロジェクトの目的（AntiGravityとの連携）と一致していないように見えます。
- `"name": "commandlineshowgitview"`
- `"displayName": "CommandLineShowGitView"`
