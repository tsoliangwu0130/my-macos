# MacTeX + Skim + Atom

## Introduction
這篇筆記將介紹如何在 [Atom](https://atom.io) 上透過 [LaTeX](https://atom.io/packages/latex) 插件編譯 `.tex` 文件並使用 [Skim](http://skim-app.sourceforge.net/) 檢視。

## Note
Before started we need to install [Atom](https://atom.io), [Skim](http://skim-app.sourceforge.net/), and [MacTeX](http://skim-app.sourceforge.net/).

### Homebrew
I use [Homebrew](https://brew.sh) to install MacTeX. To install:
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### MacTeX
To install:
```
$ brew cask install mactex
```

### Atom LaTeX Package
To install [LaTeX package](https://atom.io/packages/latex) on Atom:
```
$ apm install latex
```
To compile `.tex` files, press `ctrl + alt + b`.

## Screenshot
After installed these tools, now you can view your `.tex` files on [Skim](http://skim-app.sourceforge.net/):

![MacTeX + Skim + Atom](./images/MacTex_Skim_Atom.png)
