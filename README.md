# 202130301 강진선

# 12주차 (2023.05.25)

> 오늘은 컴텍스트 마지막 부분인 useContext와 css에 대해 배웠다.

### useContext()

1. 함수 컴포넌트에서 컨텍스트를 쉽게 사용할 수 있게 해주는 훅
2. React.createContext() 함수 호출로 생성된 컨텍스트 객체를 인자로 받아서 현재 컨텍스트의 값을 리턴
3. 컨텍스트의 값이 변경되면 변경된 값과 함께 useContext() 훅을 사용하는 컴포넌트가 재랜더링됨

### 실습 (컨텍스트를 사용하여 테마 변경 기능 만들기)

> <img width="1440" alt="스크린샷 2023-05-25 오전 10 18 45" src="https://github.com/jinseonKang/23-react1/assets/126742685/daa9a461-5f97-4ec4-89d8-5c373be32107">
>
> <img width="1440" alt="스크린샷 2023-05-25 오전 10 18 52" src="https://github.com/jinseonKang/23-react1/assets/126742685/9b9e9b50-a598-4c32-859e-603ad024badc">

### CSS

> 1. CSS란?
>
> - Cascading Style Sheets의 약자로 스타일링을 위한 언어
> - 하나의 스타일이 여러 개의 엘리먼트에 적용될 수 있고, 하나의 엘리먼트에도 여러 개의 스타일이 적용될 수 있음
>
> 2. 선택자(selector)
>
> - 스타일을 어떤 엘리먼트에 적용할지 선택하게 해주는 것
>
> - 엘리먼트 선택자
> - - HTML 태그의 이름으로 엘리먼트를 선택
>
> - 클래스 선택자
> - - 엘리먼트의 클래스 속성으로 엘리먼트를 선택
> - - 점(.) 뒤에 클래스명을 넣어서 사용
>
> - 전체 선택자
> - - 전체 엘리먼트에 적용하기 위한 선택자
> - - 한국에서는 흔히 별표라고 부르는 Asterisk(\*) 를 사용
>
> - 그룹 선택자
> - - 여러가지 선택자를 그룹으로 묶어 하나의 스타일을 적용하기 위해 사용하는 선택자
> - - 각 선택자를 콤마(.)로 구분하여 적용
>
> - 엘리먼트의 상태와 관련된 선택자
> - - 엘리먼트의 다양한 상태에 따라 스타일을 적용하기 위한 선택자
> - - :hover, :active, :checked, :first-child, :last-child
>
> 3. CSS 문법과 선택자
>
> - 선택자와 스타일로 구성됨
> - 선택자를 먼저 쓰고 이후에 적용할 스타일을 중괄호 안에 세미콜론(;)으로 구분하여 하나씩 기술
> - 각 스타일은 CSS 속성과 값으로 이뤄진 키-값 쌍이며, CSS 속성의 이름과 값을 콜론(:)으로 구분
>
> 4. 레이아웃과 관련된 속성
>
> - 레이아웃은 화면에 엘리먼트들을 어떻게 배치할 것인지를 의미
> - display: 엘리먼트를 어떻게 표시할지 그 방법에 관한 속성
> - visibility: 엘리먼트를 화면에 보여주거나 감추기 위한 속성
> - position: 엘리먼트를 어떻게 위치시킬 것인지 정의하기 위한 속성
> - width/height: 가로/세로 길이를 정의하기 위한 속성
> - min-width/min-height: 최소 가로/세로 길이를 정의하기 위한 속성
> - max-width/max-height: 최대 가로/세로 길이를 정의하기 위한 속성
>
> 4. 플렉스박스
>
> - 기존 CSS의 레이아웃 사용의 불편한 부분을 개선하기 위해 등장
> - 플렉스 컨테이너와 플렉스 아이템으로 구성되며 컨테이너는 여러 개의 아이템을 포함
> - 컨테이너의 플렉스와 관련된 CSS 속성은 아이템들을 어떤 방향과 어떤 순서로 배치할 것인지를 정의
> - flex-direction: 아이템들이 어떤 방향으로 배치될 것인지를 지정하기 위한 속성
> - - main axis: flex-direction으로 지정된 방향으로 향하는 축
> - - cross axis: main axis를 가로지르는 방향으로 향하는 축
>
> - aling-items
> - - 컨테이너 내에서 아이템을 어떻게 정렬할 것인지를 결정하기 위한 속성
> - - cross axis를 기준으로 함
>
> - justify-content
> - - 컨테이너 내에서 아이템들을 어떻게 나란히 맞출 것인지를 결정하기 위한 속성
> - - main axis를 기준으로 함
>
> 5. 폰트와 관련된 속성
>
> - font-family
> - - 어떤 글꼴을 사용할 것인지를 결정하는 속성
> - - 지정한 글꼴을 찾지 못했을 경우를 대비해서 사용할 글꼴을 순서대로 지정해 줘야 함
>
> - font-size: 글꼴의 크기와 관련된 속성
> - font-weight: 글꼴의 두께와 관련된 속성
> - font-style: 글꼴의 스타일을 지정하기 위한 속성

