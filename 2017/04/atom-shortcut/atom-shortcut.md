# atomのショートカットまとめ

## Create installed packages list
```
apm list --installed --bare > packages.txt
```

## Install packages
```
apm install --packages-file packages.txt
```

## Tips
### shortcut
- プロジェクト内のファイル検索: ctrl + shift + f
- ファイルの検索: ctrl + t
- ディレクトリ画面のトグル操作: ctrl + \
- ターミナルを新しいタブで起動(packages -> tearm3): ctrl + alt + T
- 矩形選択: ドラッグして行を選択 -> shift + alt + 矢印
- ターミナル関係(platformio-ide-terminalを利用)
    - 起動 ctrl + `
    - 新規作成 command + shift + t
    - 削除 ctrl + shift + x
    - 移動 command + shift + j(or k)

### replace
- 全ての行頭に文字を挿入する(正規表現にチェックをつける)
    - 置換前: ^(.)
    - 置換後: XXXX $1
- 全ての行末に文字を挿入する(正規表現にチェックをつける)
    - 置換前: $
    - 置換後: XXXX
- 行削除
    - 置換前: ^\n
    - 置換後: 空白
