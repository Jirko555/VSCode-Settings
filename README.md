# Visual Studio Codeの環境構築

VSCodeの設定は「settings.json」に書き込まれる。<br>
このファイルを共有すれば、どこでも同じ設定で使えるようになる。

参考：「[どこでも同じ設定でVisualStudioCodeを使う方法](https://qiita.com/canpok1/items/a7c4c96e3c1c2a1cc532)」

## 設定方法

VSCodeをインストールしたら、settings.jsonを下記フォルダに入れるだけ。<br>
C:\Users\ユーザ\AppData\Roaming\Code\User\settings.json

## 利用プラグイン
- [**Auto Rename Tag**](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)<br>
【必須】開始タグを修正した時に、自動的に対になる終了タグを修正してくれる。  

- [**Autoprefixer**](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer)<br>
ベンダープレフィックスを必要に応じて、自動で付けてくれる。対象ブラウザの指定もできる。<br>
npmパッケージの「PostCSS」のプラグイン「Autoprefixer」で代用できる。<br>
gulp用プラグインの「gulp-autoprefixer」はメンテされておらず、古いので使わない。

- [**Bracket Pair Colorizer**](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)<br>
【必須】`{}` `[]` `()`などの対応する括弧を色分けしてコードの視認性を高める。

- [**change-case**](https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case)<br>
文字列のフォーマットを変換してくれる拡張機能。<br>
コマンドパレット`Ctrl + Shift + P`で`change case`を入力して選択する。

|  フォーマット  |  変換結果  |
| ---- | ---- |
|  title  |  `Visual Studio Code`  |
|  kebab  |  `visual-studio-code`  |
|  camel  |  `visualStudioCode`  |
|  pascal  |  `VisualStudioCode`  |
|  constant  |  `VISUAL_STUDIO_CODE`  |
|  dot  |  `visual.studio.code`  |
|  path  |  `Visual/studio/code`  |

- [**Color Highlight**](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)<br>
【必須】`#000000`などのカラーコードの色を可視化してくれる。エディタ上で色を確認できる。

- [**CSS Peek**](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)<br>
HTMLのclassやidから元のCSSを確認・編集できる。

- [**CSScomb**](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-csscomb)<br>
CSSの自動整形。整形の設定をカスタマイズすることもできる。<br>
npmパッケージの「PostCSS」のプラグイン「css-declaration-sorter」で代用できる。

- [**CSSTree validator**](https://marketplace.visualstudio.com/items?itemName=smelukov.vscode-csstree)<br>
CSSのコードをW3Cチェック（バリデート）する。<br>
CSSのエラー箇所も「問題パネル」に表示されるようになる。<br>
W3C公式はこちら→[http://jigsaw.w3.org/css-validator/](http://jigsaw.w3.org/css-validator/)

- [**Git History**](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)<br>
Gitのコミット履歴を表示する。<br>
参考：[VSCodeでのGitの基本操作まとめ](https://qiita.com/y-tsutsu/items/2ba96b16b220fb5913be)

- [**GitLens**](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)<br>
git blameをVSCodeで使えるようにするプラグイン。<br>
エディタのコード上にいつ・誰がコミットしたかの概要が表示されるようになる。

- [**Highlight Matching Tag**](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)<br>
【必須】HTMLの開始タグと対応する終了タグをハイライト表示してくれる。<br>
`highlightFromContent": true`にすると、内包コンテンツにカーソルを合わせた時、タグをハイライト表示してくれる。<br>

- [**HTML Preview**](https://marketplace.visualstudio.com/items?itemName=tht13.html-preview-vscode)<br>
【必須】VSCode内でリアルタイムプレビューしてくれる。軽い修正を確認するならブラウザよりも便利。

- [**HTMLHint**](https://marketplace.visualstudio.com/items?itemName=mkaufman.HTMLHint)<br>
【必須】HTMLの記述ミスや記述ルール違反などを、即座に教えてくれる拡張機能。<br>
統合ターミナルパネルの「問題」タブに出てくるのでわかりやすい。

- [**htmltagwrap**](https://marketplace.visualstudio.com/items?itemName=bradgashler.htmltagwrap)<br>
【必須】タグで囲みたい文字列を選択して`Alt + W`を押すと、タグが付与される。デフォルトでは`p`タグ。<br>
そのままの状態で`span`とキーを打てばspanタグに切り替わります。

- [**indent-rainbow**](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)<br>
【必須】インデントに色がついて、深さが変わるごとに違う色に変化するようになる。<br>
インデントがいくつ付いているのか一目でわかる。

- [**IntelliSense for CSS class names in HTML**](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)<br>
CSSのクラス名を補完してくれる。予めCSSファイルにclassを作っておけば、HTMLを記述しているときにclass名を補完してくれる。

- [**Japanese Language Pack for VSCode**](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja)<br>
【必須】VSCodeの日本語化。

- [**Live Sass Compiler**](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)<br>
【必須】SassをCSSに自動でコンパイルしてくれる拡張機能。出力内容の設定、フォルダ指定、ベンダープレフィックスの指定などができる。<br>
インストールするとVSCodeの下部に「Watch Sass」というボタンが追加される。このボタンを押すとSassファイルをWatchすることができる。<br>
パーシャルファイルのコンパイルもできる。

- [**Live Server**](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)<br>
【必須】HTMLのリアルタイムプレビューを行える拡張機能。VSCodeに簡易ローカルサーバを立てることができる。<br>
VSCode右下に表示される「Go Live」をクリックすると、ブラウザで http://127.0.0.1:5500/ が実行される。

- [**Path Intellisense**](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)<br>
【必須】相対パスを書く際にコード補完してくれる。

- [**Peacock**](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)<br>
【必須】プロジェクトごとにカラーを変える拡張機能。複数のプロジェクトを開いていても、判別しやすくなる。

- [**SCSS Formatter**](https://marketplace.visualstudio.com/items?itemName=sibiraj-s.vscode-scss-formatter)<br>
【必須】SCSSを自動整形してくれる。`Shift+Alt+F`がショートカット。

- [**vscode-icons**](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)<br>
エクスプローラーにアイコンがついて見やすくなる。

- [**zenkaku**](https://marketplace.visualstudio.com/items?itemName=mosapride.zenkaku)<br>
全角スペースがわかりやすく表示される。