> 6. 많이 사용하는 기타 속성
>
> - background-color: 엘리먼트의 배경색을 지정하기 위한 속성
> - border: 엘리먼트에 테두리를 넣기 위한 속성

### style-components

> 1. CSS 문법을 그대로 사용하면서 결과물을 스타일링된 컴포넌트 형태로 만들어주는 오픈소스 라이브러리
> 2. 컴포넌트 개념을 사용하기 때문에 리액트와 궁합이 잘 맞음
> 3. 태그드 템플릿 리터럴을 사용하여 구성 요소의 스타일을 지정

# 11주차 (2023.05.18)

> 오늘은 리액트 컴포넌트들을 어떻게 합쳐서 사용해야 하는지에 대해서 알아보았다. 그리고 리액트 컴포넌트 사이에 데이터 전달을 효율적으로 할 수 있게 해주는 컨텍스트에 대해서 베웠다.

### 합성이란?

> 1. 여러 개의 컴포넌트를 합쳐서 새로운 컴포넌트를 만드는 것
> 2. 다양하고 복잡한 컴포넌트를 효율적으로 개발할 수 있음

### 합성 기법

> 1. Containment
>
> - 하위 컴포넌트를 포함하는 형태의 합성 방법
> - 리액트 컴포넌트의 props에 기본적으로 들어있는 children 속성을 사용
> - 여러 개의 children 집합이 필요한 경우 별도로 props를 각각 정의해서 사용

> 2. Specialization
>
> - 범용적인 개념을 구별되게 구체화하는 것
> - 범용적으로 쓸 수 있는 컴포넌트를 만들어 놓고 이를 구체화시켜서 컴포넌트를 사용하는 합성 방법

> 3. Containment와 Specializtion을 함께 사용하기
>
> - props.children을 통해 하위 컴포넌트를 포함시키기(Containment)
> - 별도의 props를 선언하여 구체화시키기(Specialization)

### 상속

> 1. 다른 컴포넌트로부터 상속받아서 새로운 컴포넌트를 만드는 것
> 2. 상속을 사용하여 컴포넌트를 만드는 것을 추천할 만한 사용 사례를 찾지 못함
> 3. 리액트에서는 상속이라는 방법을 사용하는 것보다는 합성을 사용하는 것이 더 좋음

### 실습 (Card 컴포넌트 만들기)

> <img width="1440" alt="스크린샷 2023-05-18 오전 11 09 22" src="https://github.com/jinseonKang/23-react1/assets/126742685/dcb70d7d-96c0-4075-b22c-2b43394daaad">

### 컨텍스트란?

> 1. 컴포넌트들 사이에서 데이터를 props를 통해 전달하는 것이 아닌 컴포넌트 트리를 통해 곧바로 데이터를 전달하는 방식
> 2. 어떤 컴포넌트든지 컨텍스트에 있는 데이터에 쉽게 접근할 수 있음

### 언제 컨텍스트를 사용해야 할까?

