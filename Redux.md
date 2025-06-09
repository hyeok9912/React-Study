<h1>Redux 란?</h1>
<p>Redux 는 자바스크립트의 상태관리 라이브러리이다.</p>
<p>Redux 와 같은 상태관리 라이브러리를 사용하는 이유에는</p>
<p>스토어라는 하나의 저장소에서 모든 데이터를 관리하고 다양한 컴포넌트에서 호출하여 편하게 사용할 수 있기 때문이다. </p>
<p>기존의 리액트의 경우 부모 컴포넌트에서 자식 컴포넌트로만 프롭스를 이용해서 데이터를 전달 할 수 있었다.</p>
<p>하지만 이 경우에는 최상단의 부모 컴포넌트로 부터 최하단의 자식 컴포넌트로 데이터를 전달하기 위해서는 중간의 컴포넌트들을 모두 거쳐야한다는 불편함이 존재한다.</p>
<p>이 불편한점을 해결하기 위해 Redux를 사용한다.</p>
<p>Redux의 경우에는 store.js 라는 저장소 공간에 모든 데이터를 보관하고 Redux의 스토어에 데이터를 저장하기 위해서는 아래와 같은 방식을 따른다.</p>
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FvrIOU%2FbtscyH8ejYP%2FkT86gfflLzuAMOvojvejFk%2Fimg.png"></img>
<p>먼저 애플리케이션에서 dispatch를 통해 action 객체를 reducer에게 전달하고 reducer는 기존의 상태와 action객체를 비교하여 기존의 데이터를 유지한 상태로 새로운 상태를 반영한 복사본을 store에 전달한다.</p>
<p>이후 store는 변경된 상태 컴포넌트들에게 전달하고 컴포넌트는 UI에 반영한다</p>
<p>이 과정중 추가적인 비동기 작업이 있다면 미들웨어를 거쳐 리듀서에게 전달된다.</p>
<h2>하위 컴포넌트에서 사용시</h2>
<p>useSelector 를 통해서 스토어의 특정값만 추출해서 사용할 수 있다</p>
<p>useDispatch를 통해 특정 액션객체를 리듀서로 전달하여 스토어를 업데이트 할 수 있다.</p>

<h2>Redux 의 원칙</h2>
<p>1. Single source of thuth</p>
<p>동일한 데이터는 하나의 공간에서 가져온다.</p>
<p>같은 데이터일 경우 하나의 스토어에서 가져온다.</p>
<p>2. State is Readonly</p>
<p>임의로 스토어의 상태를 변경할 수 없다.</p>
<p>스토어의 상태는 액션객체와 디스패치를 통해 변경 할 수 있다.</p>
<p>3. Change are made with Pure function</p>
<p>리듀서의 함수는 순수 함수로만 구성되어야 한다.</p>
