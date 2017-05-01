# 種類
- git log操作系
- git branch操作系
- git diff操作系
- git reset操作系

# リモートブランチの最新版をもとにローカルにブランチを作成する

# リモートリポジトリのあるブランチをローカルにpullしてくる

# コミットログを修正する

# コミットログをまとめる

`git rebase -i`を利用します。

直近3つのコミットをまとめたい場合は



例えば、以下のようなコミットログあるとします。
```
c50a10c add test3
7073308 add test2
b29fb6a add test1
3368146 first commit
```

このとき、直近のコミット3つをまとめたいとします。
その場合は`git rebase -i HEAD~~~`を実行します。(`git rebase -i HEAD~3`でもOK)
HEADのあとにまとめたいコミットの数だけ`~`を記述します。

すると以下のような内容が記述された編集画面になると思います。
```
pick b29fb6a add test1
pick 7073308 add test2
pick c50a10c add test3
```

ここでまとめたいコミットログの部分をpickからsquashに変更します。(sだけでも可能)

```
pick b29fb6a add test1
pick 7073308 add test2
pick c50a10c add test3
```



# プルリクに生じたコンフリクトを解決する

# リモートにpushしたコミットをなかったことにする

- reset hard
- revert

# addしたものと差分を確認したい

git diff --cached (commit直前に実行したりする)

# commitしたものと差分を確認したい

# pushする前にリモートと差分を確認したい

# 特定のファイル(もしくはディレクトリ)についてブランチ間で差分を確認したい

- ローカルどうし
- リモートと確認

# gitignoreの反映をさせる

# git resetについて
- reset soft
- reset hard




＝＝＝＝＝＝＝＝

リモートのdevelopブランチからブランチを切る
gch -b hogehoge origin/develop

addしたやつとHEADとの差分をみる
git diff --cached


git commit --amend


手順的には、過去直近3つ分を書き換えたい場合
git rebase -i HEAD~3

pickをeにして（もしくはedit )終了

git commit --amend
コミットログの編集
git rebase --continue
git push origin -f HEAD

diffの参考
http://qiita.com/hide/items/17b970c485e803cbce08

http://qiita.com/shibukk/items/8c9362a5bd399b9c56be
