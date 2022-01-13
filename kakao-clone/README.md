# KAKAO-CLONE

## 1) 단축키

- vscode에서 html 파일에 !를 치면 자동으로 html document를 생성할 수 있음

<br><br>

## 2) BEM (Block Element Modifier)

좀 더 쉽게 읽히는 CSS 네이밍 방법(권장)

- **block**: 구성 요소의 가장 바깥쪽 상위 요소
- **element**: 구성 요소 안쪽에는 하나 또는 그 이상의 요소가 있을 수 있다
- **Modifier**: 블록 또는 요소는 변경자를 이용하여 변경을 표시할 수 있다.

```CSS
.block_element--modifier
```

<br>

```CSS
/* Block Component */
.btn {}

/* Element that depends upon the block */
.btn__price {}

/* Modifier that changes the style of the block */
.btn--orange {}
.btn--big {}
```

<br>

예제는 아래 코드를 참고한다.

```HTML
<a class="btn btn--big btn--orange" href="https://css-tricks.com">
    <span class="btn__price">$9.99</span>
    <span class="btn__text">Subscribe</span>
</a>
```

<br><br>

## 3) icon

- [Heroicons](https://heroicons.com/)
- [FontAwesome](https://fontawesome.com/)

FontAwesome에서 icon을 더 큰 사이즈로 사용하고 싶다면, 먼저 큰 아이콘이 지원되는지 확인해보고 아래와 같이 fa-2x처럼 작성한다.

```HTML
<i class="fas fa-battery-full fa-2x"></i>
```

<br><br>

## 4) Font

- vscode에서 font-family를 쓰면 자동으로 추천해줌
- 만약 다른 폰트를 찾고 싶다면 [google Fonts](https://fonts.google.com/)를 이용한다.
- font는 head에 link를 사용해서 추가할 수도 있지만 CSS를 사용해서 추가하는 것을 권장함
- google Fonts에서 @import 방식으로 복사해온 뒤 css 파일 상단에 붙여 넣는다.

<br><br>

## 5) css hack

- 현재 status bar에 설정한 justify-content: space-between이 element 별로 서로 다른 width로 인해 시계가 중앙으로 오지 않음
- justify-content: space-between에서 justify-content: center로 변경한 후, div.status-bar\_\_column의 width를 33%로 준 뒤, 두번째 column의 자식 요소를 중앙에 둔다.

```CSS
.status-bar {
  display: flex;
  justify-content: center;
}
.status-bar__column {
  width: 33%;
}
.status-bar__column:first-child span {
  margin-right: 5px;
}
.status-bar__column:nth-child(2) {
  display: flex;
  justify-content: center;
}
.status-bar__column:last-child {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

```

<br><br>

## 6) Reset CSS

- 대부분의 태그에 margin:0, padding:0, border:0 등을 가진 css 파일을 말함
- https://meyerweb.com/eric/tools/css/reset/
- reset.css파일을 만들고 styles.css파일 상단에서 import 시킨다

```CSS
@import "reset.css";
```
