---
theme: seriph
background: https://cover.sli.dev
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  PHPカンファレンス福岡2024 / LTアワー　　
  https://phpcon.fukuoka.jp/2024/
drawings:
  persist: false
transition: slide-left
title: "runn開発者会議福岡2024"
mdc: true
addons:
  - "@katzumi/slidev-addon-qrcode"
  - "slidev-addon-components"
  - "slidev-addon-rabbit"
---

# runn開発者会議福岡2024

[PHPカンファレンス福岡2024 / LTアワー](https://phpcon.fukuoka.jp/2024/)　May 22, 2024.  
v0.0.5  
@katzumi(かつみ)

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/k2tzumi/runn-developers-conference-fukuoka-2024-keynote-speech" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
layout: two-cols-header
---

# 自己紹介

katzumi（かつみ）と申します。

「障害のない社会をつくる」をビジョンに掲げている「りたりこ」という会社に所属しています
<a href="https://litalico.co.jp/">
<img src="https://litalico.co.jp/ogp.png" class="w-40" />
</a>

以下のアカウントで活動しています。

::left::

<div class="float-left">
<img src="https://pbs.twimg.com/profile_images/1768978237210935296/idy9J4l6_400x400.jpg" class="rounded-full w-40 mr"/>  
<simple-icons-x /> <a href="https://twitter.com/katzchum">katzchum</a></div>  
<QRCode :width="180" :height="180" value="https://twitter.com/katzchum" color="4329B9" image="Logo_of_X.svg" />

::right::

<img src="https://avatars.githubusercontent.com/u/1182787?v=4" class="rounded-full w-40 mr-12"/>

<logos-github-octocat /> [k2tzumi](https://github.com/k2tzumi)  
<simple-icons-zenn /> [katzumi](https://zenn.dev/katzumi)  

<br />

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: default
transition: fade-out
---

# runn開発者会議とは？
runn とは API シナリオテストツールの OSS です。その OSS の開発者会議となります

PHPerKaigi2023 から始まるカンファレンスの廊下で繰り広げられるオフラインによる議論の場です。
 
<Tweet id="1184741983585103874" />

runn という API シナリオテストツールの開発者である @k1Low さんと  
私 @k2tzumi がツールの開発の方向性等を熱く議論しています

---

# runn開発者会議の歴史
今回は 6 回目

1. [PHPerKaigi2023](https://zenn.dev/katzumi/articles/runn-developers-conference-in-phperkaigi2023)
1. [PHPカンファレンス福岡2023](https://zenn.dev/katzumi/articles/phpcon-fukuoka-2023-talk-impression)
1. [Go Conference mini 2023 Winter IN KYOTO](https://kyotogo.connpass.com/event/285351/)
1. [PHPerKaigi2024](https://phperkaigi.jp/2024/)
1. [Go Conference 2024](https://gocon.connpass.com/event/314876/)
1. <span v-mark.circle.red="1">[PHPカンファレンス福岡2024](https://phpcon.fukuoka.jp/2024/)</span>

---

# runnを取り巻く状況

1. 精力的なバージョンアップ  
2. コントリビューター拡大  
3. GitHub Start 数増加  
4. メディア＆ブログ掲載拡大  
5. ライブラリとして採用され始める

---

# 精力的なバージョンアップ
v0.72.0 → v0.113.2

カンファレンス駆動開発にも支えられています

<Tweet id="1683029488907722752" scale="0.4" />

---

# コントリビューター拡大  
いつもありがとうございます！

新たに 5 名のコントリビューターが増えました。  
特に積極的に機能追加していただいている HaRu さんありがとうございます！


---

# GitHub Start数増加  
3 倍ぐらいに増えた

100 ちょっと　→　384

<Transform :scale="0.6">  
  <img src="/star-history-2024621.png" />
</Transform>

---

# メディア＆ブログ掲載拡大  
色々取り上げていただきありがとうございます！

- [APIテストツール４選！開発者が語る各ツールの特徴と魅力](https://trident-qa.connpass.com/event/299308/)  
runnm, Scenarigo, Karate, Postman の開発者が集まるという貴重な会でした
- [yamlでテストシナリオを書いてそのまま実行までできるAPIテストツールの新星 “runn” を試してみた](https://dev.classmethod.jp/articles/trying-runn/)  
クラスメソッドさんに取り上げられて一気に認知が広まった感
- [CI/CD Test Night #7](https://testnight.connpass.com/event/311263/)  
開発者２人が同じイベントに呼ばれるというありがたいお話を頂きました

---

# ライブラリとして採用され始める
幅広いアプリケーションに組み込まれていました

<Tweet id="1709187452144095572" scale="0.5" />

---

# ライブラリとして採用され始める
幅広いアプリケーションに組み込まれていました

<Tweet id="1763704537075073184" scale="0.5" />

---

# 本を執筆しました
一人アドベントカレンダーから爆誕

<Tweet id="1758870210076098610" scale="0.5" />

---

# 注目機能＆改善（1/3）

- [Add jq path syntax support for excluding comparison targets in diff()/compare() functions.](https://github.com/k1LoW/runn/pull/936)  
diff 関数の比較対象を除外するパターンに jq コマンドのパス構文をサポートしました
- [Support --env-file option for loading environment variables from a file.](https://github.com/k1LoW/runn/pull/945)  
runn 実行時の環境変数をまとめて env ファイルで指定可能になりました
- [Add exec.background: for executing commands in the background. ](https://github.com/k1LoW/runn/pull/943)  
コマンド実行時にバックグラウンド実行が可能となりました
- [Replace the buildTree() method by injected expr tracing approach](https://github.com/k1LoW/runn/pull/917)  
yaml フォーマット内の評価式のコメント構文で `#` が使えなくなりました  
`//` をご利用ください
- [Add dump.disableTrailingNewline: for disabling trailing newline in dump output](https://github.com/k1LoW/runn/pull/931)  
dump runner 実行時に最後の文字列に改行コードをつけるようにしました。  
オプションで以前の挙動に戻すこともできます

---

# 注目機能＆改善（2/3）

- [Use github.com/pb33f/libopenapi](https://github.com/k1LoW/runn/pull/827)  
OpenAPI の validator を行うライブラリを pb33f に変更しました
- [Add builtin functions for ID generation to faker.*](https://github.com/k1LoW/runn/pull/811)  
faker で UUID を生成するビルトイン関数が増えました
- [Add --attach option for debugging or step execution](https://github.com/k1LoW/runn/pull/817)  
ステップ実行がサポートされました
- [Support gist://](https://github.com/k1LoW/runn/pull/787)  
gist として登録された runn ブックを直接実行できるようになりました
- [Keep loaded OpenAPI documents](https://github.com/k1LoW/runn/pull/769)  
OpenAPI の仕様書をキャッシュするようにしてパフォーマンス改善しました
- [Support using YAML's anchors and aliases in runbooks](https://github.com/k1LoW/runn/pull/722)  
run ブックの yaml フォーマットで anchor 指定が可能になりました

---

# 注目機能＆改善（3/3）

- [Introduce pick() expr built-in function](https://github.com/k1LoW/runn/pull/714)  
ビルトイン関数に pick が追加されました。json のノードを一部のみにできます
- [Introduce omit() expr built-in function](https://github.com/k1LoW/runn/pull/719)  
ビルトイン関数に omit が追加されました。json のノードを省略できます
- [Add runbook ID (Full) and elapsed time to result.json](https://github.com/k1LoW/runn/pull/678)  
シナリオ実行時にユニークな ID を降るようになりました
- [Support labels: section in runbooks](https://github.com/k1LoW/runn/pull/683)  
ラベル指定して実行対象の絞り込みができるようになりました
- [Add header for trace](https://github.com/k1LoW/runn/pull/645)  
リクエストにトレース用のヘッダーを付与できます
- [Append use cookie option](https://github.com/k1LoW/runn/pull/559)  
Cookie をサポートしました

----

# 議題
今回の主に話をしたいこと([runn開発者会議スレッド](https://zenn.dev/katzumi/scraps/f00a2d3e177b77) より抜粋)

- [2024年中にはv1にしたい](https://zenn.dev/katzumi/scraps/f00a2d3e177b77#comment-3343da51e61f06)
- [失敗したシナリオを一覧表示したい](https://zenn.dev/katzumi/scraps/f00a2d3e177b77#comment-7054a8d20effdf)
- [ランブック単位でのクリーンアップ処理](https://zenn.dev/katzumi/scraps/f00a2d3e177b77#comment-47ab501dd23dd2)
- [シナリオテスト自体をドキュメント化したい](https://zenn.dev/katzumi/scraps/f00a2d3e177b77#comment-6b6d90f619fc43)
- [Property based testingをしたい](https://zenn.dev/katzumi/scraps/f00a2d3e177b77#comment-9ab29ee99988a8)

---

# 最後に
絶賛募集中です

We're contributing.

---
layout: end
---

ご清聴ありがとうございました