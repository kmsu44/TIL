---
date: 2024-04-08
category: JS
tags:
---
### 변수 선언 방식
var, let, const는 JS의 변수 선언 방식이다.


| 구분      | 중복 선언 | scope    | 재할당 | 호이스팅 | 초기화         |
| ------- | ----- | -------- | --- | ---- | ----------- |
| `var`   | O     | function | O   | O    | `undefined` |
| `let`   | X     | block    | O   | O    | X           |
| `const` | X     | block    | X   | O    | X           |
>[!tip] TDZ(Temporal Dead Zone)
> 스코프의 시작지점부터 초기화 시작지점까지 변수를 참조할 수 없는 구간

