# 참고 - 기존 파일 삭제
문제 - 구글 드라이브 파일을 다음 코드를 통해 연동시켜서 진행하려고 했으나 인식이 되지 않음.
from google.colab import drive
drive.mount('/content/drive', force_remount=True) 

![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/7be165d6-e790-467a-b3ab-23ea49bd5f8a)
위에서 파일들은 인식하지만
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/c6979407-2f6b-4da6-95a6-2cae87c440db)
여기에서는 찾지 못함

우선 시간 내 제출해야 해서 이 상태로 제출하지만, 오늘 계속 코드 수정하겠습니다

# 공부
## 1. 비교 (참고 https://junstar92.tistory.com/151)

데이터 비교 
과제 - https://www.kaggle.com/datasets/sadhliroomyprime/motorcycle-night-ride-semantic-segmentation
원본 데이터, __fuse, __save 
→ ⓐ __fuse 파일이랑 __save 파일은 왜 따로 있는거지???
→ ⓑ 초기에 fuse 파일만 masking된 파일로 사용하려고 별도의 폴더로 파일을 분리해서 사용하려하는 과정에서 시간 많이 소모
→ ⓒ 그러나 구글 드라이브와 연결 시 왜 인식을 못했는지는 아직도 잘 모르겠음
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/8253c10e-15a8-4ff8-ae60-6a3483f4057b)
데이터 내용 전혀 안읽었고 무지성 검색했었음;;


블로그 - https://academictorrents.com/details/b18bbd9ba03d50b0f7f479acc9f4228a408cecc1
print(dataset.keys())
-> dict_keys(['train', 'test']): 딕셔너리 형태의 데이터
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/049211d5-539d-4253-b959-a620ddf20751)

# 현재 파일 문제
실행이 안됨 (리소스)
--------------------------------------------
저녁
10번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/483faf15-03a7-4d5f-b81d-0eae617594ea)
40번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/c7170967-0ab3-40e6-ba34-18ee5ddae4e2)
70번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/21b6d123-fc75-47d6-bc21-3822cd8b9a0c)

이후 초기화하고, loss 함수 변경 (이전에는 'categorical_crossentropy')
https://blog.naver.com/PostView.nhn?blogId=siniphia&logNo=221972407157 참고
30번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/8ec00d99-b79a-41ce-bafa-c4547b136fe8)
60번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/1ae411ef-05b0-4e6a-8106-a8715d91a782)
90번 에포크 
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/0bf6c0fe-17fd-424b-8fc0-0a7636a667a0)

이후 batch_size 16에서 (24로 변경하려다 안돌아가서) 20으로 변경
+30번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/9b0be408-c744-4c39-9586-c3200846a22f)
+30번 에포크
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/2a318b64-f4ed-4903-9fe7-b7d2cf2b561f)

Tensorboard
![image](https://github.com/Garlic-Ryu/Main_RS/assets/112372749/e3114a63-eb15-47b7-802a-a704d6d38d5f)


언젠간 읽어보기
"Semantic Segmentation with Transfer Learning for Off-Road Autonomous Driving"


