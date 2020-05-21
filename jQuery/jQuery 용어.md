# jQuery 용어

```js
//기본형태
var 변수 = function(인수){인자});
변수(매개변수);
```



변수.**api용어** ( );

- html, text

  - html :html내용을 확인,코드의 내부를 삭제 및 변경 

  - text: 문자(텍스트)내용 확인,코드 내 글자를 삭제 및 변경

  - ```js
    var gnbBox = $("#gnbBox");
    var gnblist = gnbBox.find("li"); 
    var gnbLen = gnblist.length;
    
    	var i = 0;
    	var gnblistText;	
    
    	for(; i<gnbLen; i++){
    		gnblistText = gnblist.eq(i).text();
    		gnblist.eq(i).html('<a href="#">'+gnblistText+'</a>');
    	}
    // for문 안에 var가 들어가면 이상하기 때문에 변수선언(var gnblistText)을 먼저 해준 뒤 값을부여한다.
    ```

    

- wrap, contents

  - wrap: 감싸는 영역을 생성, 그 자체의 내용을 확인
  - contents: 내용요소를 확인-코드+글자 포함

- prepend, prependTo / append, appendTo,

  - 선택자 내부의 앞/뒤요소에 추가요소를 담는 기능

   ```js
  headBox.prepend(h1); //headBox의 내부의 앞에 h1을 옮겨담아라h1.prependTo(headBox); //h1을 headBox 내부의 앞에 옮겨담아라
  To를 쓰는 것은 주어와 목적어가 바뀔 뿐 
  
  gnbBox.prepend('<div class="gnb_btn"><button type="button">메뉴</button></div>'); 
  태그를 입력할 시 직접 만들어낼 수도 있음
   ```

    

- before, after

  - 앞 뒤에 형제요소를 만드는 기능

- attr, val

  - attr:속성값을 확인, 지정속성을 변경하는 기능
  - val: form요소 내부의 value 값을 확인/변경

- remove, empty

  - remove: 선택요소자체를 삭제
  - empty: 선택요소 내부를 비우는 기능

- clone

  - 선택요소를 복제, 'true' 를 함께 사용하면 내용 요소의 기능포함 복제

- addClass, removeClass

  - class이름 값을 추가/삭제

- hasClass

  - 선택요소에 해당클래스 이름의 유무를 판단 

- is

  - 선택요소에 class를 제외한 속성의 유무를 판단 

  ------

- width, heihgt, innerWidth, outerWidth

- scrollTop, offsetTop

- css, animate

- show, hide, fadeIn, fadeOut, slideDown, slideUp

https://oscarotero.com/jquery/ 이밖의 jQuery 용어가 나와있는 사이트

