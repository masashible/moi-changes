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
#### 参考
https://recooord.org/fadein-window-scroll/

![image](https://user-images.githubusercontent.com/26806928/97775786-b62f3400-1ba6-11eb-9dd8-babbfa4ad89c.png)
- 外観 >> テーマエディタ >> style.css にアニメーション前後のクラスを作成(名前がぶつからないようbefore_floatなどとした)
- ページ全体において `before_float` が画面内にきたら `after_float` を付与するスクリプトを追加。

## ふわっと上がってくるアニメーション(トップページ)
## メニューがゆっくり開く
