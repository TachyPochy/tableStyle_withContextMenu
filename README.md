# Excel で、表の修飾を CSS で書き出すアドイン

## はじめに

　同様のコンセプトをもつツールは多いと思いますが、nth-child でセルを指定するのが特徴です。

　以下のような用途で使用します。reStructuredText だけでなく、Markdown、textile でも使えるかもしれません。

[Sphinx、表の一部を装飾する（一部だけスタイルを変えたい） - Qiita](https://qiita.com/Tachy_Pochy/items/648dc5252a1916dabd94)

## 使い方

　スタイルを適用したセルの範囲を選択し、コンテキストメニューから CSS to Clipboad を選択してください。

## サンプルの出力結果

```html
    <style type='text/css'>
        #theTableBlock table th:nth-child(1) td:nth-child(1) {
            color: White;
            background-color: Red;
        }
        #theTableBlock table tr:nth-child(1) td:nth-child(2) {
            background-color: Yellow;
            font-weight: bold;
        }
        #theTableBlock table tr:nth-child(2) td:nth-child(3) {
            color: White;
            background-color: Blue;
            font-style: italic;
        }
    </style>
    <div id='theTableBlock'>

        <!-- TODO : write your table tag code here -->

    </div>
```

## 注意

　一行目は th として扱います。
