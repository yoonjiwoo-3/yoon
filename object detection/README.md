### object detection

## 스타터


# 1-1. Training과 Test 데이터의 이미지 수

- Training: 9023장  
- Test: 3008장


# 1-2
xml 형태의 라벨링 데이터를 읽는 코드작성 및 내용 분석
총 몇 종류의 object가 있는가?-  각 object 종류별로 training 영상과 test 영상이 각각 몇 개씩 있는가?※ 단, object 종류 중 “other objects”는 삭제


![1-2](https://github.com/yoonjiwoo-3/yoon/blob/main/object%20detection/1-2.png)


# 1-3
 xml 파일에서 제공되는 바운딩 박스 메타데이터 (<bndbox>)를 이용하여 대응되는 영상에 바운딩 박스를 plot(각 object 종류별로 한 개의 샘플 영상을 시각화, 바운딩 박스의 테두리 색상은 object 종류에 따라 다른 색상을 사용)

![1-3](https://github.com/yoonjiwoo-3/yoon/blob/main/object%20detection/1-3.png)


# 2-1
Object detection(객체인식) 모델을 학습하기 위해 영상 데이터와 메타데이터를 
Google colab으로 업로드하여야 한다. 이와 관련하여 다음의 질문에 답.
개별 파일로 존재하는 영상 데이터와 메타 데이터를 어떠한 방식으로 업로드 ? 
영상 데이터와 메타 데이터를 Colab 환경에서 어떠한 구조로 저장하였는가?  
해당 구조를 선택한 이유?


트레이닝 폴더와 테스트 폴더를 따로 만들어 각각 이미지와 라벨 폴더를 옮겨 놓은 뒤 폴더 두가지를 구글 코랩에 업로드했다. Colab 환경에서는 Google Drive를 마운트하여 데이터 저장소로 사용하였으며, 이미지데이터와 라벨데이터를 아래와 같은 디렉토리 구조로 구분하여 저장.

![2-1](https://github.com/yoonjiwoo-3/yoon/blob/main/object%20detection/2-1.png)

데이터셋은 아래 공유링크 참고

Test: <https://drive.google.com/drive/folders/1vs7G8HHdmMjJZvC6XX_eVrevkOADEDc3?usp=drive_link>

Training: <https://drive.google.com/drive/folders/1raEi5n7z8Uv4fLAhfssg1CVl0qpFxkGA?usp=drive_link>

# 3-1
해양 침적 쓰레기 검출을 위하여 사용 가능한 알고리즘/모델에는 어떠한 것들이 
있는가? 최소 3가지 이상의 알고리즘/모델을 탐색하고 그 중 한 가지를 선택.
선택한 이유에 대해서 설명.


Yolo, Faster R-CNN, SSD(Single Shot MultiBox Detector)
Yolo 선택/ 고도로 일반화되어 예상치 못한 입력을 받아도 R-CNN보다 훨씬 탁월한 성능을 보이며,이미지전체를 보기에 클래스에 대한 맥락적인 정보와 모양을 암시적으로 인코딩함으로써 Fast R-CNN과 같은 알고리즘과 다르게 배경을 객체로 잘못 예측하는 실수를 하지 않음.



# 3-2
선택한 알고리즘/모델을 구현/실행하여 mAP@IoU 50% (50% 이상 중첩되었을 
경우의 mean Average Precision)을 계산.

yolo로 구현하지 못하고 mlp로 바꿔서 구현한 결과

**mAP@IoU 50%: 0.3858**


# 3-3
모델이 잘못 분류한 영상/객체에 대해서 분석하고, 해당 문제의 발생 이유를 설명.

예측을 제대로 하지 못함








