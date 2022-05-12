# Real-time_finger_number_classification
## > File 설명
+ pytorch-fingers.ipynb
  + pytorch를 이용한 data load부터 model train, test, save 까지.
  
+ finger_webcam.ipynb
  + webcam은 캐글이나 코랩에서 켜지지 않으므로, 위에서 만든 model을 주피터노트북으로 load 해와서 사용. OpenCV 활용.

## > Data
+ 캐글 dataset (https://www.kaggle.com/datasets/koryakinp/fingers)
<img width="200" alt="화면 캡처 2022-05-12 211009" src="https://user-images.githubusercontent.com/68634729/168071687-a6673a98-219d-4c1e-a322-f57fc3caea72.png">

+ 직접 수집한 내 손가락 data..
<img width="200" alt="화면 캡처 2022-05-12 211045" src="https://user-images.githubusercontent.com/68634729/168071734-4e885b38-7d9c-4c42-94b5-23444c168275.png">

## > Model selection
<p align="center"><img src="https://user-images.githubusercontent.com/68634729/168057702-acda8b8f-b0ee-4706-870d-8167575cc498.png" width="350" height="300"/></p>
finger classification은 간단한 task이기때문에, 위 그래프 상 accuracy가 높지 않아도 충분히 높은 accuracy가 나오기 때문에, 가벼운 ShuffleNet을 이용하였다.

(처음에는 경량화까지 진행하는 것을 목표로 했으나, 흐지부지되어서 하지않았다..)

## > Result
object detection을 하려고 했으나, 앞서 선택한 모델을 연계해서 detection을 수행하기 어려워, 우선 정해진 네모 박스안에서 classification을 수행하는 정도로 진행하였다. 

추후에 yolo나 다른 object detection 툴을 사용하여 object detection까지 완성할 수 있도록 하겠다.

<p align="center"><img src="https://user-images.githubusercontent.com/68634729/168016330-a79a6e94-085e-4fc4-ab5a-9780a8ddd15a.gif" width="400" height="300"/></p>


