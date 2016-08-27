# SUPCRT_win10

Windows10でSUPCRT92を動かす

まずFortranを準備する。Windows用のFortran環境として、手っ取り早くフリーのコンパイラを利用。  
https://sourceforge.net/projects/mingw-w64/files/?source=navbar  
このページからDownload mingw-w64-install.exe (170.0 kB)をクリックしてmingw_w64-install.exeをダウンロードして解凍。  
※こちらから直接ダウンロードも可能 https://sourceforge.net/projects/mingw-w64/files/latest/download?source=file (64bit)  
Architectureをx86_64にする他はひたすらNextでとりあえず問題ない。

Fortranのテキストエディタは個人的にはAtomがおすすめなのでインストール。  
https://atom.io/
language-fortranというパッケージを入れておく。  

続いてSUPCRT92をダウンロード。  
http://pages.uoregon.edu/palandri/data/Supcrt92.zip  
これで準備は完了。

[PC]=>[ローカルディスク(C:)]=>[Program Files]=>[mingw-w64]=>[x86_64-5.2.0-posix-seh-rt_v4-rev1]を開く。  
この中にあるmingw-w64.batをSupcrt92フォルダの中にコピーする。

一応Fortranが動くことを確認しておく。
コマンドプロンプト(コルタナさんに"cmd"と聞くとよい)で  

```
>cd Downloads  
>cd Supcrt92
>atom mingw-w64.bat
```

とすると、Atomでmingw-w64.batが編集できる。
5行目のcd "C:\"を削除して保存。

```
>gfortran
```

と打って

```
gfortran: fatal error: no input files
```

となればOK。  