> 1. 여러 컴포넌트에서 계속해서 접근이 일어날 수 있는 데이터들이 있는 경우
> 2. Privider의 모든 하위 컴포넌트가 얼마나 깊이 위치해 있는지 관계없이 컨텍스트의 데이터를 읽을 수 있음

### 컨텍스트 사용 전 고려할 점

> 1. 컴포넌트와 컨텍스트가 연동되면 재사용성이 떨어짐
> 2. 다른 레벨의 많은 컴포넌트가 데이터를 필요로 하는 경우가 아니라면, 기존 방식대로 props를 통해 데이터를 전달하는 것이 더 적합

### 컨텍스트 API

> 1. React.createContext()
>
> - 컨텍스트를 생성하기 위한 함수
> - 컨텍스트 객체를 리턴함
> - 기본값으로 undefined를 넣으면 기본값이 사용되지 않음

> 2. Context.Priovider
>
> - 모든 컨텍스트 객체는 Provider라는 컴포넌트를 갖고 있음
> - Provider 컴포넌트로 하위 컴포넌트를 감싸주면 모든 하위 컴포넌트들이 해당 컨텍스트의 데이터에 접근할 수 있게 됨
> - 여러 개의 Provider 컴포넌트를 중첩시켜 사용할 수 있음

> 3. Class.contextType
>
> - Provider 하위에 있는 클래스 컴포넌트에서 컨텍스트의 데이터에 접근하기 위해 사용
> - 단 하나의 컨텍스트만을 구독할 수 있음

> 4. Context.Consumer
>
> - 컨텍스트의 데이터를 구독하는 컴포넌트
> - 데이터를 소비한다는 뜻에서 consumer 컴포넌트라고도 부름
> - consumer 컴포넌트는 컨텍스트 값의 변화를 지켜보다가 값이 변경되면 재렌더링됨
> - 상위 레벨에 매칭되는 Provider가 없을 경우 기본값이 사용됨

> 5. Context.displayName
>
> - 크롬의 리액트 개발자 도구에서 표시되는 컨텍스트 객체의 이름

### 여러 개의 컨텍스트 사용하기

> 1. Provider 컴포넌트와 Consumer 컴포넌트 여러 개 중첩해서 사용하면 됨

# 10주차 (2023.05.11)

> 오늘은 시험 점수 확인과 시험 다시보기, 실습을 하였다.

### state 끌어올리기

> 하위 컴포넌트의 state를 공통된 부모 컴포넌트로 끌어올려서 공유하는 방식

### 실습 (섭씨온도와 화씨온도 표시하기)

> <img width="1440" alt="스크린샷 2023-05-04 오후 12 31 19" src="https://user-images.githubusercontent.com/126742685/236106956-a66136ea-09fd-41be-94e5-5029cd6b00c5.png">

# 9주차 (2023.05.04)

> 이번 주차는 리액트에서 리스트를 렌더링 하는 방법과 키에대해 배우고, 리액트의 제어 컴포넌트외 이를 이용해서 사용자의 입력을 받는 방법에 대해 배웠다.

### 리스트

> 같은 아이템을 순서대로 모아놓은 것

### 키

> 각 객체나 아이템을 구분할 수 있는 고유한 값

### 여러 개의 컴포넌트 렌더링

> 자바스크립트 배열의 map() 함수를 사용
>
> - 배열에 들어있는 각 변수에 어떤 처리를 한 뒤 결과(엘리먼트)를 배열로 만들어서 리턴함
> - map() 함수 안에 있는 엘리먼트는 꼭 키가 필요함

### 리스트의 키

> 1. 리스트에서 아이템을 구분하기 위한 고유한 문자열
> 2. 리스트에서 어떤 아이템이 변경, 추가 또는 제거되었는지 구분하기 위해 사용
> 3. 리액트에서는 키의 값은 같은 리스트에 있는 엘리먼트 사이에서만 고유한 값이면 됨

### 다양한 키값의 사용법

> 1. 숫자 값을 사용
>
> - 배열에 중복된 숫자가 들어있다면 키값도 중복되기 때문에 고유해야 한다는 키값의 조건이 충족되지 않음

