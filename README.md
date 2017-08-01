# mdtexpdf
## Description
markdownファイルからTeXファイルを作成するスクリプトと，TeXからpdfを作成するスクリプト．

## Requirement
```
pthon3系
pandoc
latex
fireport.sty
jlisting.sty
```

## Usage
1. markdownファイルを作成する．
2. $./mdtex markdown.md を実行するとoutmdtex.texとsemireport.texが出力される．
3. semireport.texを編集し，細かな修正を加える．
4. $./texpdf semireport.tex を実行するとpdfファイルが生成される．

$./texpdf -o にするとプレビューが開かれる．

## Coution
1. テンプレートファイルに行数を指定して差し込んでいる（mdtex19行目）のため自分のテンプレートファイルを使う場合や，テンプレートファイルを編集した場合は注意が必要．
2. mdtexは実行ファイルの形式にしているため，シバンに自分の環境のPythonのパスを書く必要がある．
3. mdtexとtexpdfは実行権限を与える必要がある．

## Installation
このままでも実行できるが，mdtexとpdfに実行権限を与えパスの通っているディレクトリに配置するとどこからでもこのコマンドが使えて便利．
```
e.g.
chmod 755 mdtex
cp mdtex /usr/local/bin/.

```
ファイルを移動させた場合は，テンプレートファイルのパスを自分の環境に合わせて，記述し直す必要がある．
