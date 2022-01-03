# CSS

## 1) HTML에 CSS를 추가하는 방법

### (1) css 파일 분리

- css 파일을 별도로 만들고, html의 head 부분에 link 태그를 이용하여 불러온다.

```HTML
 <link href="styles.css" rel="stylesheet"/>
```

### (2) 인라인 css

- \<style\> 태그 안에 css를 직접 작성한다.

<br><br>

## 2) Cascading

CSS는 cascading 즉, 위에서부터 아래로 차례로 적용된다. 결국 맨 마지막에 있는 코드가 가장 마지막에 적용된다.

<br><br>

## 2) Blocks & Inline

- div와 같은 Box 속성들은 옆에 아무것도 오지 않는다. (div, header, main, section, footer, article)
- span 태그는 바로 옆에 다른 요소가 올 수 있다.
- 옆에 다른 요소가 못 오는 걸 **block**이라고 부르고, 다른 요소가 올 수 있는 것을 **inline**이라고 부른다.
- block이 아닌 요소는 span, a, img 등이 있다.
- 코드: [02.blacks_and_inline.html](02.blocks_and_inlines.html)
