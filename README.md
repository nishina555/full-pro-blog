# full-pro-blog

ブログの記事を管理するリポジトリです。主にブログでソースをはりつけるgist-itを利用するために使います。

# gist-itの使い方

たとえばこのブランチの`2017/04/test/index.js`をブログで表示した場合は以下のようにします。
```
<script src="http://gist-it.appspot.com/github/nishina555/full-pro-blog/blob/master/2017/04/test/index.js"></script>
```

フッターをいれない場合は`?footer=0`を追加します。例えば以下のようになります。
```
<script src="http://gist-it.appspot.com/github/nishina555/full-pro-blog/blob/master/2017/04/test/index.js?footer=0"></script>
```

他にも、行を指定したい場合は`?slice=0:5`を追加します。(これは0行目から5行目だけを指定する場合です)
さらにfooterを0にしたいときは`?slice=0:5&footer=0`とします。

# スニペットを利用した、ブログにgist-itのスクリプトを貼り付ける手順

### atomの起動します。

```
$ atom full-pro-blog
```

### ファイル名のコピー
TreeViewにあるコピーしたいソースの上で`ctrl + m`などでファイル名をコピーします。
すると、`2017/04/test/index.js`などがコピーできます。


### スクリプトの作成
Clipyでスニペット`<script src="http://gist-it.appspot.com/github/nishina555/full-pro-blog/blob/master/`を登録してあるので、末尾に先ほどコピーしたファイル名を貼り付けます。そのあと`?footer=0"></script>`のスニペットを貼り付けます。
(順番的には「ファイル名貼り付け->文頭のスニペット貼り付け->文末のスニペット貼り付け」の順番がいいと思います。)

最終的には以下のようになります。

```
<script src="http://gist-it.appspot.com/github/nishina555/full-pro-blog/blob/master/2017/04/test/index.js?footer=0"></script>
```
あとはブログに貼り付ければOKです。

# 参考
- [gist-it](http://gist-it.appspot.com/)
