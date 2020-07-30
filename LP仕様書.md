# LP仕様書

###### tags: `tm_制作` `ナレッジ共有` `仕様書`

デザイン・コーディングのガイドラインです。
厳密な設定はありませんが、最低限守る必要のある項目のみ記述しています。
> 2020/10/1以降のページデザイン(mockup)
> https://www.figma.com/proto/LO3EA8dnTXPK5pAilz72ny/joggo-v03?node-id=57%3A0&viewport=417%2C7389%2C1&scaling=scale-down

## デザイン
納品形態 → Figma/Ai/Ps(いずれか)
※データは埋め込まずリンクして、フォルダ納品をお願いします。


### グリッド
ページテンプレートは、Bootstrapを独自に改良したグリッドテンプレートを使用しています。
※ベースはグリッドデザインですが、フレックスデザインも可

| デバイス | グリッドレイアウト | MEMO |
| -------- | -------- | -------- |
| SP | http://gridcalculator.dk/#/750/2/32/32 |  |
| TB | http://gridcalculator.dk/#/1536/3/32/32 |  |
| PC | http://gridcalculator.dk/#/1152/12/32/16 |  |

### テンプレート
`newitem202008b.ai`[[ここからDL]](https://drive.google.com/file/d/15IXQG3wk89QoRF276l_8s4kvj6k6d6Ov/view?usp=sharing)
> バナーは全てLPのMVと同一、もしくは似通ったビジュアルにする必要があります。

| アートボード名 | 用途 | 注意事項 |
| -------- | -------- | -------- |
|banner-newitem202008b__LINE01|LINE用||
|banner-newitem202008b__twitter01|Twitter||
|banner-newitem202008b__google&yahoo01|[レスポンシブディスプレイ広告](https://support.google.com/adspolicy/answer/6363786)_1|2とセット。<br>テキスト面積が全体の 20% を超えると審査が通らない|
|banner-newitem202008b__google&yahoo01--1x1|レスポンシブディスプレイ広告_2|1とセット。<br>300x300pxより大きいと登録不可(Yahoo!)<br>可読性が低いので文字は不使用|
|banner-newitem202008b__gdn&ydn--300x250|[ディスプレイ広告](https://support.google.com/adspolicy/answer/176108?hl=ja)|最も掲出頻度が高い|
|banner-newitem202008b__gdn&ydn--728x90|ディスプレイ広告||
|banner-newitem202008b__gdn&ydn--160x600|ディスプレイ広告||
|banner-newitem202008b__gdn&ydn--468x60|ディスプレイ広告||
|banner-newitem202008b_gdn&ydn--320x50|ディスプレイ広告|モバイルのみ。テキストを入れる場合、最小10pxが目安（12px以上が望ましい）|
|banner-newitem202008b__gdn&ydn--320x100|ディスプレイ広告|モバイルのみ。テキストを入れる場合、最小10pxが目安（12px以上が望ましい）|
|banner-newitem202008b__instagram01--4x5|IGフィード・FBフィード|テキスト面積が全体の 20% を<br>超えると審査が通らない(FB)|
|banner-newitem202008b__instagram01--9x16|IGストーリーズ||
|mv-frontpage-slider__newitem202008b--pc|トップページPC・TB||
|mv-frontpage-slider__newitem202008b--sp|トップページSP||
|side-banner__newitem202008b|サイドバー表示||
|PC__01|PCデザイン用レイアウト|アートボード1152px以上表示用になっています。|
|TB__01|TBデザイン用レイアウト|アートボードはRetina表示用になっています。|
|SP__01|SPデザイン用レイアウト|アートボードはRetina表示用になっています。|

### ルール
- フォントサイズ、マージンなどの数値において奇数を使用しない
- マージンは８の倍数が基本(2/4/8/12/16/24/32/48/64/128)
- 文字の取り扱いについては、スタイル（css）> フォントの項目を参照


## マークアップ

### レギュレーション・ルール
- HTML5
- SPファースト
- ライブラリ(js/css)は、既存で用意されているもの以外使用しない
- インデントは、2space(TAB使用禁止)

### テンプレート
`template-lp.html` :[[ここからDL]](https://drive.google.com/file/d/1_ENWM1rxFK5lm1dylrt5i8AUGaZ8oi7u/view?usp=sharing)
> ■CSSは、`<head>` の `<style>` に記述してください。
> ■ソースは
> ```
> <!------------- テンプレートはここから ------------->
> <!------------- テンプレートはここからここまで ------------->
> ```
> 内に記述をお願いします。


### 対応環境
| OS | 対応ブラウザ | バージョン |MEMO|
| -------- | -------- | -------- | -------- |
|Windows7,8,10|InternetExplorer11/Google Chrome/Microsoft Edge/Firefox|最新|IE11は最低限の対応でOK|
|MacOS 10.10~|Safari/Google Chrome/Firefox|最新||
|iOS|Safari/Google Chrome|iOS11~||
|Android|Google Chrome|ver.5~||

### ブレークポイント（BP）
| デバイス | BP | MEMO |
| -------- | -------- | -------- |
|SP|767px以下|デザインは<br>375x812をベース（Retina対応）|
|TB|991px~768px|デザインは<br>768x1024をベース(Retina対応)|
|PC|992px以上|デザインは<br>1152x1080をベース|
※テンプレートを参照してください。


### 使用可能ライブラリ
|項目|内容|MEMO|
| -------- | -------- | -------- |
|jQuery|v3.3.1||
|Wow.js|MITライセンス|https://wowjs.uk/|
|lazyload.js|ver.2.0.0|画像は背景画像を除き、FV以外の全ての画像にlazyload.jsを使用|
|animate.css|ver.3.7.2(cdn)|Wow.jsを動かすのに必要なライブラリです。|
|slick.js|ver.1.8.0||
|fontawesome.js(light/brands)|ver.5.5.0|https://fontawesome.com/icons?d=gallery&s=brands,solid&m=pro|

### アイコン
Font Awesome を必ず使用してください。（それ以外は不可）
#### 使い方
https://fontawesome.com/how-to-use/on-the-web/referencing-icons/basic-use
#### ローカル用
- Light : [ここからDL](https://drive.google.com/file/d/1G2qfbiqci5teBlOhGnFhNw2wIEPPe_bR/view?usp=sharing)
- Brand : [ここからDL](https://drive.google.com/file/d/1G2qfbiqci5teBlOhGnFhNw2wIEPPe_bR/view?usp=sharing) 
> デザイン用データでインストールしてお使いください。
> ページ内ではjsで変換されます。
> プロジェクト終了後はローカル端末から削除をお願いします。


### スタイル（CSS）


| 項目 | 内容 | MEMO |
| -------- | -------- | -------- |
|設計規則|BEM|ID不使用、シングルクラス、構造スタイル分離であること|
|接頭詞|全てのクラスはプロジェクトコードを接頭詞にすること|例）`newitem202008b-mv` |
||||


#### フォント
|項目|内容|MEMO|
| -------- | -------- | -------- |
|ファミリー|-apple-system,BlinkMacSystemFont,"Helvetica Neue",Arial,"游ゴシック体",YuGothic,"Yu Gothic M","游ゴシック Medium","Yu Gothic Medium","Hiragino Sans","ヒラギノ角ゴ ProN W3","Hiragino Kaku Gothic ProN",Meiryo,sans-serif|デザインによりWEBフォント使用可。common.cssに記述があるため、LPに記述は不要。※2020/10~はA1ゴシックStdNに変更になります。|
|サイズ|Default:16px(1.6rem) / 最小:12px(1.2rem)|ページ内は`rem`でサイズ指定してください。|
|カラー|Default:#333333|デザインにより変更可|
|line-height|1.75|px指定禁止|
|letter-spacing|0.05em|px指定禁止|
※2020/10~は上記の設定が変更になります。
