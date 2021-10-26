# 타입스크립트란?

- 타입스크립트는 타입을 추가해서 자바스크립트를 확장시킵니다.
- 자바스크립트를 이해함으로써 코드를 실행하기 전에 에러를 잡고 고치는 시간을 절약해줍니다.
- 자바스크립트에 있는 기능을 더 강화시킵니다.
- 순수한(Plain) 자바스크립트(노드나 브라우저 환경에서 이해할 수 있는 자바스크립트)로 컴파일 해줍니다.
- 타입스크립트는 'Programming Language 언어' 입니다.
- 타입스크립트는 'Compiled Language' 입니다.
- 전통적인 Compiled Language와는 다른 점이 많습니다.
- 그래서 'Transpile' 이라는 용어를 사용하기도 합니다.
- 자바스크립트는 'Interpreted Language' 입니다.

<br>
<br>
<br>

Compiled | Interpreted
--|--
컴파일이 필요 o | 컴파일이 필요 x
컴파일러가 필요 o | 컴파일러가 필요 x
컴파일하는 시점 o => 컴파일 타임 | 컴파일하는 시점 x
컴파일된 결과물을 실행 | 코드 자체를 실행
컴파일된 결과물을 실행하는 시점 | 코드를 실행하는 시점 => 런타임

<br>
<br>

<h3>타입스크립트로 코딩한 내용은 브라우저나 노드 환경에서 바로 읽어서 사용할 수는 없습니다.    
따라서 읽어서 사용할 수 있는 형태의 Plain JavaScript 라고 하고   
변환해 주는 역할을 하는 것이 TypeScript Complier라고 하는 프로그램입니다.   </h3>
<br>
<br><br>
$npm install typescript -g (글로벌) 추천 x<br>
$npm init<br>
$npm install typescript : 프로젝트 폴더에 따로 설치하자.<br>
<br>
//글로벌로 설치하면 그냥 tsc 명령어를 사용하면 되는데 프로젝트 폴더 안에 설치했기 때문에 tsc 실행 파일이 들어있는 node_modules/.bin/tsc 까지 써주고 명령어를 사용해야 하는데 npx로 명령을 실행하면 생략이 가능하다. 그러므로 글로벌로 설치했다면 npx가 붙어있는 명령어는 빼면 된다.<br>
<br>
$npx tsc test.ts : test.ts => test.js 변환<br>
$npx tsc --init : 타입스크립트 설정이 담겨있는 tsconfig.json 파일 생성<br>
$npx tsc : 프로젝트에 담겨있는 모든 ts파일 컴파일 (tsconfig.json 파일 필요)<br>
$npx tsc -w :ts파일이 생기면 자동으로 js 파일로 컴파일 (항상 실행중이어야 함) <br>
<br>

```js
"scripts": {
    "build":"tsc"
  },
```

package.json 파일의 스크립트 부분에 tsc를 지정해놓으면 node_modules/.bin/tsc 로 하지않고<br>
npm run build 명령어로 바로 tsc 명령어를 사용할 수 있다.<br>