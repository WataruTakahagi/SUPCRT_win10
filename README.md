# SUPCRT_win10

Windows10でSUPCRT92を動かす

まずFortranを準備する。Windows用のFortran環境として、手っ取り早くフリーのコンパイラを利用。  
https://sourceforge.net/projects/mingw-w64/files/?source=navbar  
このページからDownload mingw-w64-install.exe (170.0 kB)をクリックしてmingw_w64-install.exeをダウンロードして解凍。  
※こちらから直接ダウンロードも可能 https://sourceforge.net/projects/mingw-w64/files/latest/download?source=file (64bit)  
Architectureをx86_64にする他はひたすらNextでとりあえず問題ない。

一応Fortranが動くことを確認しておく。
コマンドプロンプト(コルタナさんに"cmd"と聞くとよい)で  

```
>gfortran
```

と打って

```
gfortran: fatal error: no input files
```

となればOK。  

続いてSUPCRT92をダウンロード。  
http://pages.uoregon.edu/palandri/data/Supcrt92.zip



```
>cd Downloads  
>cd Supcrt92  
```

これで準備は完了。
