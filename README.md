<img src="icons/icon_tran.png" width=300>

# 画像処理100本ノック!!


HOMEPAGE >> https://yoyoyo-yo.github.io/Gasyori100knock/

画像処理の初学者のための問題１００問

**問題も答えもjupyterのをみてください（最新版です）**

これはイモリと一緒に画像処理の基本的処理の知識を身に着け、アルゴリズムを理解するための100本ノックです。ここに載っている問題はOpenCVでAPIが用意されているものが殆どですが、**あえてそれを自分の手で実装**してください。解答も載っけてますが、それはあくまで解答です。自分で考えながら実装して下さい。

- 【注意】このページを利用して、または関して生じた事に関しては、私は一切責任を負いません。すべて**自己責任**でお願い致します。
- **あくまで趣味ベースで作ったものなので、プルリクエストは受け付けてますが依頼などは一切受け付けません
そこをご理解頂けた方のみご利用下さい**


## Adv

- ***Study-AI株式会社様 http://kentei.ai/ のAI実装検定のシラバスに使用していただくことになりました！(ディープラーニング無限ノックも）Study-AI株式会社様ではAIスキルを学ぶためのコンテンツを作成されています！
検定も実施されてるので、興味ある方はぜひ受けることをお勧めします！***

- ***English ver (by KuKuXia) https://github.com/KuKuXia/Image_Processing_100_Questions***

- ***Chinese ver (by gzr2017) https://github.com/gzr2017/ImageProcessing100Wen***

- ***ディープラーニング∞ノック!! （ほぼTips化してるけど） https://github.com/yoyoyo-yo/DeepLearningMugenKnock***


## [チュートリアル](Tutorial)

What language do you use?

