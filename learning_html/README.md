
## 1. vsc extension
- Community Material Theme
- Material Icon Theme

<br><br>

## 2. Tag Attribute

### 1) \<a \/\>
- target 어트리뷰트 기본값은 self
- target=_blank를 설정하면 다른 탭에서 링크가 열림

```HTML
<a href="http://google.com" target="_self>
```

<br><br>

## 3. HTML Structure
### 1) \<head\> 
 - 웹사이트의 환경을 설정함 
 - 페이지에 관한 환경 설정

### 2) \<body\> 
- 사용자가 볼 수 있는 content
- [home.html](./home.html) 참고

```HTML
<!DOCTYPE html>
<html lang="kr">

<head>
</head>

<body>
</body>

</html>
```

html 태그에 lang 어트리뷰트를 넣는 이유는 google,naver와 같은 검색 엔진에 도움을 주기 위함. 우리 사이트에서 어떤 언어가 사용되고 있는지 알려줌. 주된 언어가 한국어인지 영어인지 검색엔진에게 알려주는 것임

<br><br>

## 4. Its All About the Head
- 구글에서 검색했을 때 나오는 결과는 웹 사이트의 \<title\>과 \<meta name="description"\>의 내용을 가져옴

<br>

### 1) \<meta\>
- 부가적인 정보
- 어트리뷰트로 content와 name을 가지고 있음

### 2) \<meta charset="utf-8">
- 브라우저에게 텍스트를 어떻게 그려달라고 말해줌
- 한글이나 다른 특수문자가 있는 언어를 입력할 때 브라우저가 이해할 수 있게 도와 줌.
- 이 메타태그가 없으면 브라우저가 이해하지 못하는 언어는 깨져보이게 됨

### 3) \<link\>
- 브라우저 탭에 뜨는 아이콘 이미지

```HTML
    <link rel="shortcut icon" sizes="16x16 32x32 64x64" href="https://nomadcoders.co/m.png"/>

``` 

<br>

### 4) \<meta property="og:image"\>
- open graph 태그 / og 태그 
- 링크의 미리보기, 제목, 이미지를 결정하는 태그
- 카카오톡 공유하기 시에도 확인할 수 있음
- 카카오톡의 경우 먼저 **og:title** 태그를 찾고 \<meta property="og:title"\>   
-> description을 찾은 후 \<meta name="description"\>   
-> og:image를 본다 \<meta property="og:image"\>

<br><br>

## 5. More tags

- 구글에서 html 태그 검색 시 ['mdn'](https://developer.mozilla.org/ko/docs/Web/HTML/Element) 을 붙여서 검색해라
- w3 schools 사이트는 사용하지 마라
- 태그는 암기하려고 하지 말고 검색하면 됨

<br><br>

## 6. Form tags
- [form.html](./form.html) 참고

### 1) \<label\>
- \<label\> 은 \<input\> 태그와 같이 있어야 작용함
- input 태그의 ID를 label 태그의 for 어트리뷰트 값으로 넣어주면 됨

```HTML
<label for="profile">Profile Photos</label>
<input id="profile" type="file" accept="images/*" />

```



