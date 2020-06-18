# scss

#### 주석

//  : 한줄주석 (css로 변환했을때 보이지 않음)<br>/* */ :여러줄 주석 (css와 동일한 내용을 담는다.)

scss에서 작업한 것은 css로 변환이 되지만 css에서 scss로의 변환은 불가능하다.



#### 외부파일 불러오기

-@import url(); : css에서 사용하는 기법, 파일까지 같이 가져간다.

-@import " ";  : scss에서 사용하는 기법, 내용을 내장해서 변환.

scss 파일명 앞에 _를 붙이면 암묵적(숨김)파일이 된다.(css로 변환하지 않는다): scss변수 데이터를 넣어두는 용

```
@import"../setting/_variable.scss"; 혹은
@import"../setting/variable";의 형태로 불러옴(대체로 후자 사용)
```



#### 변수 사용하기

사용하려는 기능을 변수로 만들어 사용할 수 있다.

**$변수이름 : 사용하려는기능;**

지정된 변수를 다른 곳에서 추가로 불러와서 변수로 할당할 수 있다.

```
$color : #fff;
$l1 : 1px;
$line : l1 solid #color;
```



#### 컬러 설정하기

-darken(색상, 값%);

-lighten(색상, 값%);

-rgba(색상, 투명도);

-hsla(색상, 투명도);

특정색상을 어둡게 하거나 밝게 할 수 있고,<br>css와 달리 rgb코드를 입력하지 않고 헥사코드를 입력해도 투명도 조절이 가능하다

변수를 활용하면 더욱 편리한 사용이 가능하다



#### 계산기능

-width : 100 / 3 + %;

-width : 30 / 340 * 100 + %;

calc에서 사용하던 기법을 calc없이 직접입력으로 사용가능

일부기능에서는 calc보다 더 원활하게 동작하지만,<br>무조건 동작하지는 않으므로 신중한 사용이 필요함



#### 중첩기법(nesting)

괄호 안에 하위태그를 중첩하는 것으로 코드를 줄일 수 있다.

```
#gnb{width:100%; height:100%;
	>h2{width:100px; height:100px;
		>a{display:block;
		>span{text-align: center;}
		>a:hover >span{color:#aaa;}
		}//a
	}//h2
}//gnb
```

중첩기능 시 4단계 이상은 사용하지 않는다.

시인성이 떨어지면 사용하지 않는다

끝나는 곳에는 반드시 주석으로 표기한다.



#### list기법

$li : (0,1,2,3,4);

$li : ($primary, $sub1, $sub2, $black);

​	해당하는 순서의 값을 쓰기위해서 리스트로 처리

​	nth(변수, 순서값): 해당변수의 순서번째의 값을 사용

​	length(변수) : 리스트 형식의 변수 갯수를 파악

​	for문과 함께 사용하기에 편리함

​	

#### @for

@for $i  from 1 **to** 10 {} :변수 i를 1부터 9까지(작다의 의미)

​	= js의   for(var i =0; i<10){}   와 동일

@for $i from 1 **through** 6 {} :변수 i를 0부터 6까지(작거나 같다의 의미)



```
$li:('grape','apple','tomato','banana','strawberry');
@for $i from 1 through length($li){
 .#{nth($li,$i)}_coffe {color:#fac;}  //선택자 사용시 순서를 입력할때는 보간법(#{변수}의 모양으로 처리)을 사용한다.
}
```