- [Off cource python!](Tutorial/Tutorial_python.ipynb) &emsp; <a href="https://colab.research.google.com/github/yoyoyo-yo/Gasyori100knock/blob/master/Tutorial/Tutorial_python.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
- [I'm C++ !!](Tutorial/README_opencv_c_install.md)
- [JavaScript is God!](Tutorial/README_javascript.md)

 Contents

0. 画像処理の基礎知識(Pythonのみ)
1. インストール
2. 画像読み込み・表示
3. 画像のコピー
4. 画素をいじる
5. 画像の保存
6. 練習問題

[MatplotlibとかOpenCVのTips](Image_processing_tips.ipynb)

あとは問題を解いていってください。それぞれのフォルダに問題内容が入っています。問題では assets/imori.jpg を使用して下さい。各フォルダのREADME.mdに問題、解答プログラムがあります。```python answers/answer_@@.py```　とすると解答が出ます。

## 問題

### **問題も答えもjupyterのをみてください（最新版です）**

### **画像をここから持ってこなくても、URL指定で読みこめるようにしました**

使える画像
| assets/imori_128x128.png (イモリの128x128サイズの美しい画像) | assets/imori_256x256.png (イモリの256x256サイズのかわゆい画像) |  assets/imori_512x512.png (イモリの512x512サイズのめんこいお画像) | assets/madara_128x128.png (マダライモリの128x128サイズのかわいらしい画像) | assets/madara_256x256.png (マダライモリの256x256サイズのかわない画像) |  assets/madara_512x512.png (マダライモリの512x512サイズのキュートな画像) | 
|:---:|:---:|:---:|:---:|:---:|:---:|
| <img src="assets/imori_128x128.png" width=60> | <img src="assets/imori_256x256.png" width=120> | <img src="assets/imori_512x512.png" width=240> | <img src="assets/madara_128x128.png" width=60> | <img src="assets/madara_256x256.png" width=120> | <img src="assets/madara_512x512.png" width=240> |

|　assets/imori_256x256_noise.png (ノイジーなイモリのノイズ入り画像) | assets/imori_256x256_dark.png (暗いイモリのかわいい画像) |  assets/imori_256x256_light.png (明るいイモリのかわいい画像) |  assets/imori_256x256_gamma.png (gammaされたイモリのかわいい画像) |
|:---:|:---:|:---:|:---:|
| <img src="assets/imori_256x256_noise.png" width=150> | <img src="assets/imori_256x256_dark.png" width=150> | <img src="assets/imori_256x256_light.png" width=150> | <img src="assets/imori_256x256_gamma.png" width=150> |


こういう感じで読み込めます！(詳しくは[Tutorial](Tutorial/Tutorial_python.ipynb))

```python
from skimage import io
img = io.imread('https://yoyoyo-yo.github.io/Gasyori100knock/assets/imori_256x256.png')
```

## [問題1 - 10](Question_01_10) &ensp; <a href="https://colab.research.google.com/github/yoyoyo-yo/Gasyori100knock/blob/master/Question_01_10/Question_01_10.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

<!--
|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|1 |  チャネル入れ替え| &check;| [&check;](Question_01_10/answers_cpp/answer_1.cpp) | |6| 減色処理| &check; | [&check;](Question_01_10/answers_cpp/answer_6.cpp) 
|2|グレースケール化| &check;| [&check;](Question_01_10/answers_cpp/answer_2.cpp) | |7| 平均プーリング | &check;| [&check;](Question_01_10/answers_cpp/answer_7.cpp) 
|3| 二値化| &check; | [&check;](Question_01_10/answers_cpp/answer_3.cpp)  | |8| Maxプーリング| &check;| [&check;](Question_01_10/answers_cpp/answer_8.cpp) 
|4|大津の二値化 | &check;| [&check;](Question_01_10/answers_cpp/answer_4.cpp)  | |9| ガウシアンフィルタ| &check;| [&check;](Question_01_10/answers_cpp/answer_9.cpp) 
|5| HSV変換| &check;| [&check;](Question_01_10/answers_cpp/answer_5.cpp) | |10| メディアンフィルタ| &check;| [&check;](Question_01_10/answers_cpp/answer_10.cpp) |
-->

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|1|[チャネル入れ替え](Question_01_10/Question_01_10.ipynb#q1)| [&check;](Question_01_10/answers_py/answer_1.py) | [&check;](Question_01_10/answers_cpp/answer_1.cpp) | |6| [減色処理](Question_01_10#q6-%E6%B8%9B%E8%89%B2%E5%87%A6%E7%90%86) |[&check;](Question_01_10/answers_py/answer_6.py) | [&check;](Question_01_10/answers_cpp/answer_6.cpp) 
|2|[グレースケール化](Question_01_10#q2-%E3%82%B0%E3%83%AC%E3%83%BC%E3%82%B9%E3%82%B1%E3%83%BC%E3%83%AB%E5%8C%96) |[&check;](Question_01_10/answers_py/answer_2.py) | [&check;](Question_01_10/answers_cpp/answer_2.cpp) | |7| [平均プーリング](Question_01_10#q7-%E5%B9%B3%E5%9D%87%E3%83%97%E3%83%BC%E3%83%AA%E3%83%B3%E3%82%B0) |[&check;](Question_01_10/answers_py/answer_7.py) | [&check;](Question_01_10/answers_cpp/answer_7.cpp) 
|3|[二値化](Question_01_10#q3-%E4%BA%8C%E5%80%A4%E5%8C%96) | [&check;](Question_01_10/answers_py/answer_3.py) | [&check;](Question_01_10/answers_cpp/answer_3.cpp)  | |8| [Maxプーリング](Question_01_10#q8-max%E3%83%97%E3%83%BC%E3%83%AA%E3%83%B3%E3%82%B0) |[&check;](Question_01_10/answers_py/answer_8.py) | [&check;](Question_01_10/answers_cpp/answer_8.cpp) 
|4|[大津の二値化](Question_01_10#q4-%E5%A4%A7%E6%B4%A5%E3%81%AE%E4%BA%8C%E5%80%A4%E5%8C%96) | [&check;](Question_01_10/answers_py/answer_4.py) | [&check;](Question_01_10/answers_cpp/answer_4.cpp)  | |9| [ガウシアンフィルタ](Question_01_10#q9-%E3%82%AC%E3%82%A6%E3%82%B7%E3%82%A2%E3%83%B3%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_01_10/answers_py/answer_9.py) | [&check;](Question_01_10/answers_cpp/answer_9.cpp) 
|5|[HSV変換](Question_01_10#q5-hsv%E5%A4%89%E6%8F%9B) | [&check;](Question_01_10/answers_py/answer_5.py) | [&check;](Question_01_10/answers_cpp/answer_5.cpp) | |10| [メディアンフィルタ](Question_01_10#q10-%E3%83%A1%E3%83%87%E3%82%A3%E3%82%A2%E3%83%B3%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_01_10/answers_py/answer_10.py) | [&check;](Question_01_10/answers_cpp/answer_10.cpp) |


## [問題11 - 20](Question_11_20) &ensp; <a href="https://colab.research.google.com/github/yoyoyo-yo/Gasyori100knock/blob/master/Question_11_20/Question_11_20.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

<!--
|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|11| 平滑化フィルタ | &check; | [&check;](Question_11_20/answers_cpp/answer_11.cpp) |  |16| Sobelフィルタ | &check; | [&check;](Question_11_20/answers_cpp/answer_16.cpp) | 
|12| モーションフィルタ | &check;| [&check;](Question_11_20/answers_cpp/answer_12.cpp) |  |17| [aplacianフィルタ| &check; | [&check;](Question_11_20/answers_cpp/answer_17.cpp) | 
|13| MAX-MINフィルタ | &check; | [&check;](Question_11_20/answers_cpp/answer_13.cpp) |  |18| Embossフィルタ| &check;| [&check;](Question_11_20/answers_cpp/answer_18.cpp) | 
|14| 微分フィルタ| &check;| [&check;](Question_11_20/answers_cpp/answer_14.cpp) |  |19| LoGフィルタ| &check;| [&check;](Question_11_20/answers_cpp/answer_19.cpp) | 
|16| Prewittフィルタ| &check; | [&check;](Question_11_20/answers_cpp/answer_15.cpp) |  |20| ヒストグラム表示|  [&check;](Question_11_20/answers_py/answer_20.py) |
-->

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|11| [平滑化フィルタ](Question_11_20#q11-%E5%B9%B3%E6%BB%91%E5%8C%96%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_11.py) | [&check;](Question_11_20/answers_cpp/answer_11.cpp) |  |16| [Sobelフィルタ](Question_11_20#q15-sobel%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_16.py) | [&check;](Question_11_20/answers_cpp/answer_16.cpp) | 
|12| [モーションフィルタ](Question_11_20#q12-%E3%83%A2%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_12.py) | [&check;](Question_11_20/answers_cpp/answer_12.cpp) |  |17| [Laplacianフィルタ](Question_11_20#q17-laplacian%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_17.py) | [&check;](Question_11_20/answers_cpp/answer_17.cpp) | 
|13| [MAX-MINフィルタ](Question_11_20#q13-max-min%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_13.py) | [&check;](Question_11_20/answers_cpp/answer_13.cpp) |  |18| [Embossフィルタ](Question_11_20#q18-emboss%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_18.py) | [&check;](Question_11_20/answers_cpp/answer_18.cpp) | 
|14| [微分フィルタ](Question_11_20#q14-%E5%BE%AE%E5%88%86%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_14.py) | [&check;](Question_11_20/answers_cpp/answer_14.cpp) |  |19| [LoGフィルタ](Question_11_20#q19-log%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_19.py) | [&check;](Question_11_20/answers_cpp/answer_19.cpp) | 
|16| [Prewittフィルタ](Question_11_20#q16-prewitt%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_11_20/answers_py/answer_15.py) | [&check;](Question_11_20/answers_cpp/answer_15.cpp) |  |20| [ヒストグラム表示](Question_11_20#q20-%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0%E8%A1%A8%E7%A4%BA)  |  [&check;](Question_11_20/answers_py/answer_20.py) |


## [問題21 - 30](Question_21_30) &ensp;  <a href="https://colab.research.google.com/github/yoyoyo-yo/Gasyori100knock/blob/master/Question_21_30/Question_21_30.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|21| [ヒストグラム正規化](Question_21_30#q21-%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0%E6%AD%A3%E8%A6%8F%E5%8C%96) | [&check;](Question_21_30/answers_py/answer_21.py) | [&check;](Question_21_30/answers_cpp/answer_21.cpp) |  |26| [Bi-linear補間](Question_21_30#q26-bi-linear%E8%A3%9C%E9%96%93) | [&check;](Question_21_30/answers_py/answer_26.py) | [&check;](Question_21_30/answers_cpp/answer_26.cpp)  |
|22| [ヒストグラムのスケーリングとシフト](Question_21_30#q22-%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0%E6%93%8D%E4%BD%9C) | [&check;](Question_21_30/answers_py/answer_22.py) | [&check;](Question_21_30/answers_cpp/answer_22.cpp)  | |27| [Bi-cubic補間](Question_21_30#q27-bi-cubic%E8%A3%9C%E9%96%93) | [&check;](Question_21_30/answers_py/answer_27.py) | [&check;](Question_21_30/answers_cpp/answer_27.cpp)  |
| 23| [ヒストグラム平坦化](Question_21_30#q23-%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0%E5%B9%B3%E5%9D%A6%E5%8C%96) | [&check;](Question_21_30/answers_py/answer_23.py) | [&check;](Question_21_30/answers_cpp/answer_23.cpp)  | |28| [アフィン変換(平行移動)](Question_21_30#q28-%E3%82%A2%E3%83%95%E3%82%A3%E3%83%B3%E5%A4%89%E6%8F%9B%E5%B9%B3%E8%A1%8C%E7%A7%BB%E5%8B%95) | [&check;](Question_21_30/answers_py/answer_28.py) | [&check;](Question_21_30/answers_cpp/answer_28.cpp)  |
| 24| [ガンマ補正](Question_21_30#q24-%E3%82%AC%E3%83%B3%E3%83%9E%E8%A3%9C%E6%AD%A3) | [&check;](Question_21_30/answers_py/answer_24.py) | [&check;](Question_21_30/answers_cpp/answer_24.cpp)  | |29| [アフィン変換(拡大縮小)](Question_21_30#q29-%E3%82%A2%E3%83%95%E3%82%A3%E3%83%B3%E5%A4%89%E6%8F%9B%E6%8B%A1%E5%A4%A7%E7%B8%AE%E5%B0%8F) | [&check;](Question_21_30/answers_py/answer_29.py) | [&check;](Question_21_30/answers_cpp/answer_29.cpp)  |
|25| [最近傍補間](Question_21_30#q25-%E6%9C%80%E8%BF%91%E5%82%8D%E8%A3%9C%E9%96%93) | [&check;](Question_21_30/answers_py/answer_25.py) | [&check;](Question_21_30/answers_cpp/answer_25.cpp)  | |30| [アフィン変換(回転)](Question_21_30#q30-%E3%82%A2%E3%83%95%E3%82%A3%E3%83%B3%E5%A4%89%E6%8F%9B%E5%9B%9E%E8%BB%A2) | [&check;](Question_21_30/answers_py/answer_30.py) | [&check;](Question_21_30/answers_cpp/answer_30.cpp)

### [問題31 - 40](Question_31_40)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|31| [アフィン変換(スキュー)](Question_31_40#q31-%E3%82%A2%E3%83%95%E3%82%A3%E3%83%B3%E5%A4%89%E6%8F%9B%E3%82%B9%E3%82%AD%E3%83%A5%E3%83%BC) | [&check;](Question_31_40/answers_py/answer_31.py) | [&check;](Question_31_40/answers_cpp/answer_31.cpp) |  | 36| [JPEG圧縮 (Step.1)離散コサイン変換](Question_31_40#q36-jpeg%E5%9C%A7%E7%B8%AE-step1%E9%9B%A2%E6%95%A3%E3%82%B3%E3%82%B5%E3%82%A4%E3%83%B3%E5%A4%89%E6%8F%9B) | [&check;](Question_31_40/answers_py/answer_36.py) | [&check;](Question_31_40/answers_cpp/answer_36.cpp)
|32| [フーリエ変換](Question_31_40#q32-%E3%83%95%E3%83%BC%E3%83%AA%E3%82%A8%E5%A4%89%E6%8F%9B) | [&check;](Question_31_40/answers_py/answer_31.py) | [&check;](Question_31_40/answers_cpp/answer_32.cpp) |  |37| [PSNR](Question_31_40#q37-psnr) | [&check;](Question_31_40/answers_py/answer_37.py) | [&check;](Question_31_40/answers_cpp/answer_37.cpp)
|33| [フーリエ変換 ローパスフィルタ](Question_31_40#q33-%E3%83%95%E3%83%BC%E3%83%AA%E3%82%A8%E5%A4%89%E6%8F%9B%E3%83%AD%E3%83%BC%E3%83%91%E3%82%B9%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_31_40/answers_py/answer_33.py) | [&check;](Question_31_40/answers_cpp/answer_33.cpp) | |38| [JPEG圧縮 (Step.2)DCT+量子化](Question_31_40#q38-jpeg%E5%9C%A7%E7%B8%AE-step2dct%E9%87%8F%E5%AD%90%E5%8C%96) | [&check;](Question_31_40/answers_py/answer_38.py) | [&check;](Question_31_40/answers_cpp/answer_38.cpp)
|34| [フーリエ変換 ハイパスフィルタ](Question_31_40#q34-%E3%83%95%E3%83%BC%E3%83%AA%E3%82%A8%E5%A4%89%E6%8F%9B%E3%83%8F%E3%82%A4%E3%83%91%E3%82%B9%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_31_40/answers_py/answer_34.py) | [&check;](Question_31_40/answers_cpp/answer_34.cpp) | |39| [JPEG圧縮 (Step.3)YCbCr表色系](Question_31_40#q39-jpeg%E5%9C%A7%E7%B8%AE-step3ycbcr%E8%A1%A8%E8%89%B2%E7%B3%BB) | [&check;](Question_31_40/answers_py/answer_39.py) | [&check;](Question_31_40/answers_cpp/answer_39.cpp) |
|35| [フーリエ変換 バンドパスフィルタ](Question_31_40#q35-%E3%83%95%E3%83%BC%E3%83%AA%E3%82%A8%E5%A4%89%E6%8F%9B%E3%83%90%E3%83%B3%E3%83%89%E3%83%91%E3%82%B9%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_31_40/answers_py/answer_35.py) | [&check;](Question_31_40/answers_cpp/answer_35.cpp) | | 40| [JPEG圧縮 (Step.4)YCbCr+DCT+量子化](Question_31_40#q40-jpeg%E5%9C%A7%E7%B8%AE-step4ycbcrdct%E9%87%8F%E5%AD%90%E5%8C%96) | [&check;](Question_31_40/answers_py/answer_40.py) | [&check;](Question_31_40/answers_cpp/answer_40.cpp) |

### [問題41 - 50](Question_41_50)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 41 | [Cannyエッジ検出 (Step.1) エッジ強度](Question_41_50#q41-canny%E3%82%A8%E3%83%83%E3%82%B8%E6%A4%9C%E5%87%BA-step1-%E3%82%A8%E3%83%83%E3%82%B8%E5%BC%B7%E5%BA%A6) | [&check;](Question_41_50/answers_py/answer_41.py) | [&check;](Question_41_50/answers_cpp/answer_41.cpp) | | 46 | [Hough変換・直線検出 (Step.3) Hough逆変換](Question_41_50#q46-hough%E5%A4%89%E6%8F%9B%E7%9B%B4%E7%B7%9A%E6%A4%9C%E5%87%BA-step3-hough%E9%80%86%E5%A4%89%E6%8F%9B) | [&check;](Question_41_50/answers_py/answer_46.py) | [&check;](Question_41_50/answers_cpp/answer_46.cpp) |
| 42 | [Cannyエッジ検出 (Step.2) 細線化](Question_41_50#q42-canny%E3%82%A8%E3%83%83%E3%82%B8%E6%A4%9C%E5%87%BA-step2-%E7%B4%B0%E7%B7%9A%E5%8C%96) | [&check;](Question_41_50/answers_py/answer_42.py) | [&check;](Question_41_50/answers_cpp/answer_42.cpp) | | 47 | [モルフォロジー処理(膨張)](Question_41_50#q47-%E3%83%A2%E3%83%AB%E3%83%95%E3%82%A9%E3%83%AD%E3%82%B8%E3%83%BC%E5%87%A6%E7%90%86%E8%86%A8%E5%BC%B5) | [&check;](Question_41_50/answers_py/answer_47.py) | [&check;](Question_41_50/answers_cpp/answer_47.cpp) |
| 43 | [Cannyエッジ検出 (Step.3) ヒステリシス閾処理](Question_41_50#q43-canny%E3%82%A8%E3%83%83%E3%82%B8%E6%A4%9C%E5%87%BA-step3-%E3%83%92%E3%82%B9%E3%83%86%E3%83%AA%E3%82%B7%E3%82%B9%E9%96%BE%E5%87%A6%E7%90%86) | [&check;](Question_41_50/answers_py/answer_43.py) | [&check;](Question_41_50/answers_cpp/answer_43.cpp) | | 48 | [モルフォロジー処理(収縮)](Question_41_50#q48-%E3%83%A2%E3%83%AB%E3%83%95%E3%82%A9%E3%83%AD%E3%82%B8%E3%83%BC%E5%87%A6%E7%90%86%E5%8F%8E%E7%B8%AE) | [&check;](Question_41_50/answers_py/answer_48.py) | [&check;](Question_41_50/answers_cpp/answer_48.cpp)|
| 44| [Hough変換・直線検出 (Step.1) Hough変換](Question_41_50#q44-hough%E5%A4%89%E6%8F%9B%E7%9B%B4%E7%B7%9A%E6%A4%9C%E5%87%BA-step1-hough%E5%A4%89%E6%8F%9B) | [&check;](Question_41_50/answers_py/answer_44.py) |  [&check;](Question_41_50/answers_cpp/answer_44.cpp)  | | 49 | [オープニング処理](Question_41_50#q49-%E3%82%AA%E3%83%BC%E3%83%97%E3%83%8B%E3%83%B3%E3%82%B0%E5%87%A6%E7%90%86) | [&check;](Question_41_50/answers_py/answer_49.py) |[&check;](Question_41_50/answers_cpp/answer_49.cpp) |
| 45| [Hough変換・直線検出 (Step.2) NMS](Question_41_50#q45-hough%E5%A4%89%E6%8F%9B%E7%9B%B4%E7%B7%9A%E6%A4%9C%E5%87%BA-step2-nms) | [&check;](Question_41_50/answers_py/answer_45.py) | [&check;](Question_41_50/answers_cpp/answer_45.cpp) | | 50 | [クロージング処理](Question_41_50#q50-%E3%82%AF%E3%83%AD%E3%83%BC%E3%82%B8%E3%83%B3%E3%82%B0%E5%87%A6%E7%90%86) | [&check;](Question_41_50/answers_py/answer_50.py) | [&check;](Question_41_50/answers_cpp/answer_50.cpp)|

### [問題51 - 60](Question_51_60)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 51 | [モルフォロジー勾配](Question_51_60#q51-%E3%83%A2%E3%83%AB%E3%83%95%E3%82%A9%E3%83%AD%E3%82%B8%E3%83%BC%E5%8B%BE%E9%85%8D) | [&check;](Question_51_60/answers/answer_51.py) | | | 56 | [テンプレートマッチング NCC](Question_51_60#q56-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%9E%E3%83%83%E3%83%81%E3%83%B3%E3%82%B0-ncc) | [&check;](Question_51_60/answers/answer_56.py) | | 
|52|[トップハット変換](Question_51_60#q52-%E3%83%88%E3%83%83%E3%83%97%E3%83%8F%E3%83%83%E3%83%88%E5%A4%89%E6%8F%9B) | [&check;](Question_51_60/answers/answer_52.py) | | | 57 | [テンプレートマッチング ZNCC](Question_51_60#q57-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%9E%E3%83%83%E3%83%81%E3%83%B3%E3%82%B0-zncc) | [&check;](Question_51_60/answers/answer_57.py) | | 
| 53 | [ブラックハット変換](Question_51_60#q53-%E3%83%96%E3%83%A9%E3%83%83%E3%82%AF%E3%83%8F%E3%83%83%E3%83%88%E5%A4%89%E6%8F%9B) | [&check;](Question_51_60/answers/answer_53.py) | |  | 58 | [ラベリング 4近傍](Question_51_60#q58-%E3%83%A9%E3%83%99%E3%83%AA%E3%83%B3%E3%82%B0-4%E8%BF%91%E5%82%8D) | [&check;](Question_51_60/answers/answer_58.py) | | 
| 54 | [テンプレートマッチング SSD](Question_51_60#q54-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%9E%E3%83%83%E3%83%81%E3%83%B3%E3%82%B0-ssd) | [&check;](Question_51_60/answers/answer_54.py) | |  | 59 | [ラベリング 8近傍](Question_51_60#q59-%E3%83%A9%E3%83%99%E3%83%AA%E3%83%B3%E3%82%B0-8%E8%BF%91%E5%82%8D) | [&check;](Question_51_60/answers/answer_59.py) | | 
| 55 | [テンプレートマッチング SAD](Question_51_60#q55-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%9E%E3%83%83%E3%83%81%E3%83%B3%E3%82%B0-sad) | [&check;](Question_51_60/answers/answer_55.py) | |  | 60 | [アルファブレンド](Question_51_60#q60-%E3%82%A2%E3%83%AB%E3%83%95%E3%82%A1%E3%83%96%E3%83%AC%E3%83%B3%E3%83%89) | [&check;](Question_51_60/answers/answer_60.py) | | 

### [問題61 - 70](Question_61_70)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 61 | [4-連結数](Question_61_70#q61-4-%E9%80%A3%E7%B5%90%E6%95%B0) | [&check;](Question_61_70/answers/answer_61.py) | |  | 66 | [HOG (Step.1) 勾配強度・勾配角度](Question_61_70#q66-hog-step1-%E5%8B%BE%E9%85%8D%E5%BC%B7%E5%BA%A6%E5%8B%BE%E9%85%8D%E8%A7%92%E5%BA%A6) | [&check;](Question_61_70/answers/answer_66.py) | | 
| 62 | [8-連結数](Question_61_70#q62-8-%E9%80%A3%E7%B5%90%E6%95%B0) | [&check;](Question_61_70/answers/answer_62.py) | |  | 67 | [HOG (Step.2) 勾配ヒストグラム](Question_61_70#q67-hog-step2-%E5%8B%BE%E9%85%8D%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0) | [&check;](Question_61_70/answers/answer_67.py) | | 
| 63 | [細線化](Question_61_70#q63-%E7%B4%B0%E7%B7%9A%E5%8C%96%E5%87%A6%E7%90%86) | [&check;](Question_61_70/answers/answer_63.py) | |  | 68 | [HOG (Step.3) ヒストグラム正規化](Question_61_70#q68-hog-step3-%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0%E6%AD%A3%E8%A6%8F%E5%8C%96) | [&check;](Question_61_70/answers/answer_68.py) | | 
| 64**未** | [ヒルディッチの細線化](Question_61_70#q64-%E3%83%92%E3%83%AB%E3%83%87%E3%82%A3%E3%83%83%E3%83%81%E3%81%AE%E7%B4%B0%E7%B7%9A%E5%8C%96) | | | | 69 | [HOG (Step.4) 特徴量の描画](Question_61_70#q69-hog-step4-%E7%89%B9%E5%BE%B4%E9%87%8F%E3%81%AE%E6%8F%8F%E7%94%BB) | [&check;](Question_61_70/answers/answer_69.py) | | 
| 65 | [Zhang-Suenの細線化](Question_61_70#q65-zhang-suen%E3%81%AE%E7%B4%B0%E7%B7%9A%E5%8C%96) | [&check;](Question_61_70/answers/answer_65.py) | |  | 70 | [カラートラッキング](Question_61_70#q70-%E3%82%AB%E3%83%A9%E3%83%BC%E3%83%88%E3%83%A9%E3%83%83%E3%82%AD%E3%83%B3%E3%82%B0) | [&check;](Question_61_70/answers/answer_70.py) | | 

### [問題71 - 80](Question_71_80)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 71 | [マスキング](Question_71_80#q71-%E3%83%9E%E3%82%B9%E3%82%AD%E3%83%B3%E3%82%B0) | [&check;](Question_71_80/answers/answer_71.py) | |  | 76 | [顕著性マップ](Question_71_80#q76-%E9%A1%95%E8%91%97%E6%80%A7%E3%83%9E%E3%83%83%E3%83%97) | [&check;](Question_71_80/answers/answer_76.py) | | 
| 72 | [マスキング(カラートラッキングとモルフォロジー)](Question_71_80#q72-%E3%83%9E%E3%82%B9%E3%82%AD%E3%83%B3%E3%82%B0%E3%82%AB%E3%83%A9%E3%83%BC%E3%83%88%E3%83%A9%E3%83%83%E3%82%AD%E3%83%B3%E3%82%B0%E3%83%A2%E3%83%AB%E3%83%95%E3%82%A9%E3%83%AD%E3%82%B8%E3%83%BC) | [&check;](Question_71_80/answers/answer_72.py) | | | 77 | [ガボールフィルタ](Question_71_80#q77-%E3%82%AC%E3%83%9C%E3%83%BC%E3%83%AB%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF) | [&check;](Question_71_80/answers/answer_77.py) | | 
| 73 | [縮小と拡大](Question_71_80#q73-%E7%B8%AE%E5%B0%8F%E3%81%A8%E6%8B%A1%E5%A4%A7) | [&check;](Question_71_80/answers/answer_73.py) | |  | 78 | [ガボールフィルタの回転](Question_71_80#q78-%E3%82%AC%E3%83%9C%E3%83%BC%E3%83%AB%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%81%AE%E5%9B%9E%E8%BB%A2) | [&check;](Question_71_80/answers/answer_78.py) | | 
| 74 | [ピラミッド差分による高周波成分の抽出](Question_71_80#q74-%E3%83%94%E3%83%A9%E3%83%9F%E3%83%83%E3%83%89%E5%B7%AE%E5%88%86%E3%81%AB%E3%82%88%E3%82%8B%E9%AB%98%E5%91%A8%E6%B3%A2%E6%88%90%E5%88%86%E3%81%AE%E6%8A%BD%E5%87%BA) | [&check;](Question_71_80/answers/answer_74.py) | |  | 79 | [ガボールフィルタによるエッジ抽出](Question_71_80#q79-%E3%82%AC%E3%83%9C%E3%83%BC%E3%83%AB%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%81%AB%E3%82%88%E3%82%8B%E3%82%A8%E3%83%83%E3%82%B8%E6%8A%BD%E5%87%BA) | [&check;](Question_71_80/answers/answer_79.py) | | 
| 75 | [ガウシアンピラミッド](Question_71_80#q75-%E3%82%AC%E3%82%A6%E3%82%B7%E3%82%A2%E3%83%B3%E3%83%94%E3%83%A9%E3%83%9F%E3%83%83%E3%83%89) | [&check;](Question_71_80/answers/answer_75.py) | |  | 80 | [ガボールフィルタによる特徴抽出](Question_71_80#q80-%E3%82%AC%E3%83%9C%E3%83%BC%E3%83%AB%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%81%AB%E3%82%88%E3%82%8B%E7%89%B9%E5%BE%B4%E6%8A%BD%E5%87%BA) | [&check;](Question_71_80/answers/answer_80.py) | | 

### [問題81 - 90](Question_81_90)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 81 | [Hessianのコーナー検出](Question_81_90#q81-hessian%E3%81%AE%E3%82%B3%E3%83%BC%E3%83%8A%E3%83%BC%E6%A4%9C%E5%87%BA) | [&check;](Question_81_90/answers/answer_81.py) | |  | 86 | [簡単な画像認識 (Step.3) 評価(Accuracy)](Question_81_90#q86-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98-step3-%E8%A9%95%E4%BE%A1accuracy) | [&check;](Question_81_90/answers/answer_86.py) | |  
| 82 | [Harrisのコーナー検出 (Step.1) Sobel + Gaussian](Question_81_90#q82-harris%E3%81%AE%E3%82%B3%E3%83%BC%E3%83%8A%E3%83%BC%E6%A4%9C%E5%87%BA-step1-sobel--gauusian) | [&check;](Question_81_90/answers/answer_82.py) | |  | 87 | [簡単な画像認識 (Step.4) k-NN](Question_81_90#q87-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98-step4-k-nn) | [&check;](Question_81_90/answers/answer_87.py) | |  
| 83 | [Harrisのコーナー検出 (Step.2) コーナー検出](Question_81_90#q83-harris%E3%81%AE%E3%82%B3%E3%83%BC%E3%83%8A%E3%83%BC%E6%A4%9C%E5%87%BA-step2-%E3%82%B3%E3%83%BC%E3%83%8A%E3%83%BC%E6%A4%9C%E5%87%BA) | [&check;](Question_81_90/answers/answer_83.py) | |  | 88 | [K-means (Step.1) 重心作成](Question_81_90#q88-k-means-step1-%E9%87%8D%E5%BF%83%E4%BD%9C%E6%88%90) | [&check;](Question_81_90/answers/answer_88.py) | |  
| 84 | [簡単な画像認識 (Step.1) 減色化 + ヒストグラム](Question_81_90#q84-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98-step1-%E6%B8%9B%E8%89%B2%E5%8C%96--%E3%83%92%E3%82%B9%E3%83%88%E3%82%B0%E3%83%A9%E3%83%A0) | [&check;](Question_81_90/answers/answer_84.py) | |   | 89 | [K-means (Step.2) クラスタリング](Question_81_90#q89-k-means-step2-%E3%82%AF%E3%83%A9%E3%82%B9%E3%82%BF%E3%83%AA%E3%83%B3%E3%82%B0) | [&check;](Question_81_90/answers/answer_89.py) | |  
| 85 | [簡単な画像認識 (Step.2) クラス判別](Question_81_90#q85-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98-step2-%E3%82%AF%E3%83%A9%E3%82%B9%E5%88%A4%E5%88%A5) | [&check;](Question_81_90/answers/answer_85.py) | |  | 90 | [K-means (Step.3) 初期ラベルの変更](Question_81_90#q90-k-means-step3-%E5%88%9D%E6%9C%9F%E3%83%A9%E3%83%99%E3%83%AB%E3%81%AE%E5%A4%89%E6%9B%B4) | [&check;](Question_81_90/answers/answer_90.py) | |  

### [問題91 - 100](Question_91_100)

|番号|問題| Python | C++ | |番号|問題| Python | C++ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 91 | [K-meansによる減色処理 (Step.1) 色の距離によるクラス分類](Question_91_100#q91-k-means%E3%81%AB%E3%82%88%E3%82%8B%E6%B8%9B%E8%89%B2%E5%87%A6%E7%90%86-step1-%E8%89%B2%E3%81%AE%E8%B7%9D%E9%9B%A2%E3%81%AB%E3%82%88%E3%82%8B%E3%82%AF%E3%83%A9%E3%82%B9%E5%88%86%E9%A1%9E) | [&check;](Question_91_100/answers/answer_91.py) | |   | 96 | [ニューラルネットワーク (Step.2) 学習](Question_91_100#q96-%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF-step2-%E5%AD%A6%E7%BF%92) | [&check;](Question_91_100/answers/answer_96.py) | |
| 92 | [K-meansによる減色処理 (Step.2) 減色処理](Question_91_100#q92-k-means%E3%81%AB%E3%82%88%E3%82%8B%E6%B8%9B%E8%89%B2%E5%87%A6%E7%90%86-step2-%E6%B8%9B%E8%89%B2%E5%87%A6%E7%90%86) | [&check;](Question_91_100/answers/answer_92.py) | | | 97 | [簡単な物体検出 (Step.1) スライディングウィンドウ + HOG](Question_91_100#q97-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%89%A9%E4%BD%93%E6%A4%9C%E5%87%BA-step1-%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%87%E3%82%A3%E3%83%B3%E3%82%B0%E3%82%A6%E3%82%A3%E3%83%B3%E3%83%89%E3%82%A6--hog) | [&check;](Question_91_100/answers/answer_97.py) | |
| 93 | [機械学習の学習データの用意 (Step.1) IoUの計算](Question_91_100#q93-%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%AD%A6%E7%BF%92%E3%83%87%E3%83%BC%E3%82%BF%E3%81%AE%E7%94%A8%E6%84%8F-step1-iou%E3%81%AE%E8%A8%88%E7%AE%97) | [&check;](Question_91_100/answers/answer_93.py) | | | 98 | [簡単な物体検出 (Step.2) スライディングウィンドウ + NN](Question_91_100#q98-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%89%A9%E4%BD%93%E6%A4%9C%E5%87%BA-step2-%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%87%E3%82%A3%E3%83%B3%E3%82%B0%E3%82%A6%E3%82%A3%E3%83%B3%E3%83%89%E3%82%A6--nn) | [&check;](Question_91_100/answers/answer_98.py) | |
| 94 | [機械学習の学習データの用意 (Step.2) ランダムクラッピング](Question_91_100#q94-%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%AD%A6%E7%BF%92%E3%83%87%E3%83%BC%E3%82%BF%E3%81%AE%E7%94%A8%E6%84%8F-step2-%E3%83%A9%E3%83%B3%E3%83%80%E3%83%A0%E3%82%AF%E3%83%A9%E3%83%83%E3%83%94%E3%83%B3%E3%82%B0) | [&check;](Question_91_100/answers/answer_94.py) | | | 99 | [簡単な物体検出 (Step.3) Non-Maximum Suppression](Question_91_100#q99-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%89%A9%E4%BD%93%E6%A4%9C%E5%87%BA-step3-non-maximum-suppression) | [&check;](Question_91_100/answers/answer_99.py) | |
| 95 | [ニューラルネットワーク (Step.1) ディープラーニングにする](Question_91_100#q95-%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF-step1-%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AB%E3%81%99%E3%82%8B) | [&check;](Question_91_100/answers/answer_95.py) | | | 100 | [簡単な物体検出 (Step.4) 評価 Precision, Recall, F-score, mAP](Question_91_100#q100-%E7%B0%A1%E5%8D%98%E3%81%AA%E7%89%A9%E4%BD%93%E6%A4%9C%E5%87%BA-step4-%E8%A9%95%E4%BE%A1-precision-recall-f-score-map) | [&check;](Question_91_100/answers/answer_100.py) | |


## TODO

adaptivebinalizatino, poison image blending

## Citation

```bash
@article{yoyoyo-yoGasyori100knock,
    Author = {yoyoyo-yo},
    Title = {Gasyori100knock},
    Journal = {https://github.com/yoyoyo-yo/Gasyori100knock},
    Year = {2019}
}
```

## License

&copy; tired imori All Rights Reserved.

This is under MIT License.

> https://github.com/yoyoyo-yo/Gasyori100knock/blob/master/LICENSE

