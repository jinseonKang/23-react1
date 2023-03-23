# 202130301 강진선
# 4주차 (2023.03.23)

> 오늘은 npm start를 하고, 웹사이트에 직접 리액트를 연동했다.
> 그리고 프로젝트를 생성한 뒤 repository를 삭제했다.
> 새롭게 23-React1을 생성해서 커밋했다.

> JSX는 자바스크립트 문법을 확장시킨 것이기 때문에, 모든 자바스크립트 문법을
지원한다.

```
  const name = '소플';
  const element = <h1>안녕, {name}</h1>

  ReactDOM.render(
      element,
      document.getElementById('root')
  );
```

> 위의 코드에서 엘리먼트를 선언하는 부분의 코드처럼 HTML과 자바스크립트가 섞인
형태로 코드를 작성하면 된다.
> XML/HTML 코드를 사용하다가 중간에 자바스크립트 코드를 사용하고 싶으면
중괄호를 써서 묶어주면 된다.


# 3주차 (2023.03.16)

> 오늘은 Node.js를 설치하는 작업을 였다. git.bash를 이용하여 설치한 node.js의 버전을 확인하였다.
> 리액트는 사용자와 웹사이트의 상호작용을 돕는 인터페이스를 만들기 위한 자바스크립트 기능 모음집이다.

> Virtual DOM은 가상의 DOM이다. DOM을 뭔지 확인하기 위해  크롬 개발자 도구를 열어 콘솔 탭에서 document라고 입력하면
> 웹사이트의 정보가 모두 담겨있는 DOM 이 나온다.

### 리액트의 장점
> 1. 빠른 업데이트와 렌더링 속도
> 2. 재사용성이 높은 컴포넌트 기반 구조
> 3. 메타(구 페이스북)의 든든한 지원
> 4. 활발한 지식 공유와 커뮤니티
> 5. 리액트 네이티브를 통한 모바일 앱 개발 기능

> 화면을 업데이트하면 DOM이 수정된다는 말과 동일하다. 기존의 방식으로 화면을 업데이트 하려면 DOM을 직접 수정해야하는데,
> 리액트는 DOM을 직접 수정하는 것이 아니라 업데이트해야 할 최소한의 부분만을 찾아서 업데이트한다.
> 그리고 검색된 부분만을 업데이트하고 다시 렌더링하면서 변경된 내용을 빠르게 사용자에게 보여줄 수 있는 것이다.

> 리액트의 두 번째 장점은 컴포넌트 기반의 구조이다. 컴포넌트는 구성요소라는 뜻을 갖고 있는데, 리액트는 모든 페이지가 컴포넌트로
> 구성되어 있고, 하나의 컴포넌트는 또 다른 여러 개의 컴포넌트의 조합으로 구성될 수 있다.

> 재사용성은 다시 사용이 가능한 성질을 의미한다.

> <http://blog.naver.com/storyphoto/viewer.jsp?src=https%3A%2F%2Fblogfiles.pstatic.net%2FMjAyMjA3MjhfMjU3%2FMDAxNjU4OTk0OTQ3MDM0.lgrOn1_wxnYb1dZO0xtiLiCafvIRhnVK-01i38vctlcg.9wdWFMedLBkdIC3Nrqy4eNY_0CzRw4aPBLjsGx63xGwg.PNG.kkag8997%2F%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2022-07-28_%25EC%2598%25A4%25ED%259B%2584_12.22.55.png>

> 재사용성이 높아지면 전체 소프트웨어의 개발 기간이 단축된다.
> 그리고 유지 보수가 용이해진다.

### 리액트의 단점
> 1. 학습량이 방대하다.
> 2. 높은 상태 관리 복잡도

#### 실습 step3
```
html

  <html>
    <head>
      <title>소플의 블로그</title>
      <link rel="stylesheet" href="style.css">
    </head>
    <body>
      <h1>소플의 블로그에 오신 여러분을 환영합니다!</h1>
      
      <div id="root"></div>
      
      <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
      <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
      <script src="MyButtom.js"></script>
     </body>
   </html>
```

