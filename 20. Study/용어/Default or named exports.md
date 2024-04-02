---
date: 2024-03-28
category: JS
tags: 
description:
---
### Default exports
- 한 파일 내에서 하나의 `export`만 사용 가능
- 다른 파일에서 가져올 때 이름을 마음대로 가져올 수 있다.
### Named export
- 한 파일 내에서 여러개의 `export` 가능
- `import` 하는 경우에 함수명과 이름이 동일해야함 
```js
// import
import {Profile} from './Gallery.js'

// export
export function Profile(){
	//...
}
```
