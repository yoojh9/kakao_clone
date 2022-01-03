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

## 3) Blocks & Inline

- div와 같은 Box 속성들은 옆에 아무것도 오지 않는다. (div, header, main, section, footer, article)
- span 태그는 바로 옆에 다른 요소가 올 수 있다.
- 옆에 다른 요소가 못 오는 걸 **block**이라고 부르고, 다른 요소가 올 수 있는 것을 **inline**이라고 부른다.
- block이 아닌 요소는 span, a, img 등이 있다.
- 코드: [02.blacks_and_inline.html](02.blocks_and_inlines.html)

<br>

### (1) inline -> block

display 속성에 block으로 설정한다

```CSS
span {
    display: block;
}
```

<br>

### (2) block -> inline

div의 display 속성을 inline으로 변경하면 더이상 div 영역은 보이지 않게 되는데, inline은 width와 height을 가질 수 없기 때문이다

```CSS
div {
    height: 150px;
    width: 150px;
    background-color: tomato;
    display: inline;
}
```

<br><br>

## 4) block

block은 box로 margin, padding, border를 설정할 수 있다.

- 브라우저는 기본적으로 margin과 같은 user agent stylesheet를 제공한다.
- 아래처럼 따로 margin을 설정하지 않았는데도 브라우저에서 기본적으로 marin: 8px;를 주고 있다.

```CSS
body {
    display: block;
    margin: 8px;
}
```

### (1) margin

- box의 border(경계)의 바깥에 있는 공간
- 별개로 CSS에서 아래와 같이 margin 값을 주면 CSS는 Cascading이므로 결국 margin:0 이 적용되어, 위에서 적용한 margin 값은 적용되지 않는다.

```CSS
body {
    background-color: thistle;
    margin-top: 20px;
    margin-left: 10px;
    margin-right: 5px;
    margin-bottom: 10px;
    margin: 0;
}
```

- margin 값이 1개이면 사방으로 적용이 되고, marin 값이 2개이면 (상,하), (좌,우)로 적용이 되며, margin 값이 4개이면 시계 방향과 같이 위쪽, 오른쪽, 아래쪽, 왼쪽 순으로 적용된다.

<br>

### (2) collapsing margins

<img scr="./capture.png" width="250px">
  
- 위 그림에서 CSS는 아래와 같다. 이때 사진처럼 div 태그에 상하로 적용된 margin이 20px이 있음에도 분홍색 body 태그와 div 태그는 상하 영역이 서로 붙어있다.
- 이 현상이 **collapsing margins** 현상이며 위, 아래쪽에서만 일어난다.
- collapsing margins 현상은 각 영역의 경계가 서로 같을 때 일어나고, 이 때 두 영역의 margin은 하나가 되며, 위 아래에서만 일어난다.

```
html {
    background-color: tomato;
}
body {
    background-color: thistle;
    margin: 20px 15px 40px 60px;
}

div {
    margin: 20px 15px;
    height: 150px;
    width: 150px;
    background-color: white;
}
```