```
js

function MyButton(props) {
  const [isClicked, setIsClicked] = React.useState(false);
  
  return React.createElement(
  'button',
  { onClick: () => setIsClicked(true) },
  isClicked ? 'Clicked!' : 'Click here!'
  )
 }
 
 const domContainer = document.querySelector('#root');
 ReactDOM.render(React.createElement(MyButton), domContainer);
```

# 2주차 (2023.03.09)

> 오늘은 지난 수업에 이어 github 계정을 만들고 repository를 만들었다.
> respository 이름을 23-React1로 만들어 readme file을 추가하였다.
> 그 뒤 code에서 저장소 주소를 복사한 다음 교수님이 확인하실 수 있도록 주소를 공유 해드렸다.
> 테스트를 하기 위해 Visual Studio Code에서 저번주에 만든 코드를 왼쪽 바에서 Source Control 아이콘을 눌러서
> Commit을 한다음 깃허브로 연결해 보는 것을 배웠다.

> 처음에 깃허브로 연결이 되지 않아 그 이유를 찾아보니 앱 기본 연결 브라우저가 Internet Explorer로 되어 있었다.
> 그래서 Chrome으로 변경했더니 바로 연결이 가능하였다.
> 깃허브 웹페이지에서 업로드 된 파일을 확인 가능했다.
> 이제 그 날 배운 코드를 github 계정에 공개로 올려 Readme를 추가하면 교수님이 확인 가능하다.

### Gitignore

> GitHub는 불특정 다수가 이용할 수 있는 사이트이다.
> 그래서 공유에서 문제가 생긴다. Gitignore은 이 문제를 방지하기 위한 파일이다.

### 3교시

> HTML은 웹사이트의 뼈대를 구성하기 위해 사용하는 마크업 언어이다.
> 웹사이트의 뼈대를 구성하는 기본적이고 필수적 태그는
  html, head, body이다.

> 브라우저는 각 페이지별로 HTML 파일이 따로 존재하여, 페이지를 이동하게 될 경우 브라우저에서
> 해당 페이지의 HTML 파일을 받아와서 화면에 표시해 준다.
> 수많은 페이지가 존재하는 복잡한 사이트의 경우 SPA를 사용한다.

> SPA는 여러가지 복잡한 웹사이트를 하나의 페이지로 표현한다.
> 자바스크립트는 프로그래밍 언어의 한 종류이다.
> 문자열을 선언할 때는 "나 '로 묶어주면 되는데, 두 종류의 따옴표를 한 번에 섞어서 사용하면 안된다.
> Boolean 타입은 값이 true 아니면 false 두 가지로만 정해져 있는 자료이다.

> Undefined 타입은 정의가 되지 않은 것을 의미힌다.
> 변수를 선언만 하고 값을 대입하지 않으면 변수의 자료형은 undefined가 된다.
> Null 타입은 값이 정의되긴 했는데 정의된 그 값이 null인 것을 의미한다.
> 연산을 하기 위해 사용하는 것을 연산자라고 한다.
> 기본적인 연산자로 대입 연산자가 있다. 대입 연산자는 변수에 값을 대입하기 위해 사용하는 연산자이다.
> 대입 연산자는 항상 오른쪽에서 왼쪽 방향으로 흐름이 흘러가며, equal의 오른쪽에 있는 값을 equal의 왼쪽에 대입시킨다고 해석한다.
> let a = 10; 라 하여 console.log(a); 로 출력하면 결과는 10이 된다.
> 덧셈, 뺄셈, 곱셈, 나눗셈 등 연산자를 통칭하여 산술 연산자라 한다.

let a = 4;
let b = 5;

console.log(a+b); //출력결과: 9 가 된다.

> 증가 연산자와 감소 연산자는 기호로 ++와 --룰 사용한다.
>   증감 연산자를 변수의 뒤에 붙이는 방식을 postfix 방식, 변수의 앞에 붙이는 방식을 prefix방식이라고 한다.
>   관계 연산자는 변수들 사이의 관계를 비교하기 위해서 사용하기 때문에 비교 연산자 라고도 한다.

> 오늘 수업에서는 Github 가입 및, 파일 생성 하는 법과 간단한 이론을 배웠다.





# 1주차 (2023.03.02)

1. 오리엔테이션

2. Github가입