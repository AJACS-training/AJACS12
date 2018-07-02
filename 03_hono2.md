[[AJACS12]]

&size(25){遺伝子発現データベースを使い倒す};　　　　担当：小野浩雅

~目次
#contents

# &size(20){遺伝子発現データベース};に関する統合TV [#taf036b7]
- [[統合TVの「発現情報」タグをクリック！ >http://togotv.dbcls.jp/?category=%C8%AF%B8%BD%BE%F0%CA%F3]]

# [[&size(20){BioGPS};>https://biogps.gnf.org/]] [#t5ad14b0]
&color(green){ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース};

- [[BioGPS>https://biogps.gnf.org/]]はAffymetrix社製のマイクロアレイであるGeneChipを用いた遺伝子発現プロファイルのデータベース。
- [[GNF SymAtlas>http://symatlas.gnf.org/]][[【参考動画】>http://togotv.dbcls.jp/20070816.html]]のメジャーアップデート版。
- マウスのエキソンアレイのデータが追加されたので、遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。
- 検索した遺伝子に対して、種々の外部データベースに横断検索することができる。
## 【実習】BioGPSを使ってある遺伝子の発現プロファイルを調べる [#k6b911bc]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081004.html#p01]]、[[【講習会動画】>http://togotv.dbcls.jp/20090217.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[https://biogps.gnf.org/>https://biogps.gnf.org/]]を開きます。
- 2.骨格筋の分化決定遺伝子であるMyogenic differentiation 1(MyoD)の発現プロファイルを調べてみましょう。中央の検索窓に「myod」と入力し、「search」を押します。
- 3. 表示された検索結果をクリックします。
- 4. 最初はヒトのマイクロアレイデータが表示されます。
- 5. マイクロアレイデータ左上の「Human(4654)」をクリックするとマウスやラットを選択できるので、「Mouse(17927)」をクリックしてマウスのデータを表示できます。
- 6. MyoDはどの組織、細胞で強く発現しているでしょうか？
- 7. 右上の「default rayout」をクリックすると、検索した遺伝子に関するマイクロアレイデータ以外のデータが閲覧できますが、どのようなデータが閲覧できるのか調べてみましょう。
- 8. 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。


# [[&size(20){NCBI Gene Expression Omnibus (GEO)};>http://www.ncbi.nlm.nih.gov/geo/]] [#r6287e42]
&color(green){世界最大の遺伝子発現（[[マイクロアレイ>http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4]]）データベース（レポジトリ）};


## 【実習】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる [#a83d5bfe]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090213.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の右端にある画像をクリックすると、[[発現データの詳細をみる>http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&dataset=DEAryz&dataset=yyyzzz$&gmin=5173.000000&gmax=11680.000000&absc=&gds=2294&idref=161072_at&annot=Nanog]]ことができます。
- 6. 「Display values」をクリックすると、発現値を一覧できます。
- 7. [[このサンプル>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。
- 8. ページ下部の「samples」に列挙された[[リンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。
- 9. [[リンク先のページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]の中ほどにある[[「series」のリンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]をクリックすると、この実験全体の詳細情報が見られます。
- 10. [[この実験全体の詳細情報ページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]の下部にある[[「Series Matrix File(s)」>ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/]]をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。
## 【実習】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する [#mcb0ec77]
- [[【使い方参考動画1】>http://togotv.dbcls.jp/20090221.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png 、[[【使い方参考動画2】>http://togotv.dbcls.jp/20090307.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の[[アクセッション番号（今回は GDS2294）>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]をクリックすると、解析用の「データセットブラウザ」が開きます。
- 6. 「Expression profiles」をクリックすると、[[この実験データセットにおける個々の遺伝子発現状況を検索できるページ>http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&cmd=search&term=GDS2294[ACCN]]に飛びます。
- 7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として [[Oct4>http://www.google.co.jp/search?q=Oct4]] ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。
- 8. 「データセットブラウザ」の「Data Analysis Tools」では詳細なデータ解析が可能です。
- 9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。
- 10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。
- 11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。
- 12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる[[ヒートマップ>http://images.google.co.jp/images?q=ヒートマップ]]でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。
- 13.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。




## 【実習】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&生データをダウンロードする [#ze44dc22]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081218.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2. 画面中央の「Platforms」をクリックします。
- 3. [[Platform(マイクロアレイの種類)の一覧画面が現れる>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&key=25000&imageType=8]]ので、上部の「FIND PLATFORM」をクリックします。
- 4. [[platformの検索画面>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform]]が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。
- 5. [[Affymetrixのヒトのマイクロアレイの検索結果>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform]]が表示されるので、中程にある「Affymetrix GeneChip Human Genome U133 Plus 2.0 Array」の左端にある[[「GPL570」というID>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]をクリックします。
- 6. [[表示された画面>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。
- 7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？
- 8. ヒットしたデータの左端にあるIDをクリックすると、[[そのデータセットの詳細情報>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832]]が閲覧できます
- 9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。
- 10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。
- 11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。
## 【参考】[[遺伝子発現バンク(GEO)目次、通称「GEO目次」>http://lifesciencedb.jp/geo/]] [#rdfd50d4]
- [[使い方参考動画>http://togotv.dbcls.jp/20080623.html#p01]] http://lifesciencedb.jp/image/small_video_icon.png
- NCBI GEO を日本語のインターフェイスで快適に使い、データの全容を俯瞰するための仕組み
- 今後さらに使いやすくアップデート予定






# [[&size(20){Mouse Genome Informatics(MGI)};>http://www.informatics.jax.org/]] [#w21fbbe9]
&color(green){マウスに関する遺伝子、ゲノム、生物学的な情報を提供する統合データベース};

## 【実習】MGIを使ってある遺伝子の様々な実験条件で得られた発現データを閲覧する [#p2cbd880]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081205.html#p01]]、[[【講習会動画】>http://togotv.dbcls.jp/20090217.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1.  [[http://www.informatics.jax.org/>http://www.informatics.jax.org/]]を開きます。
- 2. 脂肪代謝関連遺伝子であるperoxisome proliferator-activated receptor (PPAR) alphaのデータを調べてみましょう。サイト上部の検索窓に「ppara」と入力し、「Quick Search」を押します。
- 3. [[検索結果が表示>http://www.informatics.jax.org/searchtool/Search.do?query=ppara&submit=Quick+Search]]されるので「Genome Features」の項にある「ppara」をクリックします。
- 4. [[「Gene Detail」>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=markerDetail&key=25000]]が表示されます。真ん中あたりの「Expression」の項目へ移動します。
- 5. 「Data Summary」の [[Assays（実験手法別）>http://www.informatics.jax.org/searches/expression_report.cgi?_Marker_key=25000&returnType=assays&sort=Assay%20type]]、[[Results（全結果）>http://www.informatics.jax.org/searches/expression_report.cgi?_Marker_key=25000&returnType=assay%20results&sort=Anatomical%20structure]]、[[Tissues（組織別）>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=markerTissues&key=25000]]、[[Images（Figのある結果）>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&key=25000&imageType=8]]のそれぞれから発現データを一覧することができます。
- 6. 自分の興味ある遺伝子について同様に検索してみましょう。
## 【参考】MGIでノックアウトマウス情報の有無を調べる [#e813b839]
[[統合TVで紹介していますので興味ある方はぜひご覧ください。>http://togotv.dbcls.jp/20081128.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
