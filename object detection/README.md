### object detection

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


