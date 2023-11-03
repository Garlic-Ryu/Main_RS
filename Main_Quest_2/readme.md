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



