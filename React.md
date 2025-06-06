<details>
  <summary>
    <h1>React 란?</h1>
  </summary>
  <p>React 는 자바스크립트의 라이브러리로써 사용자의 인터페이스를 구축하기 위해 사용된다.</p>
  <br/>
  <h1>특징</h1>
  <p>- 컴포넌트 기반의 UI 업데이트</p>
  <p>- Virtual Dom 을 사용한 Dom 구조의 업데이트</p>
</details>
<br/>
<details>
  <summary>
    <h1>왜 React를 사용하는가?</h1>
  </summary>
  <p>기존의 html , css 만으로도 충분히 사용자 UI를 구축할 수 있다 하지만 React를 사용하는 이유에는 자바스크립트의 Dom에 대해서 알아야 한다.<p>
  <p>우리가 html 을 이용해서 돔의 구조를 변경하려면 DomSelect Api 를 이용해서 특정 돔을 선택한 뒤에 이벤트가 발생하게 하고 이벤트 발생에 따라 UI가 변화한다.<p>
  <p>하지만 이렇게 되면 작은 규모의 프로젝트에서는 문제가 되지 않겠지만 큰 프로젝트의 경우에는 다양한 이벤트가 일어나고 동시다발적으로 일어나기 때문에 Dom구조가 매우 복잡해지고 유지보수가 어려워 질 수 있다.<p>
  <img src='https://i.imgur.com/mJftTBq.png'></img>
  * 출처 'https://react.vlpt.us/basic/01-concept.html'
  <p>이러한 점에서 불편함을 줄여줄 수 있는 라이브러리가 React이다.<p>
  <p>React는 컴포넌트 기반의 동작을 한다.<p>
</details>
<details>
  <summary>
    <h2>컴포넌트란?</h2>
  </summary>
  <p>컴포넌트는 독립적인 요소를 의미하고 페이지를 이루고 있는 구성요소들을 의미한다.<p>
  <br/>
  <p>다시 돌아와서 컴포넌트를 사용할 경우 우리는 독립성과 재사용성을 확보할 수 있다.<p>
  <p>한 페이지 내부의 컴포넌트가 모두 독립적으로 동작하기 때문에 각 기능별 유지보수가 쉬울 뿐만 아니라 필요한 곳에 import 해서 사용할 수 있기 때문에 자주 사용되는 컴포넌트를 재사용 할 수 있다.</p>
  <p>리액트의 또 하나의 특징으로 Virtual Dom 이 있는데<p>
  <p>설명 했던 부분이지만 대규모 애플리케이션의 경우 하나의 이벤트 핸들러의 여러번의 Dom 요소의 변화가 있을 수 있고 하나의 Dom 요소에 여러개의 이벤트 핸들러가 존재 할 수 있다. 이렇게 되면 Dom 의 업데이트가 자주 일어나게 되고 브라우저는 변화가 일어날 때 마다 Dom을 다시 그려야 한다. 이렇게 되면 애플리케이션의 성능이 저하될 수 있다.<p>
  <p>React에서는 Vertial Dom을 사용한다.<p>
  <img src='https://i.imgur.com/u6YnxUS.png'></img>
  * 출처 'https://react.vlpt.us/basic/01-concept.html'
  </details>
  <details>
    <summary>
      <h1>Vertial Dom 이란?</h1>
    </summary>
  <p>실제 브라우저가 화면에 그리는 Dom 을 메모리에 자바스크립트의 객체 형태로 복사 해 놓은 형태이다.<p>
  <p>리액트에서는 Dom구조를 업데이트 해야 할 때에 실제 Dom 구조를 변경하지 않고 아래의 과정으로 동작한다<p>
  <p>1.변경된 내용을 기준으로 가상돔을 메모리에 생성한다.<p>
  <p>2.기존의 돔 구조와 업데이트 된 돔 구조를 비교한다.<p>
  <p>3.차이점을 바탕으로 변경된 부분만 찾아 실제 돔 구조에 반영한다.<p>
  <p>이 과정을 **Reconciliation(재조정)**이라고 한다.<p>
</details>

<details>
  <summary>
    <h1>나의 한줄 생각</h1>
  </summary>
  <p>- 기존의 html , css 의 유지보수의 불편함과 유지보수의 어려움에서 React라는 프레임워크가 등장하게 되었고 그 특징에 대해 다시 한번 보게 되면서 React에 대해서 조금 더 명확해 진 거 같다.</p>
</details>
