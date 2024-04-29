---
date: 2024-04-04
category: JS
tags:
---
## 얕은 복사 vs 깊은 복사
객체를 프로퍼티 값으로 갖는 객체의 경우 얕은 복사는 한 단계 까지만 복사하는 것을 말하고, 깊은 복사는 객체에 중첩되어 있는 객체까지 모두 복사하는 것을 말한다.

```js
const o = {x: {y:1}};

// 얕은 복사
const c1 = {...o};
console.log(c1 == o); // false
console.log(c1.x === o.x); // true

//깊은 복사
coonst _ = require('lodash')
const c2 = _.cloneDeep(o)
console.log(c2 ===o) // false
console.log(c2.x === o.x) // false
```
