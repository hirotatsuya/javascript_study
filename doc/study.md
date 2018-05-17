# 新入社員向け勉強会
  - JavaScriptについて

## JavaScriptとは
- WEBページに動きを付けるもの

## JavaScriptを書いてみよう
- 変数
  - データにつけるラベル
  - var
  - 種類
    - 文字列
    - 数値
    - 真偽値
    - オブジェクト
      - 配列
      - 関数
      - 組み込みオブジェクト
    - undefined
      - 定義されていない
    - null
      - 何もない
- 数値
  - 整数値
  - 実数値
  - マイナス値
- 演算子
  - 四則演算
    - +, -, *, /, %
  - 代入演算子
    - +=, -=
  - 単項演算子
    - ++, --
- 文字列
  - 表現方法
    - ', "
  - 特殊文字
    - \n, \t, \', \"
  - 文字列結合
    - +
- 条件分岐
  - if, else
  - 比較演算子
    - < >, <= >=, ===, !==
  - 論理演算子
    - ||, &&
- 三項演算子
- switch
  - switch, case, break, default
- 繰り返し文
  - for
    - break
      - ループを抜ける
    - continue
      - ループを一回スキップする
  - while
    - 前判定
  - do~while
    - 後判定
- 命令
  - alert
  - confirm
    - true / falseが返る
  - prompt
    - 値 / nullが返る
- 関数
  - 複数の処理をまとめて名前を付けたもの
function 関数名 (引数) {
  処理
  return 返り値
}
- ローカル変数
  - 関数内で定義した変数はその中でしか使えない
- 無名関数、匿名関数
var hello = function () {
  return "hello";
}
- 即時関数
(function () {
  console.log("hello")
})()
  - 変数を安全に使うために、変数をローカル変数にする
- タイマー処理
  - setInterval
  - setTimeout
    - clearTimeout
- 再帰関数
  - 関数の処理に自身の関数呼び出しを行う
var i = 0
function show () {
  console.log(++i)
  var tid = setTimeout (function () {
    show ()
  }, 1000)
  if (tid > 5) {
    clearTimeout(tid);
  }
}
show(i)
- 配列
  - グループ化されたデータ
var array = [1, 2, 3]
- オブジェクト
  - 名前と値のペアのグループ化
var object = {
  name: "tatsuya",
  age: 23
}
object.name, object["name"]
- 組み込みオブジェクト
  - 予め、JavaScriptが用意しているオブジェクト
  - String, Array, Math, Dateなど
  - オブジェクトでもリテラルでも使える
var s = new String("aaa")
var array = new Array(1, 2, 3)
  - Math
    - Math.PI
    - Math.floor(10.0)
    - Math.random()
  - Date
var date = new Date()
- DOM
  - ブラウザのいろいろなものにJavaScriptかアクセスできる
  - windowというオブジェクトをJavaScriptから使うことができる
console.dir(window) // オブジェクトのプロパティを見れる
console.log(window.outerHeight) // ブラウザの高さにアクセスする
  - 今見てるページから別のURLのページに移動する
window.location.href = 'https://hirotatsu.site'
  - window.document
    - 今開いているページのオブジェクト
    - windowは省略可能である
      - documentのみでOK
    - documentを操作することにより動的にページの一部を書き換えたり新しい要素を使いしたり出来る
- DOM
  - documentにアクセスするための様々な命令
  - 「DOMをいじる」、「DOMを操作する」というのは、documentオブジェクトに命令をして今開いているページを動的に変えることを言う
  - 古いブラウザだと、命令が異なる場合があるので注意
- DOMアクセス
  - ブラウザはHTML、CSSを読み込んだ後に、それぞれの要素をツリー構造で展開していく
    - 開発者ツールのElementsで確認
  - html要素の子要素としてhead要素とbody要素があり、body要素の子要素としてh1やpがある
  - DOMをいじるには要素のツリー構造を意識する
  - 流れ(既存の要素)
    - 要素の取得
    - domの操作
  - 取得
    - document.getElementById('aaa')
  - 操作
    - 書き換え
    - textContent = 'bbb'
  - 流れ(新しい要素)
    - 要素の作成
    - 操作
  - 作成
    - document.body.appendChild()
    - document.createElement('p')
    - document.createTextNode('Hello')
var greet = document.createElement('p')
var text = document.createTextNode('Hello')
document.body.appendChild(greet).appendChild(text)
- イベントの設定
  - ページ内の要素にイベントを設定する
  - addEventListener('イベント', function)

## JavaScriptの現在と今後
- https://qiita.com/shibukawa/items/19ab5c381bbb2e09d0d9

## ECMAScriptとJS
- https://app.codegrid.net/entry/ecmascript-1
- MozillaがJSの仕様を策定
- Ecma InternationalでECMAScriptとして標準化


