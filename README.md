vimrc
=====

vimrc　vim設定ファイル


参考
- [いまさら聞けないVim（6）：設定ファイルを作って自分の好みに改造](http://www.atmarkit.co.jp/ait/articles/1107/21/news115.html)


現段階で見よう見まね

#環境4
- Windows Vista SP2(環境2と同じPC)
- VIM - Vi IMproved version 7.4.335
- Cygwin - mintty 1.1.3 

```
set nocp
syntax on
set nobackup
set backspace=start,eol,indent
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

#環境3
- Windows Vista SP2(環境2と同じPC)
- VIM - Vi IMproved 7.4 (2013 Aug 10, compiled Feb 21 2014 18:03:10) MS-Windows 32-bit console version
- MINGW (Git version 1.9.2-preview20140411に付属)

コマンドラインは使い勝手がいいが、初期状態のVimでは構文が色分けされない。なので、カラースキームの導入と下の設定を追加したが、色分けされなかった。もう少し調べる必要あり。

```
set nocompatible
syntax on
```

***
#環境2
- Windows Vista SP2
- Command prompt
- [Vim version 7.4.274](http://www.kaoriya.net/software/vim/)

コマンドプロンプトでエディタを使う場合、フルパスで指定する必要があり、利便性を考慮すると先にPATHを通しておくことが望ましい。システム環境変数で設定できる。ついでにサクラエディタとTerapadも導入。

(エディタだけに限らない。良く使うプログラムは先にパスを通すべき)


#### このWindows用のvimとubuntuのvimで異なる点
- 日本語入力切替　Alt + 半角全角
(戻すときは、半角全角だけでok)

大いに評価する。ESCのつもりがうっかり半角全角を押して日本語入力になることはなく、これにより意識して切り替えが出来る。

これとは関係ないが、家のパソコンだとミュートではないのでESCキー連打するとポポポンと音がうるさいのが困る。




#### git commitで香り屋vimを使うと文字化けする問題

vi,さくらエディタ,Terapad,Notepadも同様:
- windowsで使うgit(:msysgit,Git 1.8.4より前のVersion)では日本語がサポートされてないっぽい。

参考：[WindowsでGitのコミットログが文字化けする問題の対処法](http://togetter.com/li/103988?page=1)

コマンドラインからコミットメッセージを書きこむとGitHub上からは文字化けせず正常に見れた。よって、git commit時のメッセージは`$ git commit -m "message"`という風に打つことにした。~~最初からそうしろ~~

`$ git commit -m "日本語文"`を打つとエラーメッセージが出た。

```
Warning: Your console font probably doesn't support Unicode. If you experience strange characters in
 the output, consider switching to a TrueType font such as Lucida Console!
```



#### 文字化け解消の試行錯誤中に

下の設定をして、vimでファイルひらくと文字化けしたのでやめる。
~~#文字化け対策(内部エンコーディングをUTF-8へ。)~~

~~kaoriya vimフォルダの/switches/catalog/utf-8.vim を /switches/enabled へコピー~~


#実際のvim設定ファイル
- 以下 _vimrc  の中身(環境1のVimrcに追加)

参考: [.vimrc-サンプル設定](https://sites.google.com/site/fudist/Home/vim-nihongo-ban/-vimrc-sample)

***
```
set nowritebackup
set nobackup
set wildmenu
set noerrorbells
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

