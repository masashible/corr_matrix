# About
`corr_matrix_4r` provides you easy data-reshaping for Researchers. When you want to create a Table like: "Means, Standard Deviations, and Intercorrelations", "Correlations among main variables", "Intercorrelations between Variables" you can use this ipynb.

なにかミスを見つけたら、ついったー @ryouen でお待ちしております！

# 使いかた
'anaconda'で'Jupyter Notebook'がインストールされている方は普通に使って下さい。
よくわからないけれど、とりあえず動かしたい！方向けの説明はこちら↓
## ① Google Colabを使ってみる
インストール不要かつ無料で使えるJupyter Notebookこと、Googleの Colabを使ってみて下さい。
https://colab.research.google.com/drive/
↑こちらからアクセスできます。

## ② ノートブックをアップロード
Googleアカウントにログインされた状態で↑にアクセスすると、
黄色い帯のポップアップに'GitHub'と書かれた場所があります。そこをクリックします。

Enter a GitHub URL に下記のURLを入力します。
https://github.com/ryouen/corr_matrix/blob/main/corr_matrix_for_researchers_210722.ipynb

入力し、Enterを押すと、灰色の帯が出現。その右端に矢印のついたアイコンがあります。
そのアイコン（新しいタブでノートブックを開く）をクリック。
ここまでで、このGitHubにアップロードした、ipynbがインストールできました。

## 動作確認
上の方のRuntime→Run all を実行します。アラートが出ますが、大丈夫だと思ったらRun Anywayを押します。
あとは説明や出力を読んでもらえれば、だいたい分かるかと思います。

## 自分のデータで実行したい
### ファイルのアップロード/読み込み
**Google Colab を利用し、自分のファイルをアップロードする場合は、次のセルのコメントアウトを外して、ファイルをGoogle Colabにアップロードできるようにする。**
と書かれた行を探します。比較的上の方です。そのコメントアウトを削除すると、ファイルがColabにアップロードできます。
コメントアウトを外した上で、前述と同じくRuntime→Run all を実行してみましょう。ファイルをローカルから選択でき、アップロードができます。（ただし、通常は途中：「デフォルトは、p値と、下三角行列のみ出力」の直下でエラーが出るはずです）

**ファイルが読み込めない場合（セル[3]までにエラーが出る場合）は、filename='あなたのアップロードしたファイル名。拡張子つき'のようにしてください。また、xlsxファイルではなくcsvをアップロードしていることを確認してみてください**

### 準備：項目を並べる順番を決め、必要ない項目名を除外する
上述のように記載のあるセルを探します。
その下の **「次のリストに入れた順序で、項目が出力される」** と書いてある行を探します。
その行のひとつ前に書かれたものが、あなたがこれから出力する項目名です。
この項目名と同じものを、
**「次のリストに入れた順序で、項目が出力される」の記載のすぐ次のセルの中に**

**lst = ['項目１', '項目2', ...]**

**となるように貼りつけます。このときの順番で出力の順序が決められます。不要なカラム名は削除してください。**
難しい場合は、元のアップロードするcsvの方に変更（左から順に必要なデータのみを並べる。不要なカラムは削除する）を加え、
**次のリストに入れた順序で、項目が出力される**
という記載の次のセルを、全てコメントアウトもしくは削除するとよいでしょう。

### 出力
上記の手順が終わったら、もういちど、Runtime→Run allを実行してみましょう。
ファイルも再度アップロードする必要があるかもしれません。
出力を確認するには
**デフォルトは、p値と、下三角行列のみ出力**
と記載のあるセルを探してください。その直後に出力されているデータフレームが、
通常あなたが必要なものです。

### 出力ファイルのダウンロード
'df_describe_p.csv'というファイル名で出力をしています。
Google Colabの左側（画面左上端）に、フォルダのアイコンがあります。
そのフォルダのアイコンをクリックすると、あなたがアップロードしたデータも含めて、
Colabにアップロードされているファイルの一覧が閲覧可能です。

'df_describe_p.csv'をクリックすると、灰色の帯の右端に︙マークが現れます。
そちらをクリックしてダウンロード/Download を押すと、csvのダウンロードが可能です。

### 出力ファイルの整形
このGitHubにも同じものをアップロードしていますが、
本ファイルの一番下「アウトプット・整形」から、Excelファイルをダウンロードできます。
さきほどダウンロードしたcsvファイルを、Excelの記載に従って貼付することで、
あなたのほしいものが得られます。



# Jupyter_Notebook
Jupyter Notebook 

### corr_matrix_for_researchers_210722.ipynb
Some explanation is in Japanese.

### Final_Output_Sample.xlsx
Copy and Phaste from your output csv to get what you want.
