
# ReactのJSX構文をBabelでコンパイルしてブラウザで表示させるだけのサンプル

## 概要

create-react-appで自動生成されるnode.js環境は何をやっているのはわかりづらい。

そのためReact/JSX/Babelがそれぞれどういうことをしているのかを理解するために作成した。

## ファイル説明

| ファイル | 説明 | 
|---|---|
| ./src/app.jsx | JSX構文が含まれたReact(JSX)のソース。これをBabelでコンパイルする。|
| ./dest/app.js | Babelでコンパイルすると生成されるJavaScriptのソース。|
| ./index.html | Reactを実行するためのHTMLファイル。React本体と今回作成したJS(React) を読み込む。|

## 事前準備

node.js実行環境はあらかじめ用意しておく。

## npm環境の初期化

```
% npm init -y
```

## Babelパッケージのインストール

```
% npm install --save-dev babel-cli babel-preset-react babel-preset-es2015
```

## JSXのコンパイル

```
% ./node_modules/.bin/babel src -d dest --presets es2015,react
```

## HTTPサーバーを起動してブラウザで動作確認。

```
% npx http-server
```

http://localhost:8080/　をブラウザで開く。
「Hello, World!」が表示されればOK。
