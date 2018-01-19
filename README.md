# Hidemaru Markdown
秀丸エディタで Markdown 執筆環境を実現するためのオレオレセットです。

![180119_222420_hidemaru_markdown_sample](https://user-images.githubusercontent.com/23325839/35152874-8782c640-fd67-11e7-838c-0120461546a7.png)

<!-- toc -->
- [Hidemaru Markdown](#hidemaru-markdown)
  - [現在サポートする機能](#現在サポートする機能)
  - [ハイライト](#ハイライト)
    - [インストール](#インストール)
  - [アウトライン表示](#アウトライン表示)
    - [インストール](#インストール-1)
  - [目次挿入](#目次挿入)
    - [インストール](#インストール-2)
    - [使い方](#使い方)
  - [License](#license)
  - [Author](#author)

## 現在サポートする機能
- ハイライト表示
- アウトライン表示
- 目次挿入（外部ツールを使います）

## ハイライト
基本的な文法とカーソル位置を見易く表示します。

### インストール
- **その他 > ファイルタイプ別の設定** を開く
  - `.md` ファイル用の設定を適当につくる
  - **デザイン > 強調表示 > 読み込み** ボタンから [md.hilight](md.hilight) を読み込む
    - この時、全てのチェックボックスをオンにしてください

インストール後、`.md` ファイルを開くとハイライト表示が適用されているはずです。

## アウトライン表示
Markdown の見出し表記をアウトラインとして扱えるようにします。これにより以下メリットがあります。

- アウトライン解析の枠に見出し一覧を表示できる
- 前/次の見出しにキー一発でジャンプできる

### インストール
- 上記ハイライトをインストールする
- **ウィンドウ > アウトライン解析の枠** をオンにしてアウトライン枠を表示させる
- **その他 > キー割り当て** から以下を割り当てる
  - Alt + Up: 前の見出し
  - Alt + Down: 次の見出し

キー割り当てはお好きな割り当てで OK です。

## 目次挿入
[intoc](https://github.com/stakiran/intoc) を用いて、目次(Table Of Contents)を生成して挿入できるようにします。Python が必要なため、導入ハードルは高いです。

### インストール
- [intoc](https://github.com/stakiran/intoc) をインストールする
  - Python 環境が必要です
  - GitHub の知識が必要です
  - 詳しい解説は割愛します :sweat:
- [launch_intoc.mac.sample](launch_intoc.mac.sample) を `launch_intoc.mac` にリネーム後、intoc.py のパスを修正する
- **その他 > マクロ登録** より `launch_intoc.mac` を登録する
- (任意) 呼び出しやすいよう当該マクロをツールバーに配置したりキー割り当てしたりする

### 使い方
- 秀丸エディタで `.md` ファイルを開く
- 目次を挿入したい行に `<!-- toc -->` と書く
- 当該マクロを呼び出す

ただし外部(intoc.py)からファイル内容を変更する挙動になるため、以下ダイアログが出ます。

![cofirm_reload](https://user-images.githubusercontent.com/23325839/35152754-f877b866-fd66-11e7-89e8-9f4aee46ef55.jpg)

## License
[MIT License](LICENSE)

## Author
[stakiran](https://github.com/stakiran)
