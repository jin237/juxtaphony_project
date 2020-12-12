# 『SILENT - talking』
### 『SILENT - talking』とは？
本プロジェクトでは、「SILENT - talking」をBluetoothを用いたスロートマイクで会話が可能となるアプリケーションを開発します。このアプリケーションでは4つのモード(右表1)を用意し、学校の講義・授業、カフェ、会食会、オフィスでの会議など日常生活でのあらゆる場面で使用可能です。集団で集まってもリスクを最大限に減らすことができます。また、どこにでも持ち運びもでき、首につけることで普段から活用できるようになります。

### 搭載機能
表１　SILENT - talkingのモードとその内容
| モード | モード内容 |
|------|------|
| アドホック | 1対１の会話システム。Bluetoothによる音声会話。双方の会話の実現。 |
| パーティー | 多数人数での会話システム。Beaconなどのホスト機器を介した多人数での音声会話。 | 
|テーブルトーク | 多数人数での会話システム。一定空間内でのランダム会話の実現。 |
|クラスルーム | 1対多数の会話システム。 Beaconなどのホスト機器を介した音声会話による講義、授業などの実現。 |

<img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode1_adhoc.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode2_party.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode3_tabletalk.jpeg" height=250px><img src="https://github.com/jin237/juxtaphony_project/blob/main/application/app_mode_visual/mode4_classroom.jpeg" height=250px>

### 『SILENT - talking』の基本構造
Bluetoothのみを用いる端末間あるいは、Beaconを介すのみのシステム.
イメージとしては、トランシーバーの上位互換だが、基本的には携帯端末の通信料がかからない。ローカル上で使える。専用端末化ができることをメリットとする。
Bluetoothによる近接感知機能を入れることによる。
Beaconを返すことによる特定領域内での複数端末での同時に行うことができる。

