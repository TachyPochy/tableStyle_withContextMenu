## ツール

[TachyPochy/tableStyle_withContextMenu](https://github.com/TachyPochy/tableStyle_withContextMenu)

## はじめに

　同様のコンセプトをもつツールは多いと思いますが、nth-child でセルを指定するのが特徴です。

　以下のような用途で使用します。reStructuredText/Sphinx だけでなく、Markdown でも使えるかもしれません。

[Sphinx、表の一部を装飾する（一部だけスタイルを変えたい） - Qiita](https://qiita.com/Tachy_Pochy/items/648dc5252a1916dabd94)

## 対応

　以下の装飾に対応しています。

- 文字色
- 背景色
- 太字
- イタリック
- 下線

## 使い方

　スタイルを適用したセルの範囲を選択し、コンテキストメニューから CSS to Clipboad を選択してください。

![図3.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/37554/50551366-1b85-3cd6-4689-a424c9999c99.png)

## サンプルの出力結果

　クリップボードには、以下のコードが出力されます。HTML カラーコードは、可能なら色名に変換します。

```html
    <style type='text/css'>
        #theTableBlock table tr:nth-child(1) th:nth-child(1) {
            color: Red;
            background-color: Yellow;
        }
        #theTableBlock table tr:nth-child(1) td:nth-child(2) {
            background-color: Red;
            font-weight: bold;
        }
        #theTableBlock table tr:nth-child(2) td:nth-child(3) {
            background-color: Blue;
            font-style: italic;
        }
        #theTableBlock table tr:nth-child(3) td:nth-child(4) {
            background-color: #E6B8B7;
            text-decoration: underline;
        }
    </style>
    <div id='theTableBlock'>

        <!-- TODO : write your table tag code here -->

    </div>
```

## 注意

　一行目は th として扱います。HTML を書くなら &lt;thead&gt;〜&lt;/thead&gt; と &lt;tbody&gt;〜&lt;/tbody&gt; が必要です。

```html
        <table>
            <thead>
                <tr>
                    <th>Test</th>
                    <th>Test</th>
                    <th>Test</th>
                    <th>Test</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                </tr>
                <tr>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                </tr>
                <tr>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                    <td>Test</td>
                </tr>
            </tbody>
        </table>
```

### ブラウザでのレンダリング例

![図4.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/37554/9e876f1f-a31b-0391-f507-384ec8029f35.png)
