2023-08-15 ~ 
「ゲームを作りながら楽しく学べる
HTML5＋CSS＋JavaScriptプログラミング[改訂版]」田中賢一郎 [著]

[サンプルプログラムのダウンロードサイト](http:future-coders.net)

## HTML入門
- DOM(Document Object Model)
  - 文書をオブジェクトとして扱うモデル
  - javaScriptからプログラムを使ってHTML文書をコントロールする方法
- documentオブジェクト
  - HTML文書がブラウザーに読み込まれると、その文書のhtml要素がdocumentという変数に保持される
- イベント
  - ページを読み込んだ
  - マウスが動いた
  - マウスがクリックされた
  - キーが押された
  - キーが離れた
  - ボタンがクリックされた
- イベントハンドラー
  - 何かしらの事象に応じて実行される関数
- デバッグのコツ
- ビジーループ

## CSS入門
- cascadeとは、滝が流れる、流れ落ちるというようなイメージを表している
- CSSは、適用した要素だけに有効になるのではなく、その子要素全体に適用される
- * ..全称セレクタ
- タイプセレクタ ..同じ種類のタグ
- #id ..idセレクタ
- .クラス名 ..クラスセレクタ
- ブロックレベル要素とインライン要素
- インライン要素 ..横方向に配置(親要素もしくはページ幅に到達すると改行)
  - ```<a>,<span>,<button>,<input>,<img>```
- ブロックレベル要素 ..矩形としての領域を確保し、縦方向に配置
  - ```<h1>,<h2>,<p>,<div>,<ol>,<ul>,<li>```
- ページレイアウトをするときは、まずブロックレベル要素を使って大まかなレイアウトを整え、その中にインライン要素を流し込んでいく
- ボックスモデル
  - margin,border,padding,height,width
  - ボックスの位置指定
    - position:absolute; を指定して、top,leftで親要素からの距離を指定
- スタイル
  - opacity ..透明度合い
  - line-height ..行間

## JavaScript入門
### 変数
- const,let
- 配列 [,,]
  - indexは0から始まる
  - 配列の要素の個数は、配列名.length

### 条件式を利用した処理の繰り返し
- for文
  - for(let i=0;i<10;i++){処理}
- isNaN(a) ..aが数字でないときにtrue ..is Not a Number
- 三項演算子
  - ?と:を組み合わせたもので、if ~ else 文のような処理を簡単に記述できる
  - (a===b)? trueのときの処理 : falseのときの処理;
- while文
  - while(ループ継続の条件式){処理}
- switch文
  - switch(式){
      case 値1:式1;break;
      case 値2:式2;break;
      case 値3:式3;break;
      case 値4:式4;break;
      default:式5;break;
     }
- continue,break
  - for文やwhile文といったループ処理において、その流れを変えるための命令
  
### 関数
- function 関数名 (引数1,引数2,...){処理;return 戻り値;} ..戻り値が不要な場合はreturn文を省略
- 変数のスコープ
  - 関数の中で宣言した変数は関数の中でしか使用できない(ローカル変数)
  - 関数の外で宣言した変数はどこからでも使用することができる(グローバル変数)
  - プログラムの規模が大きくなってくると、どこで何が行われているか把握するのが困難になってくる
  - ->グローバル変数の使用はできるだけ控え、主な作業はローカル変数ですませるようにする

### デバッグ
- デバッグツール
  - ステップイン
  - ステップオーバー
  - ステップアウト

### DOMの操作
- parentNode
- firstChild
- lastChild
- previousElementSibling
- nextElementSibling
- スタイルの変更
  - DOM要素.style.プロパティ名
  - cssと同じスタイル名が使えるが、JavaScriptでは-はマイナスと解釈されてしまうためキャメルケースで記述する
- classNameでクラス属性を指定できる
- 「演習」○✕ゲームの作成

### オブジェクトの操作
- プロパティ ..色、大きさ、重さなどの特徴のこと
- メソッド..オブジェクトに対して働きかける操作
- インターフェース ..メソッドの集合
- カプセル可 ..中で起きていることを隠すこと
- オブジェクトの作り方
  - オブジェクト = new 関数 (引数1,引数2...)
  - オブジェクトを作るための関数を「コンストラクタ」と呼ぶ
- オブジェクトのメソッドの呼び出し方
  - オブジェクト.メソッド()
  - メソッドを呼び出すことを「オブジェクトにメッセージを送る」と表現することもある
- プロトタイプ