> 2. id를 사용
>
> - id의 의미 자체가 고유한 값이므로 키값으로 사용하기 적합
> - id가 있는 경우에는 보통 id 값을 키값으로 사용

> 3. 인덱스를 사용
>
> - 배열에서 아이템의 순서가 바뀔 수 있는 경우에는 키값으로 인덱스를 사용하는 것을 권장하지 않음
> - 리액트에서는 키를 명시적으로 넣어 주지 않으면 기본적으로 이 인덱스 값을 키값으로 사용

### 실습 (출석부 출력하기)

> <img width="1440" alt="스크린샷 2023-05-04 오전 10 41 51" src="https://user-images.githubusercontent.com/126742685/236090868-a6c8e5b7-e666-466a-af7a-2b80dafc7df5.png">

### 폼이란?

> 사용자로부터 입력을 받기 위해 사용하는 양식

### 제어 컴포넌트

> 1. 사용자가 입력한 값에 접근하고 제어할 수 있게 해주는 컴포넌트
> 2. 값이 리액트의 통제를 받는 입력 폼 엘리먼트

### <input type="text"> 태그

> 1. 한 줄로 텍스트를 입력받기 위한 HTML 태그
> 2. 리액트에서는 value라는 attribute로 입력된 값을 관리

### <textarea> 태그

> 1. 여러 줄에 걸쳐서 텍스트를 입력받기 위한 HTML 태그
> 2. 리액트에서는 value라는 attribute로 입력된 값을 관리

### <select> 태그

> 1. 드롭다운 목록을 보여주기 위한 HTML 태그
> 2. 여러 가지 옵션 중에서 하나 또는 여러 개를 선택할 수 있는 기능을 제공
> 3. 리액트에서는 value라는 attribute로 선택된 옵션의 값을 관리

### <input type="file"> 태그

> 1. 디바이스의 저장 장치로부터 사용자가 하나 또는 여러 개의 파일을 선택할 수 있게 해주는 HTML 태그
> 2. 서버로 파일을 업로드하거나 리액트에서는 비제어 컴포넌트가 됨

### 여러 개의 입력 다루기

> 컴포넌트에 여러 개의 state를 선언하여 각각의 입력에 대해 사용하면 됨

### input Null Value

> value prop은 넣되 자유롭게 입력할 수 있게 만들고 싶을 경우, 값에 undefined 또는 null을 넣으면 됨

### 실습 (사용자 정보 입력받기)

> <img width="1440" alt="스크린샷 2023-05-04 오전 11 51 35" src="https://user-images.githubusercontent.com/126742685/236102295-0f65f698-0c5b-4c72-9470-fdf54ab89032.png">

### Shared state

> 하위 컴포넌트가 공통된 부모 컴포넌트의 state를 공유하여 사용하는 것

# 8주차 (2023.04.27)

> 이번 시간은 이벤트와 렌더링에 대해 배웠다.

### 이벤트란?

> 사용자가 버튼을 클릭하는 등의 사건을 의미

### 이벤트 처리하기

> 1. DOM의 이벤트
>
> - 이벤트의 이름을 모두 소문자로 표시
> - 이벤트를 처리할 함수를 문자열로 전달

> 2. 이벤트 핸들러
>
> - 이벤트가 발생했을 때 해당 이벤트를 처리하는 함수
> - 이벤트 리스너라고 부르기도 함
> - 클래스 컴포넌트
> - - 클래스의 함수로 정의하고 생성자에서 바인딩해서 사용
> - - 클래스 필드 문법도 사용가능
> - 함수 컴포넌트
> - - 함수 안에 함수로 정의하거나 arrow function을 사용해서 정의

### arguments 전달하기

> 1. Argument란?
>
> - 함수에 전달할 데이터
> - 피라미터 또는 매개변수라고 부르기도 함

> 2. 클래스 컴포넌트
>
> - arrow function을 사용하거나 Fuction.prototype.bind를 사용

> 3. 함수 컴포넌트
>
> - 이벤트 핸들러 호출 시 원하는 순서대로 매개변수를 넣어서 사용

#### 실습 (클릭 이벤트 처리하기)

