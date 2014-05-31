vimrc
=====

vimrc　vim設定ファイル


参考
- [いまさら聞けないVim（6）：設定ファイルを作って自分の好みに改造](http://www.atmarkit.co.jp/ait/articles/1107/21/news115.html)


現段階で見よう見まね

#環境2
- Windows Vista SP2
- Command prompt
- [Vim version 7.4.274](http://www.kaoriya.net/software/vim/)

コマンドプロンプトでエディタを使う場合、フルパスで指定する必要があり、利便性を考慮すると先にPATHを通しておくことが望ましい。システム環境変数で設定できる。ついでにサクラエディタとTerapadも導入。

(エディタだけに限らない。良く使うプログラムは先にパスを通すべき)

このWindows用のvimとubuntuのvimで異なる点
- 日本語入力切替　Alt + 半角英数

大いに評価する。ESCキーと間違って日本語入力になることはなく、意識して切り替えが出来る。

これとは関係ないが、家のパソコンだとミュートではないのでESCキー連打するとポポポンと音がうるさいのが困る。

git commitで香り屋vimを使うと文字化けするが、.mdファイルの編集に関しては文字化けしないことが分かったので、設定の変更は無し。

git commit時のメッセージは`git commit -m ""`という風に打つことにした。~~最初からそうしろ~~

~~#文字化け対策(内部エンコーディングをからUTF-8へ。)~~

~~kaoriya vimフォルダの/switches/catalog/utf-8.vim を /switches/enabled へコピー~~

以下 _vimrc  の中身(環境1のVimrcに追加する形)
***
```
#今のところ無し
```
ここまで
***


#環境1 14/05/30 17:29
.vimrc

```
set expandtab
set tabstop=2
set shiftwidth=2

set number
set ruler
set cursorline
set laststatus=2
set cmdheight=2
set whichwrap=b,s,h,l,<,>,[,]

set wildmenu wildmode=list:longest,full
set history=100

set incsearch
set wildmenu wildmode=list:full
set statusline=%F%r%h%=
```
***

