# Node.jsのレシピ

Node.js構築のレシピをまとめています（随時更新）  
何でも作れるのでまとめるのが難しい。

> 宗教上の理由によりTypeScriptは使用しません。

## Node.jsの利点

- スクリプト言語の中では圧倒的に速いです。
- async/awaitでの並行処理が簡単にできます。（CPU注意）
- npmやnvmなどエコシステムが充実していて開発環境の構築に困ることがありません。
- もし会社がWebサービス主体なら人材獲得に困らないNode.jsが第一候補になります。

大量のトラフィックを高速に捌く必要がある部分は Go、Nodeにまともなパッケージがない場合は Python など、基本言語はNode.jsにして一部だけ別言語に切り替えるのが一般的かと思います。

## 目次

### 開発環境

- [package.json設定](./docs/開発環境/package.jsonの設定.md)
- [コード整形](./docs/開発環境/コード整形.md)
- [テスト](./docs/開発環境/テスト.md)
- [JSDoc](./docs/開発環境/JSDoc.md)
- [Makefileも使えます](./docs/開発環境/Makefileも使えます.md)

### 便利ツール

- [serve](./docs/便利ツール/serve.md)
- [npm-run-all2](./docs/便利ツール/npm-run-all2.md)
- [vite](./docs/便利ツール/vite.md)

### Web

- [SPAとSSRとSSG](./docs/Web/SPAとSSRとSSG.md)
- [ドキュメントサイト](./docs/Web/ドキュメントサイト.md)
- [PWA](./docs/Web/PWA.md)
- [Web Worker](./docs/Web/WebWorker.md)

### サーバーサイド

- [API](./docs/サーバーサイド/API.md)
- [ファイル操作](./docs/サーバーサイド/ファイル操作.md)
- [スクレイピング](./docs/サーバーサイド/スクレイピング.md)

### ローカル

- [ファイル変更の監視](./docs/ローカル/ファイル変更の監視.md)
- [コード解析](./docs/ローカル/コード解析.md)

### パッケージ制作

- [npmパッケージの公開](./docs/パッケージ制作/npmパッケージの公開.md)
- [GitHub Packagesの公開](./docs/パッケージ制作/GitHubPackagesの公開.md)
- [オリジナルCLIの配布](./docs/パッケージ制作/オリジナルCLIの配布.md)
- [createリポジトリ](./docs/パッケージ制作/createリポジトリ.md)