> <img width="1440" alt="스크린샷 2023-04-27 오전 10 47 41" src="https://user-images.githubusercontent.com/126742685/234739991-44daa861-d13e-4c6e-9b0a-c98026c00f06.png">

### 조건부 렌더링

> 조건에 따라 렌더링의 결과가 달라지도록 하는 것

### 엘리먼트 변수

> - 리액트 엘리먼트를 변수처럼 저장해서 사용하는 방법

### 인라인 조건

> 1. 조건문을 코드 안에 집어넣는 것

> 2. 인라인 if
>
> - if문을 필요한 곳에 직접 집어넣어서 사용하는 방법
> - 논리 연산자 &&를 사용(AND 연산)
> - 앞에 나오는 조건문이 true일 경우에만 뒤에 나오는 엘리먼트를 렌더링

> 3. 인라인 if-Else
>
> - if-Else문을 필요한 곳에 직접 넣어서 사용하는 방법
> - 삼향 연산자?를 사용
> - 앞에 나오는 조건문이 true면 첫 번째 항목을 리턴, false면 두 번째 항목을 리턴
> - 조건에 따라 각기 다른 엘리먼트를 렌더링하고 싶을 때 사용

### 컴포넌트 렌더링 막기

> 1. 리액트에서는 null을 리턴하면 렌더링되지 않음

> 2. 특정 컴포넌트를 렌더링하고 싶지 않을 경우 null을 리턴하면 됨

### 실습 (로그인 여부를 나타내는 툴바 만들기)

> <img width="1440" alt="스크린샷 2023-04-27 오후 12 15 14" src="https://user-images.githubusercontent.com/126742685/234750794-f2c5201f-a543-46ff-8243-5aa1c8be1c4b.png">

# 7주차 (2023.04.13)

> 오늘은 가장 많이 사용하는 훅에 대해 배웠다.
> state와 effect를 잘 알아 두어야 한다.

### 훅

> 1. 리액트의 state와 생명주기 기능에 갈고리를 걸어 원하는 시점에
>    정해진 함수를 실행되도록 만든 것

> 2. useState()
>
> - state를 사용하기 위한 훅
> - 함수 컴포넌트에서는 기본적으로 state라는 것을 제공하지 않음
> - 클래스 컴포넌트처럼 state를 사용하고 싶으면 useState() 훅을
>   사용해야함
> - 사용법
> - - const [변수명, set함수명] = useState (초깃값);
> - - 변수 각각에 대해 set 함수가 따로 존재함

```
useState() 훅을 사용하는 예제 코드

import React, {useState} from "react";

function Counter(props) {
  var count = 0;

  return (
    <div>
      <p>총 {count}번 클릭했습니다.</p>
      <button onClick={() => count++}>
          클릭
      </button>
    </div>
  );
}

```

> 3. useEffect()
>
> - 사이드 이펙트를 수행하기 위한 훅
> - 사이드 이펙트란 서버에서 데이터를 받아오거나 수동으로 DOM을
>   변경하는 등의 작업
> - useEffect() 훅만으로 클래스 컴포넌트의 생명주기
>   함수들과 동일한 기능을 수행할 수 있음
> - 사용법
> - - useEffect(이펙트 함수, 의존성 배열);
> - - 의존성 배열 안에 있는 변수 중에 하나라도 값이 변경되었을 때
>     이펙트 함수가 실행됨
> - - 의존성 배열에 빈 배열([])을 넣으면 언마운트시에 단 한 번씩만
>     실행됨
> - 의존성 배열 생략 시 컴포넌트가 업데이트될 때마다 호출됨
> - 선언된 컴포넌트의 props와 state에 접근할 수 있음
> - useEffect()에서 리턴하는 함수는 컴포넌트 마운트가 해제될 때 호출됨

```
useEffect()를 사용한 예제 코드

import React, {useState, useEffect} from "react";

function Counter(props) {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = '총 ${count}번 클릭했습니다.';
  });

  return (
    <div>
      <p>총 {count}번 클릭했습니다.</p>
      <button onClick={() => setCount(count +1)}>
        클릭
      </button>
    </div>
  );
}
```

