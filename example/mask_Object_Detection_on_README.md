# Yolov5 학습을 위한 Data 폴더 셋팅

### 1. yolov5_mask 라는 폴더 생성
### 2. 폴더 안에 image 폴더와 labels 폴더를 생성하여 그 안에 train, valid폴더를 생성한다.
###### (보통 LabelImg를 써서 데이터 라벨링하기때문에 txt파일과 이미지파일을 분리해준다.)

![yolo_mask_valid](https://user-images.githubusercontent.com/102745119/211463867-1483788c-a64f-41ef-b0a5-9d9ddf0c377e.png)
![yolo_mask_train](https://user-images.githubusercontent.com/102745119/211463871-61aed248-9b7a-487e-bd63-f807f3aa6a89.png)

###### *예제는 이미 데이터 라벨링되어있는 샘플 자료를 가져왔음

### 3. yaml 파일 생성

### 3-1. dataset.yaml 생성

###### yolov5 폴더의 data 폴더 안에 coco128.yaml 이라는 파일이 있는데,

###### 이와 비슷하게 커스텀 data용 yaml 파일을 만들어준다.

###### yaml 파일 안에는 training data 경로, validation data 경로, 탐지할 class 개수, class 이름 리스트가 들어간다.
-----------------------
![yaml_yolo](https://user-images.githubusercontent.com/102745119/211463903-b108ceaf-323a-48ea-960a-c6f9bdb8e183.png)
