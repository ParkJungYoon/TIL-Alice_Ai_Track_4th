## 자바스크립트 최신 문법
[지난 정리](./2주차-4.md)


### 1. var -> const & let

* let: 선언과 변경이 자유로운 변수
* const: 한 번 선언하면 값을 바꿀 수 없는 상수. 같은 스코프 내에서 중복된 이름 가질 수 없다.

<br>

### 2. Array 메소드

#### < forEach >
```Array.forEach()``` <br>
: 배열의 요소를 이용해 순차적으로 함수를 실행하는 메서드(method). <br>
: 함수 내에서 따로 return을 할 필요가 없다.

#### < map >
```Array.map()``` <br>
: 배열의 요소를 이용해 순차적으로 함수를 실행하여 새로운 배열을 반환하는 메서드. <br>
: 함수 내에서 반드시 새로운 값을 return

#### < filter >
```Array.filter()``` <br>
: 배열의 요소를 이용해 순차적으로 함수를 실행하여 조건을 통과하는 요소를 모아
새로운 배열로 반환하는 메서드.

<br>

### 3. Arrow function
function 표현보다 구문이 짧은 함수 표현

<br>

### 4. Destructuring assignment
구조 분해 할당: 객체나 배열을 해체하여 개별 변수에 담을 수 있게 하는 표현식

#### < Object >
```js
const a = {i: 1, j: 2, k: 3};
const { i, j, k } = a;
```

#### < Array >
```js
const a = [1, 2, 3];
const [a0, a1, a2] = a;
```

<br>

### 5. Shorthand property names
새로 선언하는 object에 key값과 동일한 변수명을 가진 변수를 할당할 경우 value 값을 생략해서
적을 수 있다.
```js
// 과거
var eat = { apple:apple, banana:banana };
// 현재
const eat = { apple, banana };
```

<br>

### 6. Spread Syntax

#### < Object >
두 객체를 합성할 때 겹치는 key가 있을 경우 나중에 오는 값이 들어간다.

#### < Array >
```js
const list = [1, 2, 3];

const newList = [0, ...list, 4,5];
```

<br>

### 7. Template literals
표현식을 허용하는 문자열 리터럴

<br>

### 8. Optional chaining
객체나 변수에
연결된 다른 속성 참조할 때 유효한 속성인 지
검사하지 않고 값을 읽을 수 있도록 해준다.

```array?.[index]```