> 4. useMemo()
>
> - Memoized value를 리턴하는 훅
> - 연산량이 높은 작업이 매번 렌더링될 때마다 반복되는 것을 피하기 위해 사용
> - 렌더링이 일어나는 동안 실행되므로 렌더링이 일어나는 동안 실행돼서는 안될
>   작업을 useMemo()에 넣으면 안 됨
> - 사용법
> - - const memoizedValue = useMemo(값 생성 함수, 의존성 배열);
> - - 의존성 배열에 들어있는 변수가 변했을 경우에만 새로 값 생성 함수를 호출하여
>     결괏값을 반환함
> - - 그렇지 않은 경우에는 기존 함수의 결괏값을 그대로 반환함
> - - 의존성 배열을 넣지 않을 경우 렌더링이 일어날 때마다 매번 값 생성
>     함수가 실행되므로 의미가 없음

> 5. useCallback()
>
> - useMemo() 훅과 유사하지만 값이 아닌 함수를 반환한다는 점이 다름
> - useCallback(콜백 함수, 의존성 배열);은 useMemo(() => 콜백 함수,
>   의존성 배열);과 동일 훅을 사용하여 불필요한 함수 재정의 작업을 없애는 것
> - 사용법
> - - const memoizedCallback = useCallback(콜백 함수, 의존성 배열);
> - - 의존성 배열에 들어있는 변수가 변했을 경우에만 콜백 함수를 다시 정의해서 리턴함.

> 6. useRef()
>
> - 레퍼런스를 사용하기 위한 훅
> - 레퍼런스란 특정 컴포넌트에 접근할 수 있는 객체를 의미
> - 매번 렌더링될 때마다 항상 같은 레퍼런스 객체를 반환
> - 사용법
> - - const refContainer = useRef(초깃값);
> - - current라는 속성을 통해서 접근

### 훅의 규칙

> 1. 무조건 최상위 레벨에서만 호출해야함
>
> - 반복문이나 조건문 또는 중첩된 함수들 안에서 훅을 호출하면 안 됨
> - 컴포넌트가 렌더링될 때마다 매번 같은 순서로 호출되어야 함

> 2. 리액트 함수 컴포넌트에서만 훅을 호출해야 함
>
> - 혹은 리액트 함수 컴포넌트에서 호출하거나 직접 만든 커스텀
>   훅에서만 호출할 수 있음

### 커스텀 훅

> 1. 이름이 use로 시작하고 내부에서 다른 훅을 호출하는 단순한 자바스크립트 함수
> 2. 파라미터로 무엇을 받을지, 어떤 것을 리턴해야 할지를 개발자가 직접 정할 수 있음
> 3. 중복되는 로직을 커스텀 훅으로 추출하여 재사용성을 높이기
> 4. 이름이 use로 시작하지 않으면 특정 함수의 내부에서 훅을 호출하는지를 알 수 없기
>    때문에 훅의 규칙 위반 여부를 자동으로 확인할 수 없음

### 실습 (훅을 사용한 컴포넌트 개발)

> <img width="1440" alt="스크린샷 2023-04-13 오전 11 36 21" src="https://user-images.githubusercontent.com/126742685/231633606-c1051869-b6bd-4530-ad45-33b9d0782c9c.png">

# 6주차 (2023.04.06)

> 오늘은 컴포넌트 추출과 실습에 이미지를 넣어봤다.
> State에 대해 배웠다.

### 컴포넌트 추출

> 1. 큰 컴포넌트에서 일부를 추출해서 새로운 컴포넌트를 만드는 것
> 2. 기능 단위로 구분하는 것이 좋고, 나중에 곧바로 재사용이 가능한
>    형태로 추출하는 것이 좋음

#### 실습(댓글 컴포넌트 만들기)

> <img width="1440" alt="image" src="https://user-images.githubusercontent.com/126742685/230256786-91235bad-11f5-42a8-af11-ea9f57ed61c0.png">

### State

