## 2. 고정형 웹사이트와의 차이?

### 미디어 쿼리

미디어 쿼리는 CSS3에서 소개된 CSS 기법입니다.
`@media`를 통해 선언할 수 있으며 블록 내부의 특정 조건을 만족할때 CSS속성을 적용시킵니다.

반응형 웹이 탄생할 수 있었던 배경에는 미디어 쿼리의 영향이 가장 지배적이었는데 2009년 미디어 쿼리 레벨 3이 Candidate Recommendation이 이루어지며 웹에 활발하게 사용되기 시작했습니다.
미디어 쿼리를 사용하면 여러가지 환경(특정 width보다 큰지 작은지, 특정 해상도를 넘는지 안 넘는지)을 파악하여 사용자 환경에 알맞는 CSS를 선택적으로 적용시켜 줄 수 있습니다.

다른 비율의 다양한 크기의 이미지들을 사용하고 싶다면 img요소의 srcset 속성을 사용하는것 보다 `@media` 미디어쿼리 사용이 권장되면 이는 개발자가 원하는 해상도에 맞게 출력할결과를 정확하게 명시할 수 있기 때문입니다.

**예제**

작동하는 기기가 screen media이며 최소 너비가 800px 이상일때 적용시키기
```css
@media screen and (min-width: 800px) {
  .container {
    margin: 1em 2em;
  }
}
```

400픽셀 이하 / 401픽셀 ~ 700픽셀 / 701픽셀 이상
```css
.some-image {
  width: 400px;
  height: 400px;
  background-image: url("images/heropy_small.png");   
  background-repeat: no-repeat;
  background-size: cover;
}
@media (min-width: 401px) {
  .some-image {
    background-image: url("images/heropy_medium.png");   
  }
}
@media (min-width: 701px) {
  .some-image {
    background-image: url("images/heropy_large.png");   
  }
}

```html

```

**호환성 검사**

### 사용 단위

(설명란)
반응형 타이포
rem, em
vw(뷰포트 단위)
max/min width, height

**예제**

**호환성 검사**
| ![미디어 쿼리 Can I use](images/naver_3.2.5.png) |
| :-------------------------------------------: |
|            미디어 쿼리 호환성 검사             |

위 스크린샷을 참고 시 미디어 쿼리는 전반적으로 인터넷 익스플로어 환경에서는 호환되지 않는 모습을 보이면 다른 브라우저에서는 대부분 잘 동작하는걸로 확인된다.

<details>
<summary>참고자료</summary>

</details>