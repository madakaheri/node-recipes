# JSDoc

JSDoc はJavaScript内のコメントで TypeScript のように「型」を表現できる拡張機能です。  
＊ VSCodeなら何もインストールせずに使えます。

ドキュメントは [こちら](https://www.typescriptlang.org/ja/docs/handbook/jsdoc-supported-types.html) に全て記述されています。

- 関数の使い方コメント
- 引数の型と説明
- 返り値の型と説明

など、importした側にも表示されるので非常に強力な実装支援になります。

## 型の書き出し

typescriptをインストールして tsc コマンドを実行すると型を書き出せます。

1. typescriptのインストール
	```bash
	npm i -D typescript
	```

2. package.json の "scripts" にビルドコマンド追加
	```json
	{
		"scripts": {
			"build": "tsc"
		}
	}
	```
3. ビルド実行
	```bash
	npm run build
	```

## JSDoc注意点

### JSDocの「@typedef」で型を作成すると強制的に export される

一見自動exportは良いように感じますが、同じ名前の型を別ファイルで作成したときにエラーになります。これを回避するため、型定義はできるだけクラスで行うようにするのが無難です。

```javascript
/**
 * これは自動で export されてしまう。
 * @typedef {Object} SpecialType - 'SpecialType'という名前の新しい型を作成
 * @property {string} prop1 - SpecialTypeの文字列プロパティ
 * @property {number} prop2 - SpecialTypeの数値プロパティ
 * @property {number=} prop3 - SpecialTypeの任意の数値プロパティ
 * @prop {number} [prop4] - SpecialTypeの任意の数値プロパティ
 * @prop {number} [prop5=42] - SpecialTypeのデフォルト値を持つ任意の数値プロパティ
 */

// ↓↓ クラスで定義するのがおすすめ ↓↓

class SpecialType {
	/** @type {string} */
	prop1;
	/** @type {number} */
	prop2;
	/** @type {number} */
	prop3;
	/** @type {number?} */
	prop4;
	/** @type {number?} */
	prop5;
}
```
