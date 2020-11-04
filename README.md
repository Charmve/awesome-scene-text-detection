# Scene-Text-Detection
Tracking the latest progress in Scene Text Detection and Recognition: Must-read papers well organized with code and dataset.

<p align='right'>Author: <a href="https://github.com/Charmve" target="_blank">Wei ZHANG</a></p>

<!-- MarkdownTOC -->

- [1.Datasets](#1-datasets)
    - [1.1 Horizontal-Text Datasets](#11-Horizontal-Text-Datasets)
    - [1.2 Arbitrary-Quadrilateral-Text Datasets](#12-Arbitrary-Quadrilateral-Text-Datasets)
    - [1.3 Irregular-Text Datasets](#13-Irregular-Text-Datasets)
    - [1.4 Synthetic Datasets](#14-synthetic-datasets)
    - [1.5 Comparison of Datasets](#15-comparison-of-datasets)
- [2. Survey](#2-survey)
- [3. Evaluation](#3-Evaluation)
- [4. OCR Service](#4-ocr-service)
- [5. References and Code](#5-references)

<!-- /MarkdownTOC -->

------


## ✨ News! ✨
- <font size="4"><b>2020.11.04:</b> 21 papers was updated from <a href="http://cvpr2020.thecvf.com/" target="_blank">CVPR 2020</a>!</font>
Go to 📑 <a href="https://github.com/Charmve/Scene-Text-Detection/blob/main/README.md#5-references" target="_blank">5. References and Code</a> or :open_file_folder: <a href="./STD-CVPR2020.md" target="_blank">References and Code(CVPR2020)</a>
<br>
- <font size="4"><b>2020.10.12:</b> A detailed survey was organized from <a href="https://www.ijcv.org/" target="_blank">IJCV 2020</a>!</font>
Go to :open_file_folder: <a href="./Scene%20Text%20Survey.md" target="_blank">Scene Text Detection Survey</a>
	<!--
   <li><font size="4"><b>2020.03.24:</b> 4 paper was accepted by <a href="https://www.2020.ieeeicme.org/" target="_blank">ICME 2020</a> !</font></li>
 -->
<br>

<a id="1-datasets"></a>
## 1. Datasets

<a id="11-Horizontal-Text-Datasets"></a>
### 1.1 Horizontal-Text Datasets

- ICDAR 2003(IC03)：
  * **Introduction:** It contains 509 images in total, 258 for training and 251 for testing. Specifically, it contains 1110 text instance in training set, while 1156 in testing set. It has word-level annotation. IC03 only consider English text instance.
  * **Link:** [IC03-download](http://www.iapr-tc11.org/mediawiki/index.php?title=ICDAR_2003_Robust_Reading_Competitions)

- ICDAR 2011(IC11):
  * **Introduction:** IC11 is an English dataset for text detection.  It contains 484 images, 229 for training and 255 for testing. There are 1564 text instance in this dataset. It provides both word-level and character-level annotation.
  * **Link:** [IC11-download](http://www.cvc.uab.es/icdar2011competition/?com=downloads)   

- ICDAR 2013(IC13)：
  * **Introduction:** IC13 is almost the same as IC11. It contains 462 images in total, 229 for training and 233 for testing. Specifically, it contains 849 text instance in training set, while 1095 in testing set.
  * **Link:** [IC13-download](http://dagdata.cvc.uab.es/icdar2013competition/?ch=2&com=downloads)

<a id="12-Arbitrary-Quadrilateral-Text-Datasets"></a>
### 1.2 Arbitrary-Quadrilateral-Text Datasets

- USTB-SV1K：
  * **Introduction:** USTB-SV1K is an English dataset.  It contains 1000 street images from Google Street View  with  2955 text instance  in total. It only provides word-level annotations.  
  * **Link:** [USTB-SV1K-download](http://prir.ustb.edu.cn/TexStar/MOMV-text-detection/)

- SVT：
  * **Introduction:** It contains 350 images with 725 English text intance in total. SVT has both character-level and word-level annotations. The images of SVT are harvested from Google Street View and have low resolution.
  * **Link:** [SVT-download](http://vision.ucsd.edu/~kai/grocr/)

- SVT-P：
  - **Introduction:** It contains 639 cropped word images for testing. Images were selected from the side-view angle snapshots in Google Street View. Therefore, most images are heavily distorted by the non-frontal view angle. It is the imporved datasets of SVT.
  - **Link:** [SVT-P-download](https://pan.baidu.com/s/1rhYUn1mIo8OZQEGUZ9Nmrg )  \(Password : vnis)

- ICDAR 2015(IC15)：
  - **Introduction:** It contains 1500 images in total, 1000 for training and 500 for testing. Specifically, it contains 17548 text instance. It provides word-level annotations. IC15 is the first incidental scene text dataset and it only considers English words.
  - **Link:** [IC15-download](http://rrc.cvc.uab.es/?ch=4&com=downloads)

- COCO-Text：
  - **Introduction:** It contains 63686 images in total, 43686 for training, 10000 for validating and 10000 for testing. Specifically, it contains 145859  cropped word images for testing, including handwritten and printed, clear and blur, English and non-English.
  - **Link:** [COCO-Text-download](https://vision.cornell.edu/se3/coco-text-2/)

- MSRA-TD500：
  - **Introduction:** It contains 500 images in total. It provides text-line-level annotation rather than word, and polygon boxes rather than axis-aligned rectangles for text region annootation. It contains both English and Chinese text instance.
  - **Link:** [MSRA-TD500-download](http://pages.ucsd.edu/~ztu/Download_front.htm)

- MLT 2017：
  - **Introduction:** It contains 10000 natural images in total. It provides word-level annotation. There are 9 languages for MLT. It is a more real and complex datasets for scene text detection and recognition..
  - **Link:** [MLT-download](http://rrc.cvc.uab.es/?ch=8)

- MLT 2019:
  - **Introduction:** It contains 18000 images in total. It provides word-level annotation. Compared to MLT,  this dataset has 10 languages. It is a more real and complex datasets for scene text detection and recognition..
  - **Link:** [MLT-2019-download](http://rrc.cvc.uab.es/?ch=15)

- CTW：
  - **Introduction:** It contains 32285 high resolution street view images of Chinese text, with 1018402 character instances in total. All images are annotated at the character level, including its underlying character type, bouding box, and 6 other attributes. These attributes indicate whether its background is complex, whether it’s raised, whether it’s hand-written or printed, whether it’s occluded, whether it’s distorted, whether it uses word-art.
  - **Link:** [CTW-download](https://ctwdataset.github.io/)

- RCTW-17：
  - **Introduction:** It contains 12514 images in total, 11514 for training and 1000 for testing. Images in RCTW-17 were mostly collected by camera or mobile phone, and others were generated images. Text instances are annotated with parallelograms. It is the first large scale Chinese dataset, and was also the largest published one by then.
  - **Link:** [RCTW-17-download](http://rctw.vlrlab.net/dataset/)

- ReCTS：
  - **Introduction:** This data set is a large-scale Chinese Street View Trademark Data Set. It is based on Chinese words and Chinese text line-level labeling. The labeling method is arbitrary quadrilateral labeling. It contains 20000 images in total.
  - **Link:** [ReCTS-download](http://rrc.cvc.uab.es/?ch=12)

<a id="13-Irregular-Text-Datasets"></a>
### 1.3 Irregular-Text Datasets

- CUTE80：
  - **Introduction:** It contains 80 high-resolution images taken in natural scenes. Specifically, it contains 288 cropped word images for testing. The dataset focuses on curved text. No lexicon is provided.
  - **Link:** [CUTE80-download](http://cs-chan.com/downloads_CUTE80_dataset.html)

- Total-Text：
  - **Introduction:** It contains 1,555 images in total. Specifically, it contains 11,459  cropped word images with more than three different text orientations: horizontal, multi-oriented and curved.
  - **Link:** [Total-Text-download](https://github.com/cs-chan/Total-Text-Dataset)

- SCUT-CTW1500：
  - **Introduction:** It contains 1500 images in total, 1000 for training and 500 for testing. Specifically, it contains 10751 cropped word images for testing. Annotations in CTW-1500 are polygons with 14 vertexes. The dataset mainly consists of Chinese and English.
  - **Link:** [CTW-1500-download](https://github.com/Yuliang-Liu/Curve-Text-Detector)

- LSVT：
  - **Introduction:** LSVT consists of 20,000 testing data, 30,000 training data in full annotations and 400,000 training data in weak annotations, which are referred to as partial labels. The labeled text regions demonstrate the diversity of text: horizontal, multi-oriented and curved.
  - **Link:** [LSVT-download](https://rrc.cvc.uab.es/?ch=16)

- ArTs：
  - **Introduction:** ArT consists of 10,166 images, 5,603 for training and 4,563 for testing. They were collected with text shape diversity in mind and all text shapes have high number of existence in ArT.
  - **Link:** [ArT-download](https://rrc.cvc.uab.es/?ch=14)

<a id="14-synthetic-datasets"></a>
### 1.4 Synthetic Datasets

* Synth80k :
  * **Introduction:** It contains 800 thousands images with approximately 8 million synthetic word instances. Each text instance is annotated with its text-string, word-level and character-level bounding-boxes.
  * **Link:** [Synth80k-download](http://www.robots.ox.ac.uk/~vgg/data/scenetext/)

* SynthText :
  * **Introduction:** It contains 6 million cropped word images. The generation process is similar to that of Synth90k. It is also annotated in horizontal-style.  
  * **Link:** [SynthText-download](https://github.com/ankush-me/SynthText)

<a id="15-comparison-of-datasets"></a>

### 1.5 Comparison of Datasets

<body>
<table cellspacing="0" border="0">
	<colgroup width="85"></colgroup>
	<colgroup width="119"></colgroup>
	<colgroup span="7" width="85"></colgroup>
	<colgroup width="153"></colgroup>
	<colgroup width="104"></colgroup>
	<colgroup span="3" width="85"></colgroup>
	<tr>
		<td colspan=14 height="20" align="center"><b>Comparison of Datasets</b></td>
		</tr>
	<tr>
		<td rowspan=2 height="39" align="center" valign=top><b>Datasets</b></td>
		<td rowspan=2 align="center" valign=top><b>Language</b></td>
		<td colspan=3 align="center"><b>Image</b></td>
		<td colspan=3 align="center"><b>Text instance </b></td>
		<td colspan=3 align="center"><b>Text Shape</b></td>
		<td colspan=3 align="center"><b>Annotation level</b></td>
		</tr>
	<tr>
		<td align="center"><b>Total</b></td>
		<td align="center"><b>Train</b></td>
		<td align="center"><b>Test</b></td>
		<td align="center"><b>Total</b></td>
		<td align="center"><b>Train</b></td>
		<td align="center"><b>Test</b></td>
		<td align="center"><b>Horizontal</b></td>
		<td align="center"><b>Arbitrary-Quadrilateral</b></td>
		<td align="center"><b>Multi-oriented</b></td>
		<td align="center"><b>Char</b></td>
		<td align="center"><b>Word</b></td>
		<td align="center"><b>Text-Line</b></td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC03</b></td>
		<td align="center">English</td>
		<td align="center" sdval="509" sdnum="2052;">509</td>
		<td align="center" sdval="258" sdnum="2052;">258</td>
		<td align="center" sdval="251" sdnum="2052;">251</td>
		<td align="center" sdval="2266" sdnum="2052;">2266</td>
		<td align="center" sdval="1110" sdnum="2052;">1110</td>
		<td align="center" sdval="1156" sdnum="2052;">1156</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC11</b></td>
		<td align="center">English</td>
		<td align="center" sdval="484" sdnum="2052;">484</td>
		<td align="center" sdval="229" sdnum="2052;">229</td>
		<td align="center" sdval="255" sdnum="2052;">255</td>
		<td align="center" sdval="1564" sdnum="2052;">1564</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC13</b></td>
		<td align="center">English</td>
		<td align="center" sdval="462" sdnum="2052;">462</td>
		<td align="center" sdval="229" sdnum="2052;">229</td>
		<td align="center" sdval="233" sdnum="2052;">233</td>
		<td align="center" sdval="1944" sdnum="2052;">1944</td>
		<td align="center" sdval="849" sdnum="2052;">849</td>
		<td align="center" sdval="1095" sdnum="2052;">1095</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>USTB-SV1K</b></td>
		<td align="center">English</td>
		<td align="center" sdval="1000" sdnum="2052;">1000</td>
		<td align="center" sdval="500" sdnum="2052;">500</td>
		<td align="center" sdval="500" sdnum="2052;">500</td>
		<td align="center" sdval="2955" sdnum="2052;">2955</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>SVT</b></td>
		<td align="center">English</td>
		<td align="center" sdval="350" sdnum="2052;">350</td>
		<td align="center" sdval="100" sdnum="2052;">100</td>
		<td align="center" sdval="250" sdnum="2052;">250</td>
		<td align="center" sdval="725" sdnum="2052;">725</td>
		<td align="center" sdval="211" sdnum="2052;">211</td>
		<td align="center" sdval="514" sdnum="2052;">514</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>SVT-P</b></td>
		<td align="center">English</td>
		<td align="center" sdval="238" sdnum="2052;">238</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center" sdval="639" sdnum="2052;">639</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>IC15</b></td>
		<td align="center">English</td>
		<td align="center" sdval="1500" sdnum="2052;">1500</td>
		<td align="center" sdval="1000" sdnum="2052;">1000</td>
		<td align="center" sdval="500" sdnum="2052;">500</td>
		<td align="center" sdval="17548" sdnum="2052;">17548</td>
		<td align="center" sdval="122318" sdnum="2052;">122318</td>
		<td align="center" sdval="5230" sdnum="2052;">5230</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>COCO-Text</b></td>
		<td align="center">English</td>
		<td align="center" sdval="63686" sdnum="2052;">63686</td>
		<td align="center" sdval="43686" sdnum="2052;">43686</td>
		<td align="center" sdval="20000" sdnum="2052;">20000</td>
		<td align="center" sdval="145859" sdnum="2052;">145859</td>
		<td align="center" sdval="118309" sdnum="2052;">118309</td>
		<td align="center" sdval="27550" sdnum="2052;">27550</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>MSRA-TD500</b></td>
		<td align="center">English/Chinese</td>
		<td align="center" sdval="500" sdnum="2052;">500</td>
		<td align="center" sdval="300" sdnum="2052;">300</td>
		<td align="center" sdval="200" sdnum="2052;">200</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>MLT 2017</b></td>
		<td align="center">Multi-lingual</td>
		<td align="center" sdval="18000" sdnum="2052;">18000</td>
		<td align="center" sdval="7200" sdnum="2052;">7200</td>
		<td align="center" sdval="10800" sdnum="2052;">10800</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>MLT 2019</b></td>
		<td align="center">Multi-lingual</td>
		<td align="center" sdval="20000" sdnum="2052;">20000</td>
		<td align="center" sdval="10000" sdnum="2052;">10000</td>
		<td align="center" sdval="10000" sdnum="2052;">10000</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>CTW</b></td>
		<td align="center">Chinese</td>
		<td align="center" sdval="32285" sdnum="2052;">32285</td>
		<td align="center" sdval="25887" sdnum="2052;">25887</td>
		<td align="center" sdval="6398" sdnum="2052;">6398</td>
		<td align="center" sdval="1018402" sdnum="2052;">1018402</td>
		<td align="center" sdval="812872" sdnum="2052;">812872</td>
		<td align="center" sdval="205530" sdnum="2052;">205530</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>RCTW-17</b></td>
		<td align="center">English/Chinese</td>
		<td align="center" sdval="12514" sdnum="2052;">12514</td>
		<td align="center" sdval="15114" sdnum="2052;">15114</td>
		<td align="center" sdval="1000" sdnum="2052;">1000</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>ReCTS</b></td>
		<td align="center">Chinese</td>
		<td align="center" sdval="20000" sdnum="2052;">20000</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>CUTE80</b></td>
		<td align="center">English</td>
		<td align="center" sdval="80" sdnum="2052;">80</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>Total-Text</b></td>
		<td align="center">English</td>
		<td align="center" sdval="1525" sdnum="2052;">1525</td>
		<td align="center" sdval="1225" sdnum="2052;">1225</td>
		<td align="center" sdval="300" sdnum="2052;">300</td>
		<td align="center" sdval="9330" sdnum="2052;">9330</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>CTW-1500</b></td>
		<td align="center">English/Chinese</td>
		<td align="center" sdval="1500" sdnum="2052;">1500</td>
		<td align="center" sdval="1000" sdnum="2052;">1000</td>
		<td align="center" sdval="500" sdnum="2052;">500</td>
		<td align="center" sdval="10751" sdnum="2052;">10751</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>LSVT</b></td>
		<td align="center">English/Chinese</td>
		<td align="center" sdval="450000" sdnum="2052;">450000</td>
		<td align="center" sdval="430000" sdnum="2052;">430000</td>
		<td align="center" sdval="20000" sdnum="2052;">20000</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
	</tr>
  <tr>
    <td height="20" align="center"><b>ArT</b></td>
    <td align="center">English/Chinese</td>
    <td align="center" sdval="450000" sdnum="2052;">10166</td>
    <td align="center" sdval="430000" sdnum="2052;">5603</td>
    <td align="center" sdval="20000" sdnum="2052;">4563</td>
    <td align="center">～</td>
    <td align="center">～</td>
    <td align="center">～</td>
    <td align="center">✓</td>
    <td align="center">✓</td>
    <td align="center">✓</td>
    <td align="center" sdnum="2052;0;@">✕</td>
    <td align="center">✓</td>
    <td align="center">✕</td>
  </tr>
	<tr>
		<td height="20" align="center"><b>Synth80k</b></td>
		<td align="center">English</td>
		<td align="center">80k</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">8m</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
	<tr>
		<td height="20" align="center"><b>SynthText </b></td>
		<td align="center">English</td>
		<td align="center">800k</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">6m</td>
		<td align="center">～</td>
		<td align="center">～</td>
		<td align="center">✓</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center" sdnum="2052;0;@">✕</td>
		<td align="center">✓</td>
		<td align="center" sdnum="2052;0;@">✕</td>
	</tr>
</table>

<a id="2-survey"></a>
## 2. Survey
**[A] \[IJCV-2020]** Shangbang Long, Xin He, Cong Yao. **Scene Text Detection and Recognition: The Deep Learning Era**[J]. International Journal of Computer Vision, 2020, 1--24. [arXiv](https://arxiv.org/abs/1811.04256)

**[B] \[TPAMI-2015]** Ye Q, Doermann D. **Text detection and recognition in imagery: A survey**[J]. IEEE transactions on pattern analysis and machine intelligence, 2015, 37(7): 1480-1500. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6945320)

**[C] \[Frontiers-Comput. Sci-2016]** Zhu Y, Yao C, Bai X. **Scene text detection and recognition: Recent advances and future trends**[J]. Frontiers of Computer Science, 2016, 10(1): 19-36. [paper](https://link.springer.com/article/10.1007/s11704-015-4488-0)

**[D] \[arXiv-2018]** Long S, He X, Ya C. **Scene Text Detection and Recognition: The Deep Learning Era**[J]. arXiv preprint arXiv:1811.04256, 2018. [paper](https://arxiv.org/pdf/1811.04256.pdf)

<a id="3-Evaluation"></a>
## 3. Evaluation

If you are insterested in developing better scene text detection metrics, some references recommended here might be useful.

**[A]** Wolf, Christian, and Jean-Michel Jolion. "**Object count/area graphs for the evaluation of object detection and segmentation algorithms.**" International Journal of Document Analysis and Recognition (IJDAR) 8.4 (2006): 280-296. [paper](https://link.springer.com/article/10.1007/s10032-006-0014-0)

**[B]** D. Karatzas, L. Gomez-Bigorda, A. Nicolaou, S. K. Ghosh, A. D.Bagdanov, M. Iwamura, J. Matas, L. Neumann, V. R. Chandrasekhar, S. Lu, F. Shafait, S. Uchida, and E. Valveny. **ICDAR 2015 competition on robust reading**. In ICDAR, pages 1156–1160, 2015. [paper](https://ieeexplore.ieee.org/document/7333942)

**[C]** Calarasanu, Stefania, Jonathan Fabrizio, and Severine Dubuisson. "**What is a good evaluation protocol for text localization systems? Concerns, arguments, comparisons and solutions.**" Image and Vision Computing 46 (2016): 1-17. [paper](https://www.sciencedirect.com/science/article/pii/S0262885615001377)

**[D]** Shi, Baoguang, et al. "**ICDAR2017 competition on reading chinese text in the wild (RCTW-17).**" 2017 14th IAPR International Conference on Document Analysis and Recognition (ICDAR). Vol. 1. IEEE, 2017. [paper](https://ieeexplore.ieee.org/abstract/document/8270164)

**[E]** Nayef, N; Yin, F; Bizid, I; et al. **ICDAR2017 robust reading challenge on multi-lingual scene text detection and script identiﬁcation-rrc-mlt**. In Document Analysis and Recognition (ICDAR), 2017 14th IAPR International Conference on, volume 1, 1454–1459. IEEE.
[paper](https://ieeexplore.ieee.org/document/8270168)

**[F]** Dangla, Aliona, et al. "**A first step toward a fair comparison of evaluation protocols for text detection algorithms.**" 2018 13th IAPR International Workshop on Document Analysis Systems (DAS). IEEE, 2018. [paper](https://ieeexplore.ieee.org/abstract/document/8395220)

**[G]** He,Mengchao and Liu, Yuliang, et al. **ICPR2018 Contest on Robust Reading for Multi-Type Web images.** ICPR 2018. [paper](https://www.researchgate.net/publication/329316151_ICPR2018_Contest_on_Robust_Reading_for_Multi-Type_Web_Images)

**[H]** Liu, Yuliang and Jin, Lianwen, et al. "**Tightness-aware Evaluation Protocol for Scene Text Detection**" Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR). 2019. [paper](https://arxiv.org/abs/1904.00813) [code](https://github.com/Yuliang-Liu/TIoU-metric)



<a id="4-ocr-service"></a>
## 4. OCR Service

|                             OCR                              | API  | Free |
| :----------------------------------------------------------: | :--: | :--: |
| [Tesseract OCR Engine](https://github.com/tesseract-ocr/tesseract) |  ×   |  √   |
| [Azure](https://azure.microsoft.com/zh-cn/services/cognitive-services/computer-vision/#Analysis) |  √   |  √   |
| [ABBYY](https://www.abbyy.cn/real-time-recognition-sdk/technical-specifications/) |  √   |  √   |
|               [OCR Space](https://ocr.space/)                |  √   |  √   |
|       [SODA PDF OCR](https://www.sodapdf.com/ocr-pdf/)       |  √   |  √   |
|          [Free Online OCR](https://www.newocr.com/)          |  √   |  √   |
|           [Online OCR](https://www.onlineocr.net/)           |  √   |  √   |
|             [Super Tools](https://www.wdku.net/)             |  √   |  √   |
|          [Online Chinese Recognition](http://chongdata.com/ocr/)           |  √   |  √   |
|   [Calamari OCR](https://github.com/Calamari-OCR/calamari)   |  ×   |  √   |
|   [Tencent OCR](https://cloud.tencent.com/product/ocr?lang=cn)   |  √   |  ×   |


<a id="5-references"></a>
## 5. References and Code

## 场景文本检测

### 深度关系推理图网络用于任意形状文本检测

[1].Deep Relational Reasoning Graph Network for Arbitrary Shape Text Detection

作者 | Shi-Xue Zhang, Xiaobin Zhu, Jie-Bo Hou, Chang Liu, Chun Yang, Hongfa Wang, Xu-Cheng Yin

单位 | 北京科技大学；中国科学技术大学人工智能联合实验室；腾讯科技（深圳）

代码 | https://github.com/GXYM/DRRG

备注 | CVPR 2020 Oral

解读 | https://blog.csdn.net/SpicyCoder/article/details/105072570

 
<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzN5ZGpybFFCVkUxbVQ1Z3g5aFVrRDg4YzlVbThnWUpHdDQ2OGN0Y1cydW54emtLRThlOGFqdlEvNjQw?x-oss-process=image/format,png">
</div>


[2].ContourNet: Taking a Further Step Toward Accurate Arbitrary-Shaped Scene Text Detection

作者 | Yuxin Wang, Hongtao Xie, Zheng-Jun Zha, Mengting Xing, Zilong Fu, Yongdong Zhang

单位 | 中国科学技术大学

代码 | https://github.com/wangyuxin87/ContourNet

解读 | https://zhuanlan.zhihu.com/p/135399747
 
<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNpYmliRzh0UGhGRFhGUTM3Z2NuMzdVWEFkU3NQdVc0ekZFT2pkZEpUQTJMVVZyWFJHNGlhVWZWaWN3LzY0MA?x-oss-process=image/format,png">
</div>

## 场景文本识别

### 论场景文本识别中的词汇依赖性

[3].On Vocabulary Reliance in Scene Text Recognition

作者 | Zhaoyi Wan, Jielei Zhang, Liang Zhang, Jiebo Luo, Cong Yao

单位 | 旷视；中国矿业大学；罗切斯特大学

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNQV2NveDhvRTRybWplcWc0dGliRDVHOXNpYlN5d1dNVEl3Y2M2QUtxazlxaWJ0MGNpYm9sckJUSVd3LzY0MA?x-oss-process=image/format,png">
</div>


[4].SCATTER: Selective Context Attentional Scene Text Recognizer

作者 | Ron Litman, Oron Anschel, Shahar Tsiper, Roee Litman, Shai Mazor, R. Manmatha

单位 | Amazon Web Services

 
<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzM2YlYyQllSY2ZuUk9CUTZJWG5ZQWI2MkRYekRpYTc0eXVHbXNnemp1N3FzQnhkWUNESVZxd2FBLzY0MA?x-oss-process=image/format,png">
</div>


### 语义推理网络，用于场景文本的精确识别

[5].Towards Accurate Scene Text Recognition With Semantic Reasoning Networks

作者 | Deli Yu, Xuan Li, Chengquan Zhang, Tao Liu, Junyu Han, Jingtuo Liu, Errui Ding

单位 | 国科大；百度；中科院

代码 | https://github.com/chenjun2hao/SRN.pytorch

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzN0Tmw4ZzFQR3d3cGtxSlVjeUtBZ0hvNHoxcG5Vd2pscHVXRDR1RVNOU2liNTBWOUlpY1lZenhJQS82NDA?x-oss-process=image/format,png">
</div>

 

### 语义增强的编解码框架，用于识别低质量图像（模糊、光照不均、字符不完整等）场景文本

[6].SEED: Semantics Enhanced Encoder-Decoder Framework for Scene Text Recognition

作者 | Zhi Qiao, Yu Zhou, Dongbao Yang, Yucan Zhou, Weiping Wang

单位 | 中科院；国科大

代码 | https://github.com/Pay20Y/SEED（即将）

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNqY3R0dzQyeUc3RzRtbjQzMTgyZ1dEWG1icEx4ZVFxMGFaQjdXdU1EYWlhY3dBdmV1Sm9LOHF3LzY0MA?x-oss-process=image/format,png">
</div>


## 手写文本识别
 

[7].OrigamiNet: Weakly-Supervised, Segmentation-Free, One-Step, Full Page Text Recognition by learning to unfold

作者 | Mohamed Yousef, Tom E. Bishop

单位 | Intuition Machines, Inc

代码 | https://github.com/IntuitionMachines/OrigamiNet

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNYSTk2V1NJTnFLYlg2YUg2UmliSDlCNjRSNGxiNWpBd2liN09SUXpMZUg0VThjOVBWdk1LTVVuZy82NDA?x-oss-process=image/format,png">
</div>


## Scene Text Spotting
 
### 实时端到端场景文本识别

[8].ABCNet: Real-Time Scene Text Spotting With Adaptive Bezier-Curve Network

作者 | Yuliang Liu, Hao Chen, Chunhua Shen, Tong He, Lianwen Jin, Liangwei Wang

单位 | 华南理工大学；阿德莱德大学；

代码 | https://github.com/Yuliang-Liu/bezier_curve_text_spotting

备注 | CVPR 2020 Oral

解读 | https://zhuanlan.zhihu.com/p/146276834


<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNrNU5hRUJrNFF6aWNSUkJyaWNTaGljR2lhRHdsOWRCeDdLb2lhdU1kY3BtSXpPMmpwT0JUWDRrOHkzQS82NDA?x-oss-process=image/format,png">
</div>

## 手写文本生成

 

半监督变长手写文本生成，增加文本数据集，提高识别算法精度

[9].ScrabbleGAN: Semi-Supervised Varying Length Handwritten Text Generation

作者 | Sharon Fogel, Hadar Averbuch-Elor, Sarel Cohen, Shai Mazor, Roee Litman

单位 | 以色列国，Amazon Rekognition；康奈尔大学

代码 | https://github.com/amzn/convolutional-handwriting-gan

 

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X2dpZi9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNVbmNpY1c2Z2hmNDFNTFkwaGxtdTdCUGNDVzdPYnFJMU9SQWliYUQyRVhQNTZWb05Dam4xajA4QS82NDA?x-oss-process=image/format,png">
</div>

 

## 场景文本合成


使用渲染引擎合成场景文本，增加训练样本，提升识别算法精度

[10].UnrealText: Synthesizing Realistic Scene Text Images From the Unreal 

作者 | WorldShangbang Long, Cong Yao

单位 | 卡内基梅隆大学；旷视

代码 | https://jyouhou.github.io/UnrealText/

解读 | https://zhuanlan.zhihu.com/p/137406773


<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNjc2NQOHY0NlcxbFBQazZYTG1kbVFTY2liQUxaUmljQktpY3FId0puTFRUZUxGSHMyNVU5T1JKUUEvNjQw?x-oss-process=image/format,png">
</div>

 

## 数据增广+文本识别


图像增广用于手写与场景文本识别

[11].Learn to Augment: Joint Data Augmentation and Network Optimization for Text Recognition

作者 | Canjie Luo, Yuanzhi Zhu, Lianwen Jin, Yongpan Wang

单位 | 华南理工大学；阿里

代码 | https://github.com/Canjie-Luo/Text-Image-Augmentation

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzN0Q3FWODZMSjNLVjdMRzVEdFlYbDZkcHZsckl2S2Q4cmJpYWFoYUtoa2MxdXBtc2liakpkZmljVncvNjQw?x-oss-process=image/format,png">
</div>

 

## 场景文本编辑

[12].STEFANN: Scene Text Editor Using Font Adaptive Neural Network

作者 | Prasun Roy, Saumik Bhattacharya, Subhankar Ghosh, Umapada Pal

单位 | 印度统计研究所；印度理工学院

代码 | https://github.com/prasunroy/stefann

网站 | https://prasunroy.github.io/stefann/

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X2pwZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNFdTdDUjdkanVpYnJZdU9COXFocUsxakNiR2sxTEF1MFZVdmljTkZWYXJxaWI2TGh2NklINWlhcWFnLzY0MA?x-oss-process=image/format,png">
</div>


## 碎纸文档重建

破碎纸片重建文档，用于法医等刑侦调查

[13].Fast(er) Reconstruction of Shredded Text Documents via Self-Supervised Deep Asymmetric Metric Learning

作者 | Thiago M. Paixao, Rodrigo F. Berriel, Maria C. S. Boeres, Alessandro L. Koerich, Claudine Badue, Alberto F. De Souza, Thiago Oliveira-Santos

单位 | IFES，Brazil；UFES，Brazil；ETS，Canada
 
<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNnQUJtZ2lhOERHUWVVN3RnWTlpYkhQbGRLYzdkVW1XU2RjZ3dkRE5jRzFrQ3Y5c0JneFZnVzZody82NDA?x-oss-process=image/format,png">
</div>
 

## 文本风格迁移

[14].SwapText: Image Based Texts Transfer in Scenes

作者 | Qiangpeng Yang, Jun Huang, Wei Lin

单位 | 阿里
 
<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNtaWNrYVZHdUdHMDJpYnY2YUd1aWFiYXZpYVpnSXpOemVKckJpYWtPejN5RUFpYVRMeHdTZzBXWjRLUFEvNjQw?x-oss-process=image/format,png">
</div>


## 场景文本识别+对抗攻击

[15].What Machines See Is Not What They Get: Fooling Scene Text Recognition Models With Adversarial Text Images

作者 | Xing Xu, Jiefu Chen, Jinhui Xiao, Lianli Gao, Fumin Shen, Heng Tao Shen

单位 | 电子科技大学

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNtaWNVdnZ0RGlib0Q0dVJXYWJOc1JPdnJRbUJpY3c2OTVDckRCNm1VRjBjdEtHVnNxVXRVT25UOVEvNjQw?x-oss-process=image/format,png">
</div>


## 笔迹鉴定

[16].Sequential Motif Profiles and Topological Plots for Offline Signature Verification

作者 | Elias N. Zois, Evangelos Zervas, Dimitrios Tsourounis, George Economou

单位 | University of West Attica ；派图拉斯大学

<div align=center>
  <img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9CSmJSdndpYmVTVHVjN281d0tjd3hRNkd1ZEg1VHRKRzNiVHdGdG9mRTBBWUtwZUc0ek4ycU52d08wcGdaMmV5UHFLZmsxWWc1cmZXVVBpY2RoQkRnN3ZnLzY0MA?x-oss-process=image/format,png">
</div>

# Contribute & Acknowledge

## Contributing

Feel free to dive in! [Open an issue](https://github.com/Charmve/Scene-Text-Detection/issues/new) or submit PRs. 

## Acknowledge

This project exists thanks to all the people who contribute. 
<a href="graphs/contributors"><img src="https://opencollective.com/standard-readme/contributors.svg?width=890&button=false" /></a>

More sincerely, I'm appreciate to @<a href="https://github.com/HCIILAB" target="_blank">HCIILAB</a> & @<a href="https://github.com/Jyouhou" target="_blank">Jyouhou</a>

# License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a>

# Copyright

Copyright © 2020 MaiweiAI.cn @<a href="https://github.com/Charmve" target="_blank">Charmve</a>. All Rights Reserved.

<!--
<p align="center">
    <img src="https://charmve.github.io/mhy.jpg" alt="Sample"  width="150" height="75">
    <p align="center">
        <em></em>
    </p>
</p>
-->


<div align=right>
  *<i>Last updated in July 2020.</i><br>
</div>
