12/24 Study
============

## Component

### What is component?
>javascript 함수와 유사


### component 렌더링

    function welcome(props){
        return <h1>Hello, {props.name}</h1>;
    }

    const root = ReactDOM.createRoot(document.getElementById('root'));
    const element = <Welcome name="Sara" />;
    root.render(element);

>사용자 정의 컴포넌트 가능
>component 이름은 항상 대문자로 시작


### props는 읽기 전용
>컴포넌트 자체 props 수정 X


12/23 Study
============

## Element

### What is element?
>react에서 가장 작은 단위. 화면에 표시할 내용
>컴포넌트의 구성 요소


### DOM에 엘리먼트 렌더링

    <div id='root'></div>

>root DOM 노드

    const root = ReactDOM.createRoot(
        document.getElementById('root');
    );

    const element = <h1>hello world!</h1>;
    root.render(element);

### 엘리먼트 업데이트

    function tick(){
        const element ={
            <div>
            <h1>hello world!</h1>
            <h2>It is {new Date().toLocaleTimeString()}.</h2>
            </div>
        };
        root.render(element);
    }

    setInterval(tick,1000);

> setInteval 함수가 tick을 초에 한번 호출해야하지만, 실제로는 한번만 호출.
> react DOM은 해당+자식 엘리먼트를 이전과 비교해 필요한 경우에만 DOM을 업데이트함

12/21 Study
============

## JSX

### What is JSX?
> javascript xml
> 마크업과 로직 분리x 
> js 코드 안에서 UI 작업 할 때 시각적으로 도움

    const name = 'Josh Perez';
    const element = <h1>Hello, {name}</h1>;

>중괄호 안은 유효한 js 표현식 모두 가능

### 속성 정의
> attribute 에 js 표현식 넣을 때 ""나 {} 중 하나만 쓰기
> html attribute 이름 대신 camelcase 프로퍼티 사용



12/19 Study
============

## map()
    const numbers = [1, 2, 3];
    const doubled = numbers.map(x => x * 2); // [2, 4, 6]

> JS array가 가지고 있는 함수

## key
> 각 컴포넌트를 구별할 수 있게 하여 다시 렌더링 할 때 state를 유지
> 컴포넌트는 key 조회 불가

12/15 Study
============

## 함수 component
    state없이 render함수만을 가짐
    react.component 확장 클래스 대신 props를 입력받아서 렌더링할 대상을 반환

12/14 Study
============

## 부모 component에서 자식에 state 요청 X
    부모 component에서 각 state를 저장하는 방법으로
    부모가 자식에게 prop을 전달

> 자식 컴포넌트들이 서로 통신하려면 부모 컴포넌트에서 공유 state를 정의해야함


12/13 Study
============

## function()={} 을 ()=> 로 변환 가능
    onClick={() => console.log('click')}
onClick prop으로 console.~ 함수를 전달

## 하위 클래스의 생성자 정의할 때 super 호출
    모든 react 컴포넌트 클래스는 생성자를 가질 때 super(props) 호출해야함




## 불변성

> 직접적인 객채 변경이나, 기본 데이터 변경 X
### 장점
1. 복잡한 특징들을 단순하게 함 (특정 행동을 취소하고 되돌리기 등의 기능 구현)
   * 이전 버전의 이력을 유지하고 재사용할 수 있게 함
2. 변화 감지에 용이
3. React에서 다시 렌더링 하는 시기를 결정
   * react에서 순수 컴포넌트 만드는데 도움
   * 변경 판단 후 컴포넌트가 다시 렌더링 할지를 결정 

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
