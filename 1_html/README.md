# 1. HTML과 CSS

HTML은 하이퍼텍스트 마크업 언어(HyperText Markup Language, 문화어: 초본문표식달기언어, 하이퍼본문표식달기언어)라는 의미의 웹 페이지를 위한 지배적인 마크업 언어다.

HTML은 웹 브라우저에서 보이는 외관이라고 할 수 있다. 주의해야할 점은 html로 웹을 디자인하는 것이 아닌 웹의 기본 뼈대를 만드는 것이다.

## 1.1 Web

웹(Web)은 전 세계에 흩어져 있는 정보 자원을 연결하는 네트워크(World Wide Web)을 말합니다. 이 네트워크는 컴퓨터와 인터넷을 이용하여 접속할 수 있고 거미줄(web)처럼 복잡하게 얽혀져 있습니다. 사람들이 웹을 통해 정보자원에 접근하여 이용할 수 있는 것은 다음과 같은 메커니즘을 갖고 있기 때문인데 이것을 웹의 3대 요소라고 부른다.


<img src="https://t1.daumcdn.net/cfile/tistory/2678CA44552E934902"></img>
> 웹의 3요소

* URL : 정보자원의 위치를 표시하기 위한 표기법
* HTTP : 위치 표시가 있는 정보자원에 접근하기 위한 통신 규약
* HTML : 정보자원과 정보자원 사이를 오가기 위한 하이퍼텍스트

출처: http://webdir.tistory.com/33 [WEBDIR]

## 1.2 HTML 기본 구성
~~~~
<!DOCTYPE html>
<html>
    <head>
        <title>Title of the document</title>
    </head>
    <body>
    	The content of the document......
    </body>
</html
~~~~
> index.html

위에 코드를 보시면 아주 간단한 HTML 코드이다. 보이는 것과 같이 HTML에는 기본적으로 몇 개의 테크로 뼈대를 나눠놨다.

* __html__
* __head__
* __body__

크게 세개가 있다. 첫 번째로 html테크는 이 태그안에 있는 코드들은 html 마크업 언어로 정의한다는 표현이다. 두 번째로 head 태그안에는 현재 사이트의 설정 코드들을 정의하는 부분이다. 페이지를 열때 웹브라우저에 어떤 것도 표시되지 않으며, ```<title>```같은 페이지나, CSS의 링크, 파비콘(favicon), 그리고 다른 meta data를 포함한다. 마지막으로 body 태그안에 본문의 내용, 그리고 뼈대를 작성하는 부분이다.

이제부터 주로 다루는 내용은 body태그안에서 다루는 작업들이다.

## 1.3 HTML 요소

HTML은 Markup language이다. 그러하여 태그들로 구성작성되어 있다. 태그들은 '시작 태그'와 '종료 태그'로 나눌 수 있다.

<img src="https://t1.daumcdn.net/cfile/tistory/25691C3F552EADD21E"></img>

태그는 이런 식으로 꺾쇠괄호(<>)로 둘러싸인 키워드이다. 태그들은 (<>)로 시작하여 (</>) '/'를 포함한 꺾쇠괄호로 끝을 맺어야한다. 이렇게 함으로써 내가 지정한 태그의 영역을 명확히 구분할 수 있기 때문이다.

태그들 가운데 쌍을 이루지 않고 혼자서 그 쓰임을 다하는 것들이 있는데, 예로 ```<input/>, <img/>```가 있으며, 이들을 __홀태그__ 라고 부른다.


또한 태그안에는 텍스트 내용이 아닌 속성들을 가지고 있다. 쉽게 말하자면, 이 태그의 특징을 설정한다고 생각할 수 있다. 

예를 들어, 
~~~
<button> click </button>
~~~
이라는 버튼을 만들었다. 하지만 코드로만 봤을 땐, 이 버튼만 생길 뿐이지, 버튼을 눌렀을 경우 어떤 이벤트도 일어나지 않을 것이다. 이런 클릭 이벤트라던가, 버튼의 크기, 이미지 source 같은 것들을 정의할 수 있다.

이런 태그 속성은 html작성하는 데 빼놓을 수 없는 요소이고, 속성이 없는 태그들은 안에 내용물이 없는 껍데기라고 생각할 수 있다.


<img src="https://t1.daumcdn.net/cfile/tistory/217AC745552EB25920"></img>

위의 그림과 같이 __속성 이름(attribute)__ 과 __값(value)__ 이 한 쌍으로 구성되어 있다.


### 주요 HTML 태그

* ``` <TABLE>, <ul>, <ol>, <li> ```
* ``` <img src= > ```
* ``` <a href=“http://..............”> ```
* ``` <H1>, <H2>, <strong>, <q>, <p>, <br>, <!--...--> ```

Paragraph, break, pre

