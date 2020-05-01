#### border-radius

border-radius: 전체를 준다

border-top-left/right-radius: 위(top)을 기준으로 왼쪽/오른쪽에 r값을 준다

border-bottom-left/right-radius : 아래(bottom) 기준으로 왼쪽/오른쪽에 r값을 준다

boder-radius:50% -원형

직사각형에 50%를 주면 타원이 되기 때문에 50px을 준다.

##### text-indent

한줄 들여쓰기

##### css appearance속성

##### box-shadow

box-shadow: X값 이동치/ Y값 이동치/ 번짐의정도 / 부피의크기(잘 사용x)/색상

box-shadow:inset <-  그림자 내부로 표현

#### transform

1.이동-translate 

2.크기변경-scale

3.회전-rotate

4.기울이기-skew

단위:이동-px | rem | % ...

​		크기-1==100% , 0.5==50%, 3==300%

​		회전-deg(각도)

조건:block요소여야 한다, float기능이 되었을때는 일부 동작하지 않는것이 있다

축: x | y | z -대부분x축을 기본으로 처리( 회전은 z축(가운데)을 기본으로 한다)

perspectie:부모요소에 적용하는 원근법 요소(z축 이동을 사용하기 위해)

transform-origin:축의 기본위치를 변경;



#### gradient 그라데이션

background-image: 해당기능();

1.inear-gradient (각도, 색1 위치, 색2 위치, 색3 위치 ...)

2.radial-gradient([circle | closeset-side] at 위치, 색1 위치, 색2 위치, 색3 위치....)

3.repeating-[형태(linial | radial)]-gradient(내용은 위 두기능과 동일)

이미지를 대체하는 기능으로 인지



##### filter

그래픽툴의 기능을 대신해준다

아직 IE에서는 사용하지 않는다.

