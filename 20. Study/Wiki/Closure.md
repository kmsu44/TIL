---
date: 2024-04-09
category: 
tags:
---
### 클로저란?
함수가 선언될 때의 렉시컬 환경과의 조합을 말한다.
==함수가 속한 렉시컬 스코프를 기억하여, 함수가 렉시컬 스코프 밖에서 실행될 때에도 이 스코프에 접근할 수 있게 해준다.==
예시

```js
function makeCounter() {
    let count = 0; // `makeCounter`의 렉시컬 스코프에 있는 `count` 변수

    return function() {
        return count++; // 클로저를 통해 `count`에 접근
    };
}

let counter = makeCounter();
console.log(counter()); // 0
console.log(counter()); // 1
console.log(counter()); // 2
```

### 클로저의 활용
#### 정보 은닉
특정 데이터에 대한 접근을 제어하고 싶을 때
#### 커링
인자의 수를 주령서 한 번에 하나의 인자만 받도록 만들 수 있다.
```js
function multiply(a) {
    return function(b) {
        return a * b;
    };
}

// 커링 함수 사용
const multiplyByTwo = multiply(2);
console.log(multiplyByTwo(5)); // 10
console.log(multiplyByTwo(10)); // 20

const multiplyByThree = multiply(3);
console.log(multiplyByThree(5)); // 15
console.log(multiplyByThree(10)); // 30


function add(a) {
    return function(b) {
        return function(c) {
            return a + b + c;
        };
    };
}

// 커링 함수 사용
const addOne = add(1);
const addOneAndTwo = addOne(2);
console.log(addOneAndTwo(3)); // 6

```
부분 적용함