- 유사한 주제의 문자열 모음 ``` <p>```
- 줄 바꿈 ```<br>```
- 문자열 그대로 ```<pre>```

이런 text 태그에는 block element와 inline element가 있다.

* Block element:
  * ``` <h1>, <h2>,..., <p>, <blockquote>, <ol>, <ul>, <li> ```
  * Element 앞과 뒤에서 line break를 가진다. (줄바꿈)

* Inline element:
  *  Inline Element는 Inline Element만을 포함
  *  줄바꿈 되지않음


논리적인 블록 영역을 설정하기 위해서 div를 대표적으로 사용한다.

``` <div id=“some unique name”> ``` 

또한, id 속성을 사용하여 현재 태그를 식별할 수 있다.


### Document Object Model(DOM)
CSS 나 Javascript를 진행하기 앞서 dom에 대한 개념이 필요할까 싶어 넣게 되었습니다. 
<img src="https://thebook.io/img/006946/031.jpg"></img>

출처 : https://thebook.io/006946/ch01/02/01/01/

HTML안에 구성 요소들을 구조적인 object 트리형석으로 구성된 모델이다.
저런 object들은 부모 노드를 식별될 수 있으며, javascript를 통해 document 구조, 스타일, 내용들을 변화시키기 위해 접근될 수 있다.

~~~javascript
document.getElementsByTagName('body')
~~~
> javascript 예시 (body tag를 가리킴)

잠깐 예시를 보면 코드의 document는 dom의 document를 가르키는 것이다. javascript는 dom을 이용하여 html의 구조, 스타일, 내용을 변환시킬 수 있다.

## Cascading Style Sheets(CSS)
주로 css라고 많이 부른다. css는 html의 본문들을 꾸미고, 디자인하는 역할을 한다. 

style sheet으로는

* html tag안에 작성

~~~html
<span style="color:red;">hello</span>
~~~

* html head tag안에 작성

~~~html
<html>
  <head>
    <style>
      a:visited {
        color: pink;
      }
    </style>
  </head>
  	.
  	.
  	.
~~~

* html 파일 밖에 파일 형식으로 작성

~~~html
<html>
  <head>
	<link rel="stylesheet" type="text/css" href="ex1.css" /> 
  </head>
  	.
  	.
  	.
~~~


* 이 3개의 경우에 속하지 않는 경우 default

위에서 부터 차례대로 style이 적용이된다.

처음에 html안에 style을 관리함으로써 유지보수하기 힘들고 코드가 복잡해졌는데 css로 인하여 style 관리 문제점을 해결하였다.

### Syntax

3개의 part가 있다.

~~~css
Selector{ property : value }
~~~

* selector : style을 변경할 object를 가르킴
* property : style을 변경하고 싶은 속성을 가르킴
* value : 변경하고 싶은 속성에 값을 가르킴

~~~css
h1{ height : 100 }
~~~
> h1 tag의 내용을 높이 100으로 설정

Selector같은 경우, Type Selector, Class Selector, Id Selector, 동적 Selector등이 있다.

* Type Selector (tag를 selector로 지정)
   * ``` <p>, <body>  h1, h2, h3, h4 ```
    
* Class Selector (class를 selector로 지정)
   * Class 속성값 앞에 마침표를 추가함
   * .chapter 혹은 p.chaper
 
* Id Selector (id를 selector로 지정)
   * id 속성값 앞에 #를 추가함
   * #volume1

* 동적 Selector
   * hover(마우스를 올릴 경우), active(마우스를 누를 경우), visited(마우스를 이미 눌렀을 경우)
   * a:visited {color: red}


__Example__

* index.html
~~~html
<html>
<head>
<link rel="stylesheet" type="text/css" href="ex1.css" /> </head>
<body>
<h1>This header is 36 pt</h1>
<h2>This header is blue</h2>
<p>This paragraph has a left margin of 50 pixels</p>
</body> </html>
~~~

* ex1.css
~~~
body {background-color: yellow}
h1 {font-size: 36pt}
h2 {color: blue}
p {margin-left: 50px}
~~~

> 중요! html에서 class나 id naming을 잘 지정해줘야 css를 쉽게 작성할 수 있다.

### Margin & Padding

<img src="https://image-proxy-cdn.teamtreehouse.com/e4314d5c336cc352a806606bac61d4cffd46ae69/687474703a2f2f692e737461636b2e696d6775722e636f6d2f6e4e4b48682e676966"/>


* padding : content 와 border사이의 공백 거리
* margin : border 밖에 공백 거리

## 1.4 HTML5 (2014)

* Multimedia지원
It includes multimedia elements 
~~~
( <audio> and <video>)
~~~

* Websocket
양방향 통신 지원

## Reference

* 그림 : http://webdir.tistory.com/33 ,https://thebook.io/006946/ch01/02/01/01/
