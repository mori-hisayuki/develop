# SolidJS Sample Development

## 概要

`SolidJS`で開発するためのサンプル開発環境です。
主に VSCode で開発されることを想定しているため、`devcontainer`と`.editorconfig`が付属しています。
アプリケーションディレクトリ(`app`)は SolidJS の[template](https://github.com/solidjs/templates)を利用しました。
使用した template は`ts-vitest`です。

## 選定技術

- [TypeScript](https://www.typescriptlang.org/)
- [pnpm](https://pnpm.io/ja/)
- [Vite](https://vitejs.dev/)
- [SolidJS](https://www.solidjs.com/)
- [Vitest](https://vitest.dev/)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)
- [husky](https://typicode.github.io/husky/#/)

## ディレクトリ構造

```
|--.devcontainer // remote containerの設定
|  |--devcontainer.env // Git管理対象外
|  |--devcontainer.json
|  |--docker-compose.yml
|  |--ubuntu
|     |--Dockerfile
|--.app // アプリケーション本体
|  |--.husky // husky用script
|--.gitignore
|--.editorconfig // VSCode拡張 "EditorConfig for VS Code"用のファイル
|--README.md
```

## Github への接続

ホストの`~/.ssh`ディレクトリをマウントしているため、接続先情報はホストに依存する
接続情報が追加された known_hosts を ssh ディレクトリに追加する

## 環境変数

`.devecontainer`の直下に`devcontainer.env`ファイルを配置すると読み込まれる
