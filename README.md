# Yolo_v5
### YOLO 셋팅 방법 가이드 ( YOLO v5 ) 
###### YoLo는 버전별로 상이 - 버전별 성능 비교 (https://learnopencv.com/performance-comparison-of-yolo-models/)

##### 환경 셋팅을 위한 사전에 맞춰야하는 버전 - **YOLO v5 기준 : 최소 Python ≥ 3.8 and PyTorch≥1.7**
##### Yolo 셋팅 전에 선택한 사양에 맞춰서 CPU or GPU에서 각각 사전 작업 필요 - 아래 내용 참고

-----------------------
### CPU 사전 작업

###### (가상환경 생성) !conda create -n yolov5 python=3.8 --y 

###### (생성한 가상환경 커널 추가) !python -m ipykernel install --user --name yolov5 --display-name "yolov5” 
![yolo_v5](https://user-images.githubusercontent.com/102745119/211443404-d778e65c-7489-498c-8472-687695df95d9.png)


###### (커널을 yolov5으로 변경하여 선택 후 pytorch 설치) !conda install pytorch==1.7.1 -c pytorch 
-----------------------
### GPU 사전 작업

###### (가상환경 생성) !conda create -n yolov5 python=3.8 --y 

###### (생성한 가상환경 커널 추가) !python -m ipykernel install --user --name yolov5 --display-name "yolov5” 
![yolo_v5](https://user-images.githubusercontent.com/102745119/211443404-d778e65c-7489-498c-8472-687695df95d9.png)

###### (커널을 yolov5으로 변경하여 선택 후 pytorch, CUDA 관련 패키지 설치) CUDA 11.0

###### !conda install pytorch==1.7.1 torchvision==0.8.2 torchaudio==0.7.2 cudatoolkit=11.0 -c pytorch --y

###### *(PyTorch설치관련 내용은 yolov5/requirements.txt에 포함되어있으므로 따로 설치 안해도 되긴함, 다만 특정 버전으로 설치시에 따로 설치)

-----------------------
# 1. YOLO

!git clone [https://github.com/ultralytics/yolov5.git](https://github.com/ultralytics/yolov5.git)

*경연의 워크스페이스 jupyterLab에서는 권한 에러 발생으로 

로컬에서 git clone 받은 후 압축하여 압축파일을 jupyterLab에 올려서 

압축 풀고 사용 - 압축풀기 명령어:  !unzip 파일명.zip

(경로는 어디든지 상관 없으나, /home/work/ 경로에 맞춰서 가이드)

# 2. YOLO 필수 모듈 설치

!pip install -r /home/work/yolov5/requirements.txt

# 3. YOLO v5 를 활용한 예시

[YOLO v5  활용 예시 : 마스크 - 착용 여부 확인](https://www.notion.so/)

-----------------------

## 부록
###### model 폴더 안에 yolov5l.yaml , yolov5m.yaml, yolov5s.yaml, yolov5x.yaml 파일들이 존재
###### yolov5는 yolov5s, yolov5m, yolov5l, yolov5x의 4가지 버전이 있는데, yolov5s가 가장 가벼운 모델이고 yolov5x가 가장 무거운 모델이다.
###### 따라서 yolov5s가 성능이 가장 낮지만 FPS(초당 프레임 수)가 가장 높고
###### yolov5x가 성능이 가장 높지만 FPS가 가장 낮다.

![Yolo_v5_image](https://user-images.githubusercontent.com/102745119/211443987-9af72bab-cb80-4872-84e6-90fad156056d.png)

###### *Object Detection의 성능 지표중 하나인 FPS:
###### 영상에서 초당 frame이 많을 수록 움직임이 더 자연스럽다.
###### Object Detection에서 FPS라는건 초당 detection(탐지)하는 비율을 의미
###### 따라서 Object Detection의 성능 측정할때는 정확도가 중요하지만 속도도 중요하다.
