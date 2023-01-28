# **뉴스기사 3줄 요약하기**


---
### 📝 **기본 지식**
> 바이너리 파일을 문자열로 변경 - base64 <br>
> 문자열 다루기 - textwrap, re <br>
> 단어 개수 구하기 - collections.Counter <br>
> 문서 요약하기 - gensim <br>
> 텍스트 파일 저장 - open, close <br>
> 프로젝트 실습

<br>

## [바이너리 파일을 문자열로 변경-base64](https://github.com/qsdcfd/Python_Project/blob/TIL/Simple_Project/Text_summary/02.%20%E1%84%87%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%82%E1%85%A5%E1%84%85%E1%85%B5%20%E1%84%91%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A1%E1%84%8B%E1%85%A7%E1%86%AF%E1%84%85%E1%85%A9%20%E1%84%87%E1%85%A7%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%20-%20base64.py)

> ### **바이너리 파일 (Binary file)** 
> <img align='left' src='img/binary_icon.png' width='50' height='50'/> <br> <br> <br>
>
> - 바이너리 파일이란 ‘0’ 과 ‘1’ 을 이용한 **2진수 데이터** 만으로만으로 인코딩된 파일
> - 사람이 직접 읽을 수 없다
> - 데이터를 효율적으로 처리, 저장, 실행 등을 목적으로 만들어진 파일
> - 장점
>    - 데이터를 처리하고 전송하는데 일반적으로 비용이 적게 든다.
>    - 텍스트 파일에 비해서 데이터 처리 속도가 빠르다.
>    - 데이터 저장 공간도 적게 듦
> - 대표적인 확장자 : exe, dll, zip, rar, mp3, mpg, jpg, png 등

<br>

> ### **Base64 인코딩**
> - 다양한 통신채널 (HTML, 이메일 등) 을 통해 **바이너리 데이터**를 **안전하게 전송**할 수 있게 하는 방법
> - ASCII, Unicode 인코딩과 함께 실생활에서도 많이 사용되는 인코딩 방법
> - ASCII (8bit) 인코딩은 프로토콜,시스템마다 다르게 해석되어 데이터가 왜곡될 여지가 있기 때문에 적합하지 않음
> - XML이나 HTTP 프로토콜에서도 특수문자 파싱 문제를 해결할 수 있는 수단
> - 64 진법은 ASCII문자들을 모두 표현할 수 있는 가장 작은 진법
>    - `문자열 입력` -> `ASCII/Binary (8bit)` -> `6bit cut` -> `base64`
> - [Base64 인코딩 테이블](https://en.wikipedia.org/wiki/Base64)
> <img src='img/base64_example.png' width='600' height='600'/>

<br>

## [문자열 다루기](https://github.com/qsdcfd/Python_Project/tree/TIL/Simple_Project/Text_summary)

### textwrap

> - 파이썬에서 **문자열을 보기 좋은 형태**로 정렬 또는 줄바꿈하는데 사용할 수 있는 라이브러리입니다.
> - 원하는 길이에 맞게 줄이기 : textwrap.shorten()
> - 긴 문장 자르기 : textwrap.wrap()
> - 긴 문장 줄바꿈 : textwrap.fill()
> - [샘플 기사](https://www.codingworldnews.com/news/articleView.html?idxno=12116)

### re

> - **정규표현식(regular expressions)**은 복잡한 문자열을 처리할 때 사용하는 기법으로, 파이썬뿐 아니라 C, 자바, 심지어 문서 작성 프로그램 등 문자열을 처리해야 하는 다양한 곳에서 활용중
> - 특정 문자열 `추출`, `변환` 등에 사용
> - [공식문서](https://docs.python.org/3/library/re.html)

<br>

## [단어 개수 구하기](https://github.com/qsdcfd/Python_Project/blob/TIL/Simple_Project/Text_summary/04.%20%E1%84%83%E1%85%A1%E1%86%AB%E1%84%8B%E1%85%A5%20%E1%84%80%E1%85%A2%E1%84%89%E1%85%AE%20%E1%84%80%E1%85%AE%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20-%20collections.Counter.py)

### collections.Counter

> collections.Counter는 리스트나 문자열과 같은 자료형의 요소 중 **값이 같은 요소가 몇 개인지를 확인**할 때 사용
