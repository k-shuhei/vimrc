vimrc
=====

vimrc　vim設定ファイル


参考
- [いまさら聞けないVim（6）：設定ファイルを作って自分の好みに改造](http://www.atmarkit.co.jp/ait/articles/1107/21/news115.html)


現段階で見よう見まね

- 環境2
- Windows Vista SP2
- Command prompt
- Vim version 7.4.274

このWindows用のvimとubuntuのvimで異なる点
- 日本語入力切替　Alt + 半角英数

大いに評価する。ESCと間違って日本語入力になることはなく、意識して切り替えが出来る。

これとは関係ないが、家のパソコンだとミュートではないのでESCキー連打するとポポポンと音がうるさいのが困る。


以下 _vimrc  の中身
***
```vim
#検索と補完機能
set incsearch
set wildmenu wildmode=list:full

#カーソルライン
syntax on
set nohlsearch
set cursorline

#文字ハイライト
highlight Normal ctermbg=black ctermfg=grey
highlight StatusLine term=none cterm=none ctermfg=black ctermbg=grey
highlight CursorLine term=none cterm=none ctermfg=none ctermbg=darkgray

#行番号
set number

#インデント
set tabstop=2

#ステータス表示
set laststatus=2
set statusline=%F%r%h%=
```
***
ここまで
