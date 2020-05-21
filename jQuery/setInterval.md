# setInterval

### setInterval(function( ){ },시간)

주기성, 일정시간마다 { 기능 }을 수행

clearInterval을 사용하기 위해서는 변수화를 해준다.

##### clearInterval ()

setinteval을 취소하기

```js
var t = setInterval(function( ){ },시간)  //변수화
변수.on("mouseenter",function(){
    clrearInterval( t );
});//변수에 마우스를 올리면 t(setInterval의 변수)이 사라진다.
```

##### requestAnimationFrame( 수행내용  )

1. 1ms마다 움직임
2. 자원(데이터)관리: 사용하지 않을때는 동작하지 않는다

##### setTimeout(function(){ },시간) 

일회성, 일정시간 뒤에



### 예시



```js
var i = 0 // 바깥에 변수를 선언해준다.
	setInterval(function(){
		i += 1; //0(바깥에서 i로 선언해준 수)에 1을 더한 상태가 계속 된다

		if(i >= addViewList.length){i = 0}//갯수만큼의 순서가 지나면 다시 처음으로 돌아간다

		AdViewMv(i);
	}, timed*4 );
```



**마우스 올리면 멈추고 떼면 다시 움직이는 기능**

```js
var startA;//미리 변수 선언
var MvSet = function(){ //MvSet은 startA의 기능을 가진 변수이다
	startA = setInterval(function(){
		i += 1; //0에 1을 더한 상태

		if(i >= addViewList.length){i = 0}
        //i가 li개수보다 크거나 같다면
        //갯수만큼의 순서가 지나면 다시 처음으로 돌아간다

		AdViewMv(i);
	}, timed*2 );
};

MvSet();// setInterval 기능이 있는 변수를 실행시켜준다


	$('#viewBox').on('mouseenter', function(){
		clearInterval(startA);
	});//viewBox에 마우스를 올릴 시 startA라는 기능은 사라진다

	$('#viewBox').on('mouseleave', function(){
		MvSet();
	});//마우스가 떠나면 변수 MvSet은 실행된다
	
```

