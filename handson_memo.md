# vue.jsの内容

### head:について
- アプリケーションのメタ情報
- title => タブの名前が変わる

### css:について

- アプリ全体で使うstyleを定義するときに使う(global) 

## コードの書き方
- NuxtでもVue.jsのスタイルガイドに沿ってコードを書くべき
https://jp.vuejs.org/v2/style-guide/

## dataについて
- Componentsで使える変数みたいなもの.
- 正確にはreactiveなproperty。
- reactiveにさせるために、アローファンクションではなく、関数定義でないとダメ。
### reactiveとは
=>変更するとレンダリングされて、表示が更新される

## methodsについて
- 値を変更するだけでもOK
(= returnさせなくてもいい。)

## computedにいて
- 定義したものを実行した際に何かしら値を返す必要がある
(= 値をreturnさせる)
- methodsとの違いはキャッシュされること
- つまり、再描画されない

## ライフサイクル
- mount = 表示。
- mounted: DOMが表示された後になにかをしたい場合は、このライフサイクルを使う。

***computedとmethodsの違いは、値が変わったときに再描画されるかどうか***
## 属性のデータバインド
HTMLのattributeにバインドさせることで、定義したクラスなどを紐付けることができる

## v-if/v-show/v-for
### v-if
- 真偽値でデータの表示を切り替えるための関数
- DOMが完全に消え去る

### v-show 
- DOMが残り続ける
- display: none;されるだけ

### v-for
- リストレンダリングさせる

## props

- 外から受け取る値

## スロット
- 親要素に子要素のHTMLを渡すときに使う
- モーダルとかを使いたいときとか]
- nameによって名前をつければ、場所を指定できる。

# Nuxt.jsの内容

## assetsとstaticの違い

- assets => nuxt本体から読み込まれる
- static => webpack経由で読み込まれる

## pages

- ルーティングが勝手に生成される
- nuxtのメイン機能

## nuxt.config.js

- Nuxt全体を制御するファイル
- 変更したら再起動させる


## nuxt-link
- aタグだと、リロードになるが、nuxt-linkはjsでルーティングをするので、リロードされない

## titleTemplate
- タイトルのテンプレートを定義することができる

` titleTemplate: '%s - ポートフォリオ',`

## default.vue
- アプリ全体で反映されるstyleなどを管理
- <nuxt/>タグは必須
- ヘッダーやフッダーを定義すれば、それがページ全体で反映される

## asyncData
- Vueにはなく、Nuxt.jsのみに使える。
- これを使うとコンポーネントのHTML生成前に,asyncDataの中で外部APIを叩いたりでき、非同期処理が可能

## 総括
- NuxtはVueと違って、pagesファイルを作れば、それがそのままルーティングのパス名になる
- vue-routerの設定を書かなくていい。
(裏側でnuxtがよしなにやってくれる)

## 参考リンク
- [第1回Nuxt.jsハンズオン初心者編](https://takanorip.gitbook.io/nuxt-hands-on/)
- [ディレクトリ構造](https://ja.nuxtjs.org/guide/directory-structure/)
