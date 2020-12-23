# gitignore

> git으로 관리하지 않을 파일 / 폴더를 관리

* `.gitignore` 파일을 생성하여 아래와 같이 작성한다.
  * 메모장에서 편집은 절대 금지!

```bash
data.csv 		# 특정 파일
secret/			# 특정 폴더
*.png 			# 특정 확장자
!profile.png	# 예외 처리 ( 즉 , 이번 profile.png는 포함 시킨다는 것)
```

* OS (Windows / Mac), 개발환경 (IDE / Text editor), 특정 언어에서 발생하는 파일 / 폴더들
  * https://gitignore.io
    * 예) 자바로 Eclipse을 활용하여 윈도우에서 개발하고 있다.
      * ![gitignore_ex](md-images/gitignore_ex.PNG)
      * 이렇게 검색을 하면 예외해야되는 부분들이 나옴