> 1. 리액트 컴포넌트의 변경 가능한 데이터
> 2. 컴포넌트를 개발하는 개발자가 직접 정의해서 사용
> 3. state가 변경될 경우 컴포넌트가 재렌더링됨
> 4. 렌더링이나 데이터 흐름에 사용되는 값만 state에 포함시켜야 함

### State의 특징

> 1. 자바스크립트 객체 형태로 존재
>
> 2. 직접적인 변경이 불가능 함
>
> 3. 클래스 컴포넌트
>
> - 생성자에서 모든 state를 한 번에 정의
> - state를 변경하고자 할 때에는 꼭 setState()함수를 사용해야 함
>
> 4. 함수 컴포넌트
>
> - useState()훅을 사용하여 각각의 state를 정의
> - 각 state별로 주어지는 set함수를 사용하여 state 값을 변경

### 생명주기

> 1. 마운트
>
> - 컴포넌트가 생성될 떼
> - componentDidMount()
>
> 2. 업데이트
>
> - 컴포넌트의 props가 변경될 때
> - setState() 함수 호출에 의해 state가 변경될 때
>
> 3. 언마운트
>
> - 상위 컴포넌트에서 현재 컴포넌트를 더 이상 화면에 표시
>   하지 않게 될 때
> - componentWillUnmount()
>
> 4. 컴포넌트는 계속 존재하는 것이 아니라 시간의
>    흐름에 따라 생성되고 업데이트되다가 사라지는 과정을
>    겪음

#### 실습(State 사용해보기)

> <img width="1440" alt="스크린샷 2023-04-06 오후 12 09 19" src="https://user-images.githubusercontent.com/126742685/230262914-79f4b18a-8bc7-4a44-895d-de145dd58bef.png">

# 5주차 (2023.03.30)

> 이번주는 리액트 엘리먼트 개념과 특징,
> props와 컴포넌트 대해 배웠다.

### 엘리먼트의 정의

> 1. 리액트 앱의 가장 작은 빌딩 블록들
> 2. 화면에 나타나는 내용을 기술하는 자바스크립트 객체
> 3. 리액트 엘리먼트는 DOM 엘리먼트의 가상 표현

### 엘리먼트의 생김새

> 1. 엘리먼트는 자바스크립트 객체 형태로 존재
> 2. 컴포넌트 유형과 속성 및 내부의 모든 자식에 대한 정보를
>    포함하고 있는 일반적인 자바스크립트 객체

### 엘리먼트의 특징

> 1. 불변성을 갖고 있음
> 2. 엘리먼트 생성 후에는 자식이나 속성을 바꿀 수 없음.

### 엘리먼트 렌더링하기

> 1. 렌더링을 위해 ReactDOM의 render()라는 함수를 사용
>
> - 리액트 엘리먼트를 HTML 엘리먼트에 렌더링하는 역할
>
> 2. 렌더링 되는 과정을 Virtual DOM에서 실제 DOM으로 이동하는 과정

### 렌더링된 엘리먼트 업데이트하기

> 1. 엘리먼트는 한 번 생성되면 바꿀 수 없기 때문에 엘리먼트를
>    업데이트하기 위해서는 다시 생성해야 함.
> 2. 기존 엘리먼트를 변경하는 것이 아니라 새로운
>    엘리먼트를 생성해서 바꿔치기 하는 것

```
실습: 시계 만들기
import React from "react";

function Clock(props) {
  return (
    <div>
      <h1>안녕, 리액트</h1>
      <h2>현재 시간: {new Date().toLocaleTimeString()}</h2>
    </div>
  );
}

export default Clock;
```

### 리액트 컴포넌트

> 1. 컴포넌트 기반 구조
>
> - 작은 컴포넌트들이 모여서 하나의 컴포넌트를 구석하고 이러한 컴포넌트들이 모여서 전체 페이지를 구성
>
> 2. 개념적으로는 자바스크립트의 함수와 비슷함
>
> - 속성들을 입력으로 받아서 그에 맞는 리액트 엘리먼트를 생성하여
>   리턴함.

### Props

#### Props의 개념

> 1. 리액트 컴포넌트의 속성
> 2. 컴포넌트에 전달할 다양한 정보를 담고 있는 자바스크립트 객체

