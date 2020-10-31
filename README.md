# moi-changes
お手伝いで変更した項目のメモ

## コンテンツ幅調整
### 内容
![image](https://user-images.githubusercontent.com/26806928/97775325-10c69100-1ba3-11eb-8e41-96e672076c0a.png)
- 元はオレンジの余白が左右になかったので追加した。
### 操作
![image](https://user-images.githubusercontent.com/26806928/97775448-0658c700-1ba4-11eb-8d6d-b5f45a093bab.png)
- 外観 >> テーマエディタ >> style.css におけるpost_contentクラスの子要素のp全てに 90%中央寄せを実施。

## ふわっと上がってくるアニメーション(固定ページ)
### 内容
<img width="374" alt="スクリーンショット 2020-10-31 18 17 14" src="https://user-images.githubusercontent.com/26806928/97775620-79af0880-1ba5-11eb-9a14-c4aa55852b43.png">

- 固定ページにおける各要素が画面内に入った時にフェードインしながら上がってくるように変更。
- 固定ページというのは wordpressにおける下記の部分。

![image](https://user-images.githubusercontent.com/26806928/97775522-b1698080-1ba4-11eb-9f55-843655cd8884.png)

### 操作
```
#### 参考
- https://recooord.org/fadein-window-scroll/
```

![image](https://user-images.githubusercontent.com/26806928/97775786-b62f3400-1ba6-11eb-9dd8-babbfa4ad89c.png)
- 外観 >> テーマエディタ >> style.css にアニメーション前後のクラスを作成(名前がぶつからないようbefore_floatなどとした)

![image](https://user-images.githubusercontent.com/26806928/97775845-35246c80-1ba7-11eb-9e7d-e53af1157653.png)
- ページ全体において `before_float` が画面内にきたら `after_float` を付与するスクリプトを追加。
  - 追加場所 外観 >> テーマエディタ >> js >> jscript.js

![image](https://user-images.githubusercontent.com/26806928/97775914-c562b180-1ba7-11eb-894c-12223c5de1e4.png)
- フェードインさせたいブロックに対して `before_float` クラスをつけてあげるとふわっとする。

## ふわっと上がってくるアニメーション(トップページ)
### 内容
- 上記のアニメーションをトップページにも設置
### 操作
- トップページはコンテンツビルダーで作られているのでcssをguiで付与するのができなさそうだった。
  - なのでトップページを開いた時にコンテンツビルダーで追加された要素に対して `before_float` を付与して回るスクリプトを設置。
  ![image](https://user-images.githubusercontent.com/26806928/97776020-7406f200-1ba8-11eb-8a99-04c569f8fccf.png)
  - 追加場所 外観 >> テーマエディタ >> js >> jscript.js

## メニューがゆっくり開く
### 内容
<img width="376" alt="スクリーンショット 2020-10-31 18 41 10" src="https://user-images.githubusercontent.com/26806928/97776071-bf210500-1ba8-11eb-9c6e-8019f521f92b.png">

- SPのメニューバーが開く速度をより遅く変更
- オーバーレイでバックが灰色に変わるのが早すぎるのでグラデーションするように変更

### 操作
```
#### 参考
- イージングの動きをいい感じにする
https://cubic-bezier.com/#.57,.17,.54,.92
- オーバーレイの色変更をゆっくりにする
https://qiita.com/gonshi_com/items/4ae066ef4bea6d519854
```

- メニューの開閉自体はテーマに実装されているものだったので変数をいじった。上のイージングのサイトを使うといい感じに調整できる。
![image](https://user-images.githubusercontent.com/26806928/97776201-7e75bb80-1ba9-11eb-9d9e-da111a11af56.png)
- 変更場所 外観 >> テーマエディタ >> css >> responsive.css

- オーバーレイに関しては、`display: none;` からのアニメーションなので `transition` を使わずにアニメーションを定義する。
![image](https://user-images.githubusercontent.com/26806928/97776253-ea582400-1ba9-11eb-885a-99ff054ae44b.png)
- 変更場所 外観 >> テーマエディタ >> css >> responsive.css
