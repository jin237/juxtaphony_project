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
https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/conde_demo_spectrum.txt
https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/throat_demo_spectrum.txt  
これらをグラフ化したものは以下で出力
csvファイルまたはtxtファイルにてHamming Windowなどの数値データの公開
![スロートマイクのスペクトラムグラフ](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/throat_demo_spectrum.png)<br>
図３　スロートマイクのスペクトラムグラフ
<br><br>
![コンデンサマイクのスペクトラムグラム](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/conde_demo_spectrum.png)<br>
図４　コンデンサマイクのスペクトラムグラフ
<br><br>
![スロートマイク及びコンデンサマイクの波形の重ね合わせ](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/mix_wave.png)<br>
図５　スロートマイク及びコンデンサマイクの波形の重ね合わせ
<br><br>
![スロートマイク及びコンデンサマイクのスペクトラムグラフの重ね合わせ](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/mix_demo.png)<br>
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