## 組み込みオブジェクト
- JavaScriptに最初から用意されている関数やオブジェクト
  - タイマー
    - setTimeout(関数名,ミリ秒) ..ミリ秒後に関数を1回呼び出す
    - clearTimeout(timerId1) ..setTimeoutの処理を停止する。timerId1はsetTimeoutの戻り値
    - setInterval(関数名,ミリ秒) ..ミリ秒間隔で関数を繰り返し呼び出す
    - clearInterval(timerId2) ..setIntervalの処理を停止する。timerId2はsetIntervalの戻り値
  - Mathオブジェクト
    - Math.min(a,b)
    - Math.max(a,b)
    - Math.random()
    - Math.floor(n)
    - Math.ceil(n)
    - Math.round(n)
    - Math.sqrt(n) ..nの平方根を返す
    - Math.PI
  - Arrayオブジェクト
    - 配列名.length
    - 配列名.indexOf(検索対象) ..ないときは-1を返す。第2引数として検索開始位置を指定することも可能。
    - 配列名.lastindexOf(検索対象) ..うしろから探す
    - 配列名.splice(index,howMany) ..indexからhowMany個分の古い要素を取り除く。その位置に新しい要素を追加することもできる。
    - 配列名.sort(func) ..配列をソートする
    - 配列名.push(e1) ..配列の最後に要素e1を追加する
    - 配列名.pop() ..配列の最後の要素を削除
    - 配列名.shift() ..配列の先頭の要素を削除
    - 配列名.forEach(callback) ..配列の各要素を引数として、都度コールバック関数を実行。
      - コールバック関数とは、のちほど呼び出される関数で、事前に処理内容を定義しておくもの。
      - forEachで指定するコールバック関数は、Arrayの各要素を引数として、要素の回数分呼び出される関数。
    - 配列名.every(callback)
    - 配列名.some(callback)
    - 配列名.filter(callback)

### JSON記法
- Arrayを[]で、Objectを{}で記述
- 配列名=[{"プロパティ":値,"プロパティ":値},{"プロパティ":値,"プロパティ":値},{"プロパティ":値,"プロパティ":値}];

## Canvas HTML5の描画機能
### コンテキスト
```JavaScript
      let canvas = document.getElementById("canvas");
      ctx = canvas.getContext("2d");
```
- ctx.strokeStyle ..線や輪郭の色
- ctx.fillStyle ..塗りつぶしの色
- ctx.lineWidth ..線の幅
- ctx.lineCap ..線の終端の形状。butt,round,square
- ctx.shadowColor ..影の色
- ctx.shadowBlur ..影をぼかす範囲

### 描画の方法
- beginPath() ..パスをクリア
- moveTo ..筆をおろす場所を指定
- lineTo ..筆を動かす
- closePath() ..パスを閉じる
- stroke() ..描画、塗りつぶす場合はfill()
- strokeStyle ..線の色
- fillStyle ..塗りつぶしの色

- 矩形の描画
  - ctx.fillRect(x,y,width,height); ..(x,y)を左上とする幅width、高さheightの大きさの矩形を塗りつぶす
  - ctx.strokeRect(x,y,width,height); ..(x,y)を左上とする幅width、高さheightの矩形の枠線を描画
  - ctx.clearRect(x,y,width,height); ..(x,y)を左上とする幅width、高さheightの矩形領域を透明化

- 円の描画
  - ctx.arc(x,y,radius,startAngle,endAngle,anticlockwise);
    - x,y ..中心座標 
    - radius ..半径
    - startAngle,endAngle ..円弧を描き始める角度、円弧を描き終わる角度
      - 角度の単位はラジアン(360°を2πとする単位 | 360°=360*π/180=2πラジアン)
    - anticlockwise ..trueで反時計回り、falseで時計回り

## 文字
- ctx.fillText(text,x,y,maxWidth) ..(x,y)座標を起点としてtextを塗りつぶして描画。maxWidthで最大幅を指定できる。
- ctx.strokeText(text,x,y,maxWidth) ..(x,y)座標を起点としてtextの輪郭を描画。maxWidthで最大幅を指定できる。

## 画像
- ctx.drawImage(image,dx,dy)
- ctx.draiImage(image,dx,dy,dh)
- ctx.drawImage(image,sx,sy,sw,sh,dx,dy,dw,dh)
- d=destination ..描画対象となるCanvas
- s=source ..描画する元画像

## 座標系
- ctx.save() ..コンテキスト(座標系)を保存
- ctx.translate(100,100) ..座標系の原点をx方向に100，ｙ方向に100移動
- ctx.rotate(r) ..座標系をr回転
- ctx.restore() ..コンテキストをsave時に復元

## ゲームプログラミング

### SnakeBite風ゲーム

### 一般的なゲームプログラムの流れ
  1. 初期化
  2. キー入力判定
  3. 各種処理
  4. 描画更新
  5. GameOver ..でなければ2.に戻る

### 地雷除去ゲーム

### ブロック崩し

### テトリス

### 記憶ゲーム

