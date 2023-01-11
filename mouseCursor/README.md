
# Custom Mouse Cursor

## navbar에 다가가면 변화가 생기는 마우스

### mix-blend-mode  CSS 속성

https://developer.mozilla.org/ko/docs/Web/CSS/mix-blend-mode

특정 요소의 콘텐츠가 자신의 배경 및 부모와 어떻게 일치할지 증명한다

`mix-blend-mode: difference;`를 사용하여 정반대로 보이게 해주었다

```css
mix-blend-mode: normal;
mix-blend-mode: multiply;
mix-blend-mode: hard-light;
mix-blend-mode: difference;
```


### CSS will-change 속성

https://dev.opera.com/articles/ko/css-will-change-property/

값이 변경될 속성에 대한 힌트를 미리 지정해주는 것이다.

웹 어플리케이션이 진화함에 따라 opacity, transform 등의 css 속성 값이 동적으로 변화하는 상황이 갈수록 자주 생긴다

동적으로 변화하는 상황시에, will-change 속성을 이용하면 브라우저에 엘리면트의 어떤 속성이 높은 확률로 변할 것인지 알려줄 수 있다

**브라우저는 이것을 통해 앞으로 동적으로 변활할 값을 알고 더 부드러운 이벤트를 구사할 수 있다**

```css
will-change: auto; /* 기본값 */
will-change: scroll-position; /* 엘리먼트의 스크롤 위치가 바뀔 것 */
will-change: contents; /* 엘리먼트의 컨텐츠 중 일부가 바뀔 것 */

/* 혹은 특정 CSS 속성을 명시할 수 있다. */
/* transform, opacity, top, left, right, bottom가 많이 사용됨 */
will-change: transform;
will-change: left, top; /* 여러 속성을 동시에 명시할 수 있음 */

```

하지만 이러한 will change를 사용할때는 사전 준비에 비용이 든다
필요하지않은 상황에서 사용하게 될시에는 성능이 저하될 것이다.
기본적으로 css사용할때 성능의 문제가 없다면 따로 will change를 사용할 일은 없다.

참고로 will-change의 사용이 끝날시에는 다시 auto로 초기화를 시켜주는 것이 좋다.
