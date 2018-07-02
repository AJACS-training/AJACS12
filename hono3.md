[[AJACS12]]

&size(25){続・遺伝子発現データベースを使い倒す};　　　　担当：小野浩雅

~目次
#contents


# &size(20){遺伝子発現データベース};に関する統合TV [#taf036b7]
- [[統合TVの「発現情報」タグをクリック！ >http://togotv.dbcls.jp/?category=%C8%AF%B8%BD%BE%F0%CA%F3]]


# マイクロアレイデータの準備 [#z6529d62]
サンプルデータとして、[[NCBI GEO>http://www.ncbi.nlm.nih.gov/geo/]]より取得した公共の遺伝子発現データ（[[GSE1657>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE1657]]:Adipocyte Differentiation[Homo sapiens]）を用いて、ヒトの脂肪細胞の分化前後で発現増加した上位500個の遺伝子群のリストを使います。
#ref(090907_sample_U133A_adipo.txt,left)
（右クリックして「名前を付けてリンク先を保存」してください。）
# [[&size(20){BioMart};>http://www.biomart.org/]] [#uebdfdc7]
&color(green){クリックしていくだけで自分の欲しいデータが手に入る};
- [[the Ontario Institute for Cancer Research (OiCR)>http://www.oicr.on.ca/]]と [[the European Bioinformatics Institute (EBI)>http://www.ebi.ac.uk/]] が共同で開発しているクエリ指向型データ管理システム。
- クリックしていくだけでデータの絞り込みやIDの対応表を簡単に作ることができる優れもの。



## 【実習】BioMartを使って、マイクロアレイデータのIDに対応したGO termのリストを取得する [#a83d5bfe]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090225.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.biomart.org/>http://www.biomart.org/]]を開きます。
- 2.リスト中の[[Ensembl>http://www.ensembl.org/biomart/martview]]をクリックします。
- 3. 「-CHOOSE DATABASE-」のプルダウンメニューを「Ensembl 55」に設定します。
- 4. 「-CHOOSE DATASET-」のプルダウンメニューを「Homo sapiens genes (GRCh37)」に設定します。
- 5. 左端の「Filters」をクリックし、出現する「GENE」の＋ボタンをクリックして展開します。
- 6. 「ID list limit」にチェックを入れ、「Affy hg u133a ID(s)」を選択し、「参照」ボタンを押して先ほど保存した「090907_sample_U133A_adipo.txt」を選択します。
- 7. 「Attributes」をクリックして、「GENE」のなかの「Ensembl Gene ID」、「Ensembl Transcript ID」のチェックをはずします。
- 8. 続いて、「EXTERNAL」の＋ボタンをクリックし、「 go biological process」中の「Gene Ontology Accession」にチェックを入れます。
- 9. 左端上部の「Count」をクリックすると、これまで設定した条件に該当する数がわかります。（今回の設定では408 / 44285 Genes）
- 10. 「Results」をクリックし、「Export  all results to」を「Files」（ファイル容量が大きい場合は「Compressed file(.gz)」を選択するとよい）と「TSV」（タブ区切りテキスト）を選択し、「Go」をクリックします。
- 11. 「mart_export.txt」というファイルがダウンロードされるので、デスクトップに保存し、「090907_U133A_adipo_GO.txt」とファイル名を変更します。

うまくダウンロードできない場合は下記のファイルを使用してください。
#ref(090907_U133A_adipo_GO.txt,left)
（右クリックして「名前を付けてリンク先を保存」してください。）


# [[&size(20){GO Terms Classification Counter (CateGOrizer)};>http://www.animalgenome.org/bioinfo/tools/countgo/]] [#k08f6dac]
&color(green){マイクロアレイデータの特徴をGO termを使って概観する};

- [[GO Terms Classification Counter (CateGOrizer)>http://www.animalgenome.org/bioinfo/tools/countgo/]]はマイクロアレイ実験などで得られた発現変動のあった遺伝子群に付けられたGO termリストのファイルをuploadすると分類して可視化（集計表とパイチャート）してくれるツール。

## 【実習】GO Terms Classification Counter (CateGOrizer) を使ってマイクロアレイデータの結果の解釈をする [#qdf3a83c]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090806.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.animalgenome.org/bioinfo/tools/countgo/>http://www.animalgenome.org/bioinfo/tools/countgo/]]を開きます。
- 2.「Click to Start」をクリックします。
- 3.「Your GO file to upload」にさきほどDLした「&ref(090907_U133A_adipo_GO.txt);」を指定します。
- 4. 「For security reasons, type the letters from the image on the left into the box next to it」の下に表示されている画像の文字を入力し、「Upload file」をクリックします。
- 5.「Your Email」に自分のメールアドレスを入力します（必須）。計算が終わるとメールが届きます。
- 6. 「Choose a GO classification」で「GO_Slim2」を選択します。「Choose a counting method」で「Count single occurances」を選択し、「Continue」をクリックします。
- 7. しばらく待つと結果が表示されます。
- 8. どのような生物学的機能に関する遺伝子群がリストに含まれていたでしょうか。


# [[&size(20){Reactome};>http://www.reactome.org/]] [#h1efcca2]
&color(green){マイクロアレイデータの特徴を遺伝子機能やパスウェイ情報を使って概観する};
- ヒトの生体中での反応やパスウェイを整備したデータベース。
- 収録されている情報は、それぞれの分野の専門家が編集しているため、非常に信頼性が高い。
- 代謝パスウェイだけでなく、シグナル伝達や膜輸送、感染など様々なパスウェイが収録されている。

## 【実習】Reactomeを使ってマイクロアレイデータの結果の解釈をする [#od6d0761]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090508.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.reactome.org/>http://www.reactome.org/]]を開きます。
- 2.上部の「Tools」から「SkyPainter」をクリックします。
- 3. 「参照」をクリックして、&ref(090907_sample_U133A_adipo.txt);をアップロードします。
- 4.「Focus species」を「Homo Sapiens」に設定します。
- 5.「Paint!」をクリックします。
- 6.結果が表示されます。
- 7.GO Terms Classification Counter (CateGOrizer)で出力された結果とどこがどう違うか考えてみましょう。

# [[&size(20){【番外編】Human Protein Atlas};>http://www.proteinatlas.org/]] [#h1efcca2]
&color(green){さまざまなヒトの組織やガン細胞、細胞株におけるタンパク質の発現および局在を知る};
- タンパク質の発現および局在を、特異的抗体を用いて得られた免疫組織化学染色写真をもとに調べることができるデータベース。
- 2009年9月5日現在では8,832個の抗体および7,334,244枚の染色写真が閲覧可能。
- 蛍光抗体法による染色写真も充実。


## 【参考】Human Protein Atlasを使って組織・細胞におけるタンパク質発現情報を調べる [#e813b839]
[[統合TVで紹介していますので興味ある方はぜひご覧ください。>http://togotv.dbcls.jp/20090501.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
