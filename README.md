# おしゃれなソーシャルメディアボタン

[デモサイトはこちら](https://taku-web3.com/project/social-media-button/index.html)


## 改めて学んだこと
- box-sizing: border-box;
- display: grid;
- place-items: center;
- float: left;
- overflow: hidden;
- display: inline-block;

***

### box-sizing: border-box;について
CSSのbox-sizingは要素の幅と高さにpaddingとmarginを含めるかどうかを指定する。
初期値では含まない。その場合は、要素の幅を100％としたときに、paddingとmarginの分だけはみ出る。
border-boxを使う場合は、基本的にはすべての要素に対して指定してしまうのが楽。

***


### display: grid;について
要素を簡単に中央寄せする方法
```css
body {
  display: grid;
  height: 100%;
  width: 100%;
  place-items: center;
  /* justify-content: center; */
  /* align-items: center; */
}
```
place-itemsプロパティを使うことで、justify-contentとalign-itemsを省略して書ける。

***

### float: left;について
floatプロパティは、イメージとして画面から「浮いてしまう」ような状態。
floatプロパティを適用していない要素が間に入り込んでしまう。


### overflow: hidden;について
overflow: hidden;を使うことで初期状態は文字を隠している。
ボタンとアイコンのサイズを同じにして、文字が入る余白をなくすことで実装できる。


### displayの基本

#### - display: block;
要素が縦に並ぶ
幅と高さを指定することができる。
余白も上下左右に付けられる。

text-alignやvertical-alignを指定しても、要素が中央寄せにはならない（要素の中の文字は中央寄せになる）


#### - display: inline;
主に文章の一部として使う。
要素の間には改行が入らない
基本的にはblockの中で使われる
幅と高さを指定できない
左右の余白（margin, padding）は自由に指定できる
上下のmarginは使えない
上下のpaddingは使えるがレイアウトが崩れる可能性が高い
text-alignが指定できる（親要素に対して指定する）
vertical-alignを指定するときには、親要素ではなくinlineの要素に対して直接指定すればOK


#### - display: inline-block
inlineとblockの間を取ったようなもの
要素の並び方はinline的で、要素の中身はblock的な性質を持つ
改行が入らず横に並ぶ
幅・高さの指定ができる
上下左右の余白の指定もできる
text-alignとvertical-alignの指定もできる
基本的にモノを横に並べたいときに使える


#### - display: none
非表示にする（読み込みが早くなるわけではない）