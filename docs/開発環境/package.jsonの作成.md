# package.json の作成

package.json はプロジェクトルートに必要なファイルで、**node の挙動設定** や **npmパッケージの管理** など色々な設定ができるファイルです。このファイルを作るのは簡単で次のコマンドを打つと "コマンドを打った場所に" package.json が作成されます。

## package.jsonの生成コマンド

```bash
npm init
```

実行すると対話形式で生成できます。

```bash
npm init -y
```

```-y``` オプションを付けると全部Yesの設定でサクッと作成できます。  
ターミナルでチマチマ入力するよりも生成されたファイルを修正する方が手っ取り早いと感じるなら -y を付けて生成しても全然構いません。

### このリポジトリで生成したサンプル

```json
{
  "name": "recipes",
  "version": "1.0.0",
  "description": "Node.js構築のレシピをまとめています（随時更新）   何でも作れるのでまとめるのが難しい。",
  "type": "module", // <-- 超重要
  "main": "index.js",
  "directories": {
    "doc": "docs"
  },
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/madakaheri/node-recipes.git"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/madakaheri/node-recipes/issues"
  },
  "homepage": "https://github.com/madakaheri/node-recipes#readme"
}

```

## 重要な設定

### "type": "module"

現在のデフォルトは ```"type": "commonjs"``` という、かなり初期のJavaScriptモードでファイル解析されるようになっています。現在では基本的に ```"type": "module"``` と書いて問題ありません。

module に指定しないと import / export が動きませんので必ず設定するようにしましょう。
