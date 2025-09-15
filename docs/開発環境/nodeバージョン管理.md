# nodeバージョン管理

まず最初に「[nvm](https://github.com/nvm-sh/nvm)」をインストールして node.js のバージョンを合わせましょう。  
nvmを使えばバージョン番号を指定するだけで node と npm のバージョンを切り替えてくれるようになります。

インストールが済んで nvm コマンドが使用できるようになったら次へ進んでください。

## 1. 必要なnodeバージョンをインストール

多くの場合はLTS版（今なら22.x）だけインストールしておけば問題ありません。

```bash
nvm install --lts
```

古いバージョンのプロジェクトを持っている場合は古いバージョンも入れておきましょう。

```bash
nvm install 18
```

## 2. デフォルトのnodeバージョンを設定

今なら22をデフォルトにしておけば間違いありません。

```bash
nvm alias default 22
```

### デフォルト設定してもすぐ元に戻ってしまう場合

この症状、私も出ています。 ```open ~/.zshrc``` コマンドで zshrc に ```nvm use default``` を追記するとターミナルを開く度にデフォルトが使用されます。

```bash
# nvmに必要な設定
export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

# 常にデフォルトのNode.jsバージョンを使用
nvm use default
```

---

> #### 知識: Run Command ファイル
>  .zshrc や .bashrc は 「Run Command ファイル」と呼ばれるもので、ここに書いたスクリプトはターミナルを開く度に実行されます。
