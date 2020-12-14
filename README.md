# Juxtaphony Project

[English](https://github.com/jin237/juxtaphony_project/blob/main/README-en.md)
[Français](https://github.com/jin237/juxtaphony_project/blob/main/README-fc.md)

<img src="https://github.com/jin237/juxtaphony_project/blob/main/images/document_visual_theme.001.jpeg">
<img src="https://github.com/jin237/juxtaphony_project/blob/main/images/document_visual_theme.002.jpeg">
<img src="https://github.com/jin237/juxtaphony_project/blob/main/images/document_visual_theme.003.jpeg">

### Juxtaphony Teamによるプロジェクト概要と意義

　本プロジェクトでは、「密」の状態でのウイルス感染のリスクを極小化することを目指しています。密集状態で話すことは飛沫感染のリスクを高めますが、「話さない」と言うことは生活上、不可能です。そこで、「ささやき声」で発話することによって、口の中にあるウイルス・細菌が減ることが報告されています。「ささやき声」での会話の実現ができれば、マスクの着用や集団回避による流行前にできていたような社会的な活動を回復させることができると考えています。
　ここで、本プロジェクトチームでは喉元の些細な音を拾うことのできる「スロートマイク」(咽喉マイク、骨伝導マイクとも呼ばれる)に着目し、また活用することによって、「ささやき声」での会話が実現を目指したいます。また、スロートマイクを用いた会話を実現するためにBluetooth(スマートフォン、パソコンなどについている無線通信機能)を用いたアプリケーションを開発することによって手短にスロートマイクの使いやすい環境が整えられると考えています。


# 『スロートマイク』
　スロートマイクとは、喉仏のあたりの骨伝導により音声を拾うマイクで、騒音や風が強いなどの雑音環境下でも音声を拾うことができます(下図)。その他のタイプのマイクでは、背景雑音が多いことから上記のような環境下ではうまく機能しません。ハイクオリティであればあるほど、「ささやき声」を拾うことができるため、ほとんど発声音量がなくとも、コミュニケーションが取れるようになります。
 
 <img src="https://github.com/jin237/juxtaphony_project/blob/main/images/ThroatMIC_Black.png" height=200px>
 
 Wikipediaより引用：： ["Throat Microphone"](https://en.wikipedia.org/wiki/Throat_microphone)
>A throat microphone, also called a laryngophone, is a type of contact microphone that absorbs vibrations directly from the wearer's throat by way of single or dual sensors worn against the neck. The sensors, called transducers, can pick up speech even in extremely noisy or windy environments, such as on a motorcycle or in a nightclub. Other types of microphones do not function well under these conditions because of high levels of background noise. Advanced laryngophones are able to pick up whispers, and therefore perform well in environments where communicating with others at a distance in silence is required, such as during covert military or law enforcement operations. Throat microphones are also very useful when helmets or respiratory protection is required. Many full-face SCBA, CABA, SAR Respirator, Elastomeric Respirator, N95 Respirator PAPR, or re-breather masks do not have a provision for a microphone inside the mask. The throat microphone can be used safely, as it is positioned outside the mask's face seal and as such does not compromise the respiratory protection provided by the mask, nor does it violate mask approvals and certification.
>With the advent of COVID-19 in 2020, throat microphone usage has expanded into other areas such as Hospital Emergency Rooms [1], Retail & Restaurants. This is because universal face mask usage and clear plastic physical dividers to enforce social distancing, has made face to face communications much more challenging with people having to raise their voice significantly to communicate.

日本語訳::
<br><br>
咽喉マイクとも呼ばれるスロートマイクは、首に装着した単一または二重のセンサーによって、装着者の喉仏からの振動を直接的に感知する接触マイクの一種である。トランスデューサーと呼ばれるセンサーは、バイクやナイトクラブなどの騒音や風の強い環境でも音声を拾うことができる。他タイプのマイクは、背景雑音が多いために、上記のような環境下ではうまく機能しない。高度な咽喉マイクは、ささやき声を拾うことができるため、軍事機関などの隠密作戦のように、遠く離れた場所にいる人と無音でコミュニケーションを取ることが必要な環境でも効果を発揮する。ヘルメットや呼吸器保護が必要な場合でも、スロートマイクは非常に有効である。多くのフルフェイスSのCBA、CABA、SAR呼吸器、エラストマー呼吸器、N95呼吸器PAPR、または再呼吸式マスクには、マスク内部にマイクのための規定がない。喉マイクはマスクのフェイスシールの外側にあるため、マスクの呼吸保護機能を損なうことなく、マスクの承認や認証に違反することもなく、安全に使用することができる。
2020年のCOVID-19の流行により、喉マイクの使用は、病院の救急室、小売店やレストランなどの他の分野にも拡大している。これは、普遍的なフェイスマスクの使用と、社会的な距離感を強制するための明確なプラスチック製の物理的な仕切りにより、人々がコミュニケーションをとるために声を大きく上げなければならないため、対面でのコミュニケーションがより困難になっているからである。



# 『SILENT - talking』
### 『SILENT - talking』とは？
本プロジェクトでは、「SILENT - talking」をBluetoothを用いたスロートマイクで会話が可能となるアプリケーションを開発します。このアプリケーションでは4つのモード(右表1)を用意し、学校の講義・授業、カフェ、会食会、オフィスでの会議など日常生活でのあらゆる場面で使用可能です。集団で集まってもリスクを最大限に減らすことができます。また、どこにでも持ち運びもでき、首につけることで普段から活用できるようになります。

### 『SILENT - talking』の基本構造
Bluetoothのみを用いる端末間あるいは、Beaconを介すのみのシステム.
イメージとしては、トランシーバーの上位互換だが、基本的には携帯端末の通信料がかからない。ローカル上で使える。専用端末化ができることをメリットとする。
Bluetoothによる近接感知機能を入れることによる。
Beaconを返すことによる特定領域内での複数端末での同時に行うことができる。

### 『SILENT - talking』に搭載する機能について
「SILENT - talking」は基本的にスロートマイクを端末に挿してささやき声で会話することを目的としたアプリケーションです。このアプリケーションでは、Bluetoothを用いて通信をし、音声のやりとりを行います。あらゆる場面に合わせた4つのモードを搭載することで活用できます。また、機器同士の距離に応じて、イヤホンから聞こえてくる音量も変わる仕組みとなっています。

表１　SILENT - talkingのモードとその内容
| モード | モード内容 |
|------|------|
| アドホック | 1対１の会話システム。Bluetoothによる音声会話。双方の会話の実現。 |
| パーティー | 多数人数での会話システム。Beaconなどのホスト機器を介した多人数での音声会話。 | 
|テーブルトーク | 多数人数での会話システム。一定空間内でのランダム会話の実現。 |
|クラスルーム | 1対多数の会話システム。 Beaconなどのホスト機器を介した音声会話による講義、授業などの実現。 |

<img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode1_adhoc.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode2_party.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode3_tabletalk.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode4_classroom.jpeg" height=250px>

#### アドホックモード
アドホックモードは「1対1」で会話ができます。

活用例：
- 2人でカフェに行く時
- 面談を行う時など個人的な会話

日常生活において、さまざまな人と会話をしても飛沫量を抑制することができ、普段通りの会話ができます。

#### パーティーモード
パーティーモードは、大きな空間で「多人数」と会話ができます。

活用例：
- 結婚式などのパーティー会場
- 学校での日常生活

パーティーなど大きな空間で色々な人と話すことのでき、感染リスクのを減らすこともできます。

#### テーブルトークモード
テーブルトークモードは、限られた「多人数」と会話ができます。

活用例：
- 居酒屋などの飲食店の各机やスペース
- ポスターセッションなどの各ブース

パーティーモードよりも狭い空間で個々のブースや席で話すことができます。他のテーブルのことは聞くことができません。

#### クラスルームモード
クラスルームモードは、授業や講義で使うことができます。

活用例：
- 授業や講義
- 講演会やワークショップ

授業や講演会など話す人が1人、聞く人が大勢の時などに使うことができます。このモードでは話者を変えることもできます。


### 『SILENT - talking』の使い方

1. 『SILENT - talking』を開く
2. スロートマイクを繋げる
3. 上記の4つのモードから場面に応じて選択
4. 会話相手またはグループを選択
5. 会話を開始

「ささやき声」で会話をお楽しみください。
『SILENT - talking』内で、スロートマイクで聞き取りやすい音声に変換を行っています。(嚥下音や首との摩擦音などを除去しています。)



# スロートマイクの音質向上のためのデータセット作成

## 概要
スロートマイク（咽喉マイク、骨伝導マイク）に関する音源及び評価数値データセット<br>

2020年に世界的な大流行を引き起こしたSARS-CoV-2ウイルスにおいては、感染経路として発声により生じる微細な飛沫の口腔外への拡散が重要視されている。発声により口外へウイルスが出ていくことにより、飛沫感染が起こる。そのため、密集状態における発語を禁ずることにより、当該ウイルスの伝播経路を効率的に遮断しうる可能性がある。また、口外飛沫量は発声量を小さくすることにより減少することが報告されている。しかしながら、社会生活において発語を禁じることは現実的でない。そこで我々は、僅かな発声をも採音しうるスロートマイク(喉頭マイク)を活用することにより、感染性ウイルスの環境への拡散を極小化しうる可能性に着目した。
本研究では、スロートマイクの音質向上のため、高音質なコンデンサマイクとの同時録音を通じた対照データ生成の予備実験を行った。これら対照データを用いた両者の波形データ、周波数、ハミング窓の値などの定量的比較と被験者を用いた定性評価の結果、「首の運動に伴うノイズ」、「嚥下音」に加えて、「両唇音」や「無声摩擦音」が、スロートマイクを介した会話における障害となることを同定した。人的評価による50音評価では、両唇音や無声摩擦音により発音するものが聞き取りにくく、「ま行」や「は行」、「さ行」が主に正解率が25％と低かった。今回得られた知見を元にフィルタ学習用のデータセットを構築することにより、スロートマイクを用いた低音量でのさまざまな会話支援技術の実現が期待される。また、その学習データの活用と共に現在流行しているコロナウイルスの収束の１つの起因となると確信している。

### 音源データ内容
スロートマイクと高音質マイク（本実験では、コンデンサマイク）での同時録音を行ったものに対する音源データセット
### 数値データ内容
- 上記の音源に対する各ウィンドウの数値データ（.csv）
- 音声通話による50音における各行の人的相対音声評価
<br><br>
## 実験環境
### 実験機材
| 機材概要 | 機材詳細名称 |
| ------- | -------- |
| コンデンサマイク | SHURE BETA87A 超単一指向性ボーカル用コンデンサーマイク |
| スロートマイク | ・SONONIA　ヘッドセット ヘッドフォン ネックバンド スロートマイク<br>・HoneyBB 携帯電話咽喉マイク イヤホン 骨伝導 声帯マイク チューブ式  |
| オーディオインターフェース | TASCAM ( タスカム ) / SERIES 102i |
| モニター用ヘッドホン | ・SONY ステレオヘッドホン MDR-7506 <br>・Pioneer SE-M521 ヘッドホン |
| 録音及び波形編集ソフト | ・Cubase Elements 11 <br>・Audacity |

<img src="https://github.com/jin237/juxtaphony_project/blob/main/images/ThroatMIC_Black.png" height=150px>
図１　スロートマイクCGモデル
<br>
<img src="https://images-na.ssl-images-amazon.com/images/I/61Hzs8tXaQL._AC_SL1317_.jpg" height=150px>
図２　SHURE BETA87A 超単一指向性ボーカル用コンデンサーマイク
<br><br><br><br>

### 雑音環境
スロートマイクに関する雑音は外的な要因（空調、対象者以外の声など）は含まれにくいことが報告されているため、スロートマイクでの雑音は、”音源データ内容ー発話音源ー雑音のみの音源”に記されたものであるとする。
<br>コンデンサマイクに関する雑音は、外的な周囲雑音は空調であるとし、その音源に関しても、抽出及びラベルをつけて公表する。


### プログラム環境
graph_of_wavefile.ipynb, mix_spectrum_dft.ipynb, mix_wave.ipynbなどのプログラムによるグラフ、数値の抽出におけるプログラム環境
- Python 3.8.3
  - wave
  - numpy
  - matplotlib
- Jupyternotebook 6.0.3


# 音源データ内容
スロートマイク（咽喉マイク、骨伝導マイク）と高音質マイク（本実験では、コンデンサマイク）での同時録音を行ったものに対する音源データセット
<br>
## 発話音源
### フレーズ「これはデモ音源です」と発話したもの
６人の男性（20代）が「これはデモ音源です」と発話したもの<br>
各音源データに対して、音源(TMとCM)及びHamming Windowを同時系列、各人によってデータ化
<br>
### 日本語50音表の発話
１人の男性（20代）がCosComに掲載されているひらがな50音表にある日本語発音を行う<br>
https://www.coscom.co.jp/hiragana-katakana/kanatable-j.html
<br>
### 雑音のみの音源
本データでは、以下のものを雑音とする<br>
・首の運動により生じる、スロートマイクとの擦れ及び筋肉による軋みの音<br>
・唾液、液体物の飲み込みにより生じる音<br>
・機器の接続によって生じる音<br>
とする。それぞれに対して、ノイズのラベル付けを行っている。
<br><br><br><br>

# 数値データ内容
### 上記の音源に対する各ウィンドウの数値データ（.csv/.txt）
データは、以下のようなもので出力
https://github.com/jin237/juxtaphony_project/tree/main/data_set/preliminary_experiments/analysis_result/conde_demo_spectrum.txt
https://github.com/jin237/juxtaphony_project/tree/main/data_set/preliminary_experiments/analysis_result/throat_demo_spectrum.txt  
これらをグラフ化したものは以下で出力
csvファイルまたはtxtファイルにてHamming Windowなどの数値データの公開
<img src="https://github.com/jin237/juxtaphony_project/blob/main/data_set/preliminary_experiments/analysis_result/throat_demo_spectrum.png">

  図３　スロートマイクのスペクトラムグラフ
<br><br>
<img src="https://github.com/jin237/juxtaphony_project/blob/main/data_set/preliminary_experiments/analysis_result/conde_demo_spectrum.png">

  図４　コンデンサマイクのスペクトラムグラフ
<br><br>
<img src="https://github.com/jin237/juxtaphony_project/blob/main/data_set/preliminary_experiments/analysis_result/mix_wave.png">

  図５　スロートマイク及びコンデンサマイクの波形の重ね合わせ
<br><br>
<img src="https://github.com/jin237/juxtaphony_project/blob/main/data_set/preliminary_experiments/analysis_result/mix_demo.png">

  図６　スロートマイク及びコンデンサマイクのスペクトラムグラフの重ね合わせ
<br><br>

### 音声通話による50音における各行の人的相対音声評価
- ４人を対象に飯野が話者として、Skypeで2名、LINEで2名以下のような実験を行った。
- 通信通話アプリケーション（LINE、Skype）を用いて、定常的な雑音環境下に置いて、「あ」「い」「う」「え」「お」の発音を最初に教え、その後に、「さ」行、「ま」行、「か」行　など、の行をランダムに発音することで、評価を行う
<br>
＜結果と考察＞

- 「ま」行、「さ」行、「わ」「や」の認識率：２５％
- 「は」「か」行は認識率：５０％
- 唾を飲み込むことによる音はささやき声よりも大きい
  - 突発的ではあるが、特殊な音ではあるのでフィルターはかけやすいかもしれない。
<br><br>


# 参考資料(articles内)
### 音源抽出・モデル作成
  - [July 2018, 情報処理学会研究報告, Vol.2018-SLP-123 No.8, “深層学習に基づく特徴量変換を用いた咽喉マイクの音声認識”](https://ipsj.ixsq.nii.ac.jp/ej/?action=repository_action_common_download&item_id=190621&item_no=1&attribute_id=1&file_no=1)
  - [September 2019, INTERSPEECH 2019, "Knowledge Distillation for Throat Microphone Speech Recognition"](https://www.researchgate.net/publication/335829265_Knowledge_Distillation_for_Throat_Microphone_Speech_Recognition)
  - [Deep Learningにおける知識の蒸留](http://codecrafthouse.jp/p/2018/01/knowledge-distillation/)
  - [Proceedings, APSIPA Annual Summit and Conference 2018 12-15 November 2018, Hawaii, "Bottleneck feature-mediated DNN-based feature mapping for throat microphone speech recognition"](http://www.apsipa.org/proceedings/2018/pdfs/0001738.pdf)
  - [August, 2013, Koc University, A Thesis Submitted to the
Graduate School of Sciences and Engineering in Partial Fulfillment of the Requirements for the Degree of Master of Science in Electrical and Electronics Engineering, "Enhancement of Throat Microphone Recordings Using Gaussian Mixture Model Probabilistic Estimator"](https://arxiv.org/abs/1804.05937)
  - [January 2004, COST278 and ISCA Tutorial and Research Workshop (ITRW) on Robustness Issues in Conversational Interaction, "Combined Use of Close-Talk and Throat Microphones for Improved Speech Recognition under Non-Stationary Background Noise"](https://www.researchgate.net/publication/228889100_Combined_use_of_close-talk_and_throat_microphones_for_improved_speech_recognition_under_non-stationary_background_noise)
  - [学会誌「EICA」第 19 巻 第 2・3 合併号（2014）, p182-186, "高雑音下での声帯マイクを用いた音声認識"](http://eica.jp/search/browse.php?file=a_19_2_182.pdf&id=1202)
<br><br>
### NMF
  - [半教師あり非負値行列因子分解における音源分離性能向上のための効果的な基底学習法](https://www.slideshare.net/DaichiKitamura/ss-66384298)<br>
  - [Daniel D.Lee & H.Sebastian Seung, "Learning the parts of objects by non-negative matrix factorization"](http://www.columbia.edu/~jwp2128/Teaching/E4903/papers/nmf_nature.pdf)
  - [IBIS2018 企画セッション 招待講演, "音声分野における敵対的学習の可能性と展望"](http://ibisml.org/ibis2018/files/2018/11/takamichi.pdf)

<br><br>
### 発話関連
  - [June 2018, 情報処理学会研究報告, Vol.2018-SLP-122 No.33, "雑音下異常検知における前処理としてのNMF音源抽出手法の検討"](https://ipsj.ixsq.nii.ac.jp/ej/index.php?active_action=repository_view_main_item_detail&page_id=13&block_id=8&item_id=189961&item_no=1)
  - [岡山県立大学保健福祉学部紀要, 第21巻１号2014年, 45~55頁, "音声分析によるマスク着用時のコミュニケーション方法についての検討"](https://core.ac.uk/download/pdf/51452429.pdf)
  - [January 2020, Journal of Sifnal Processing, Vol.24, No.1, pp.19-29, "複数の装着型マイクを用いた多人数会話の音声認識"](https://www.jstage.jst.go.jp/article/jsp/24/1/24_19/_article/-char/ja/)

### COVID-19関連
  - [April 2020, New England Journal of Medicine 382(21), “Visualizing Speech-Generated Oral Fluid Droplets with Laser Light Scattering”](https://www.researchgate.net/publication/340674849_Visualizing_Speech-Generated_Oral_Fluid_Droplets_with_Laser_Light_Scattering)


