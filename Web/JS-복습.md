## 자바스크립트 복습

<br>

### 1) 호이스팅

-자바스크립트가 동작이 될 때 우리가 쓰는 객체를 메모리에 등록을 하는 것. 메모리에 들어가는 것이라 변수명이나 함수명이 겹치면 error나 오류가 생길 수 있다.

-이런 호이스팅 때문에 var(전역)를 지양하려고 한다.
-var은 코드를 실행하기 전에 한번 훝으면서 var을 메모리에 다 올려버린다.
-let, const(수정X)는 지역을 탄다.

### 2) 문법 복습

* window.innerWidth : 현재 창의 너비

* [Template_literals](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Template_literals)

* [object literal](https://velog.io/@janghyoin/Replacing-switch-statements-with-Object-literals)

#### < CharAt >

#### [< indexOf >](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)

#### < slice >
```.slice(0,100)```

<br>

### 3) 알아두면 좋을 자바스크립트 문법

### 1. Static 메소드 문법

class 의 메소드(함수) 앞에 static -> 인스턴스를 만들지 않아도 해당 메소드를 쓸 수 있게 해줌.

```js
class Dog {
    static bark(){ 
        console.log("나는 짖고 있다. 멍멍!")
    }
}

Dog.bark()  // "나는 짖고 있다. 멍멍!"
```
* async를 붙일 때
```js
class Dog {
    static async bark(){} // 올바른 순서
}
```

### 2. import-export vs require-module.exports

* node는 디폴트 -> require-exports
* import-export 문법을 사용하는 방법
    * package.json 에 “type”: “module” 항목을 추가

### 3. Babel

* import-export 등의 문법으로 쓰여진 파일을 바로 node로 실행하는 방법

1. 패키지 다운<br>
```yarn add -D @babel/core @babel/cli @babel/node ```

2. babel.config.json 파일 생성<br>
```js
{
  "presets": [
    [
      "@babel/preset-env",
      {
        "targets": {
          "node": "current"
        }
      }
    ]
  ],
  "plugins": ["@babel/plugin-transform-runtime"]
}
```

3. 터미널 실행<br>
```babel-node index.js```

### 4. dotenv (.env)
자바스크립트에서 환경변수를 이용할 수 있게 해준다.

1. 설치<br>
```yarn add dotenv```

2. .env 파일 생성
```js
MY_SECRET_KEY=abcde123
```

3. 환경변수 사용
```js
const myKey = process.env.MY_SECRET_KEY
```