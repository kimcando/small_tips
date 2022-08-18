# small_tips

### 문자열 관련
* 문자 표현 : ascii, unicode
* 인코딩 : utf-8, utf-8-sig, euc-kr -> `import chardet` 로 enc 확인 후 넣으면 됨
* [\ufeff](https://frhyme.github.io/python-basic/py_eff_byte_order_mark/) : 해당 file이 어떤 문자열로 코딩되었는지를 의미하는 일종의 식별자. utf-8은 BOM 필요 X. `encoding=utf-8-sig`
* BOM(byte order mark)


### 기본 re 관련
* 한글
  * ㄱ-힣 하면 이 사이에 있는 코드들도 같이 묶여짐 -> `[가-힣ㄱ-ㅎㅏ-ㅣ]`
* 한자
  * `[一-龥]` 로 커버 안되는 것도 존재. [추가 확인](https://stackoverflow.com/questions/2718196/find-all-chinese-text-in-a-string-using-python-and-regex)
* 영어 
  * `a-zA-Z`
* 일본어
  * `ぁ-ゔァ-ヴー々〆〤` : 마찬가지로 unicode range에 안잡히는거 있는 듯

### 패턴 파악
* kcbert cleand [kaggle](https://www.kaggle.com/datasets/junbumlee/kcbert-pretraining-corpus-korean-news-comments)
