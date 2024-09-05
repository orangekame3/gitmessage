# gitmessage

## Conventional Commits

コミットメッセージは[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)にゆるくしたがってください。

### コミットメッセージのフォーマット

.gitmessageを利用することでコミットメッセージのテンプレートを提供します。
これは`git config --local`に設定することで、本プロジェクト内でのみ有効になります。

```bash
git config --local commit.template .gitmessage
```

この設定を行うことで、`git commit`を実行した際に`.gitmessage`の内容がエディタ(デフォルトではVim)に表示されます。

```bash
git commit
# Overview (Uncomment one of the following templates)
#feat: 
# └  A new feature
#fix:
# └  A bug fix
#docs:
# └  Documentation only changes
#style:
# └  Changes that do not affect the meaning of the code
#    (white-space, formatting, missing semi-colons, etc)
#refactor:
# └  A code change that neither fixes a bug nor adds a featur
#test:
# └  Adding missing or correcting existing tests
#ci:
# └  Changes to our CI configuration files and scripts
#chore:
# └  Changes to the build process or auxiliary tools and libraries

```

適切なテンプレートを選択し、コメントアウトをはずしてコミットメッセージを記述してください。

```bash
docs: Update README.md
# └  Documentation only changes
```

## コミットメッセージとラベルの対応

`develop`ブランチへのPRを作成するときにコミットメッセージからラベルを自動で付与するように設定しています。
以下、プレフィックスとラベルの対応です。

|　プレフィックス | ラベル | 説明|
|---|---|---|
|feat: | `feature` | 新機能の追加|
|fix: | `bugfix` | バグの修正|
|docs: | `documentation` | ドキュメントのみの変更|
|style: | `style` | コードの意味に影響を与えない変更（空白、フォーマット、セミコロンの欠落など）|
|refactor: | `refactor` | バグの修正や機能の追加を行わないコードの変更|
|test: | `test` | テストの追加、修正|
|ci: | `ci` | CIの追加、修正|
|chore: | `chore` | 些末な変更 |
