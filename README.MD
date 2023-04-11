# Hash tag generate with bert model
```
음성데이터와 이미지 데이터로부터 해시태그를 뽑아내는 프로젝트입니다.
```
<img width="983" alt="스크린샷 2023-04-11 오후 2 18 09" src="https://user-images.githubusercontent.com/97833069/231063575-7c5909dd-04a2-4b8d-9891-0fe2fb8d9abe.png">

```
언어 모델로 다국어 Bert를 사용 다양한 모델들이 존재하였지만 성능이 제일 우수하여 이를 선택하였습니다.
```

<img width="991" alt="스크린샷 2023-04-11 오후 2 18 45" src="https://user-images.githubusercontent.com/97833069/231063646-b223c344-35ec-43f7-85b6-3faf81f1f5ed.png">

```
음성부분의 데이터와 이미지로부터온 데이터의 유사도를 word2vec으로 계산하여 유사도가 가장 높은 순위를 뽑았습니다.
```
<img width="990" alt="스크린샷 2023-04-11 오후 2 18 57" src="https://user-images.githubusercontent.com/97833069/231063641-037a7cb9-e84e-4e9b-8257-4a013e0c2fe3.png">
<img width="987" alt="스크린샷 2023-04-11 오후 2 19 17" src="https://user-images.githubusercontent.com/97833069/231063635-ee66a5dc-7eae-49c5-ba58-a41f9e14ae24.png">



### Archive contents
```
wanso/
├── pickle_data/
│   ├── common_tag.pickle
│   ├── dic.pickle
│   ├── hash_table.pickle
│   └── img_table.pickle
├── weights/
│   └── classification_model.pt
├── ko.bin
├── adot_clf_model.py
├── adot_tag_generate.py
└── adot_tag_run.py
```

### 설치 파일
requirements.txt
- 필요한 라이브러리 설치
```
!pip install -r requirements.txt
```
### Word2Vec 설치
```
!gdown https://drive.google.com/file/d/1-0FZyuS9gt1Avb8vY_VtCsksVL_JMTUv/view?usp=share_link
```
### gz 파일 압축해제
```
!gzip -d ko.bin
```
### 모델 weights 다운로드 weights folder에 넣어줘야한다.
```
!wget https://drive.google.com/file/d/1-XnfaC5az-1pVzixhQZkMLnSgxz7cv0e/view?usp=sharing
```
### 실행 방법
```
python3 adot_tag_run.py
```


