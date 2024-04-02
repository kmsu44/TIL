---
date: 2024-03-28
category: 
tags:
---
## JSX
### JavaScript에 마크업 넣기
웹이 인러랙티브해지면서 로직이 컨텐츠를 결정하는 경우가 많아져, js가 html을 담당하게 되었다. 따라서 react에서 렌더링 로직과 마크업이 함께 있는 이유다.

### 단일 루트 엘리먼트를 반환 해야함
`JSX`는 내부적으로 `JavaScript` 객체로 변환 되기 때문에 하나의 배열로 감싸지 않은 하나의 함수 에서는 두 개의 객체를 반환할 수 없기 때문에 다른 태그나 `Fragment`로 감싸야한다.
### 모든 태그를 닫아야함
`JSX`에서는 태그를 명시적으로 닫아야 함
### 거의 대부분이 camelCase
`JSX`는 `JavaSciprt`로 바귀고, `JavaScript`에서는 변수명에 제한이 있기 때문에 `class`와 같은 예약어를 사용할 수 없다.

> [!example]
`stroke-width` -> `strokeWidth`

> [!note]
<></>여기에 key이런거 추가할려면 `<Fragment></Fragment>`