#### Props의 특징

> 1. JSX를 사용할 경우 컴포넌트에 키-값 쌍 형태로 넣어 주면 됨
> 2. 문자열 이외에 정수, 변수, 그리고 다른 컴포넌트 등이 들어갈
>    경우에는 중괄호를 사용해서 감싸주어야 함
> 3. JSX를 사용하지 않는 경우에는 createElement() 함수의 두 번째
>    파라미터로 자바스크립트 객체를 넣어 주면 됨

### 컴포넌트 만들기

> 1. 컴포넌트의 종류
>
> - 클래스 컴포넌트와 함수 컴포넌트로 나뉨
>
> 2. 함수 컴포넌트
>
> - 함수 형태로 된 컴포넌트
>
> 3. 클래스 컴포넌트
>
> - ES6의 클래스를 사용하여 만들어진 컴포넌트
>
> 4. 컴포넌트 이름 짓기
>
> - 컴포넌트의 이름은 항상 대문자로 시작해야 함
> - 소문자로 시작할 경우 컴포넌트를 DOM 태그로 인식하기 때문
>
> 5. 컴포넌트 렌더링
>
> - 컴포넌트로부터 엘리먼트를 생성하여 이를 리액트 DOM에 전달

### 컴포넌트 합성

> 여러 개의 컴포넌트를 합쳐서 하나의 컴포넌트를 만드는 것

# 4주차 (2023.03.23)

> 오늘은 npm start를 하고, 웹사이트에 직접 리액트를 연동했다.
> 그리고 프로젝트를 생성한 뒤 repository를 삭제했다.

> 터미널에 git config --global user.name,
> git config --global user.email을 입력하여 사용자 이름과,
> 이메일을 추가하였다.
> 새롭게 23-React1을 생성해서 커밋했다.

> JSX는 자바스크립트 문법을 확장시킨 것이기 때문에, 모든 자바스크립트 문법을
> 지원한다.

```
  const name = '소플';
  const element = <h1>안녕, {name}</h1>

  ReactDOM.render(
      element,
      document.getElementById('root')
  );
```

> 위의 코드에서 엘리먼트를 선언하는 부분의 코드처럼 HTML과 자바스크립트가 섞인
> 형태로 코드를 작성하면 된다.
> XML/HTML 코드를 사용하다가 중간에 자바스크립트 코드를 사용하고 싶으면
> 중괄호를 써서 묶어주면 된다.

### JSX의 역할

> 1. JSX로 작성된 코드는 모두 자바스크립트 코드로 변환
> 2. 리액트는 JSX 코드를 모두 createElement() 함수를 사용하는 코드로 변환

### JSX의 장점

> 1. 코드가 간결해짐
> 2. 가독성 향상
> 3. Injection Attack을 방어함으로써 보안성이 올라감

### JSX 사용법

> 1. 기본적으로 모든 자바스크립트 문법을 지원
> 2. 자바스크립트에 XML과 HTML을 섞어서 사용
> 3. 중괄호를 사용하여 자바스크립트 코드를 삽입

# 3주차 (2023.03.16)

> 오늘은 Node.js를 설치하는 작업을 였다. git.bash를 이용하여 설치한 node.js의 버전을 확인하였다.
> 리액트는 사용자와 웹사이트의 상호작용을 돕는 인터페이스를 만들기 위한 자바스크립트 기능 모음집이다.

> Virtual DOM은 가상의 DOM이다. DOM을 뭔지 확인하기 위해 크롬 개발자 도구를 열어 콘솔 탭에서 document라고 입력하면
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
> html, head, body이다.

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
> 증감 연산자를 변수의 뒤에 붙이는 방식을 postfix 방식, 변수의 앞에 붙이는 방식을 prefix방식이라고 한다.
> 관계 연산자는 변수들 사이의 관계를 비교하기 위해서 사용하기 때문에 비교 연산자 라고도 한다.

> 오늘 수업에서는 Github 가입 및, 파일 생성 하는 법과 간단한 이론을 배웠다.

# 1주차 (2023.03.02)

1. 오리엔테이션

2. Github가입
