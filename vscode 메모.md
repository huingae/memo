# vscode 메모

###  기본세팅

#### package 다운받기

1.Increment Selection(숫자 자동변환:ctrl + alt + I)

2.px to rem(px을 rem으로 자동 변환:Alt+Z)

3.Bracket Pair Colorizer 2 (같은 묶음을 찾아서 같은 컬러로 표현)

4.material icon theme(아이콘 테마)

5.browsersync-jeremy rajan(브라우저싱크)

#### 기본세팅

setting- tab size:2 , zoom:on

#### html 단축키 만들기-user-snippets

설정아이콘-usersnippet-html-설정 뒤 저장

``` html
	  "Print to console": {
		"prefix": "lee",
		"body": [
		"<!DOCTYPE html>",
    "<html lang=\"ko-KR\">",
    "<head>",
    "<meta charset=\"UTF-8\">",
		"<meta http-equiv=\"X-UA-Compatible\" content=\"IE=edge\">",
		"<meta name=\"viewport\" content=\"width=device-width, user-scalable=yes, initial-scale=1.0, maximum-scale=3.0, minimum-scale=0.5\">",
		
		"<!-- <link rel=\"stylesheet\" href=\"../fonts/\"> -->",
    "<link rel=\"stylesheet\" href=\"../css/base/reset.css\">",
    "<link rel=\"stylesheet\" href=\"../css/base/common.css\">",
    "<link rel=\"stylesheet\" href=\"../css/src/common.css\">",

    "<!--[if IE]>",
    "<script src=\"./ie/html5shiv/dist/html5shiv.min.js\"></script>",
		"<script src=\"./pie/PIE.js\"></script>",
		"<script src=\"../ie/respond/dest/respond.min.js\"></script>",
		"<![endif]-->",
		
		"<title>Document</title>",
		"</head>",
		"<body>",
		
		"<!-- layout -->",

		"<!-- script -->",
		"<script src=\"../js/base/jquery-3.5.1.min.js\"></script>",
		"<script src=\"../js/base/jquery-ui.min.js\"></script>",
		"<script src=\"../js/src/\"></script>",

		"</body>",
		"</html>",
		],
	
		"description": "html 기본 형식 설정"
}
```



### 단축키

선택: shift

숫자 바꾸기: 선택 이후 ctrl+alt+i

랩핑: 코드선택 - ctrl+shift+p - 문법입력(ex:a,span...)

터미널 열기: ctrl+`  (git으로 변경하여 사용)

source control: git에 바로 올리기 기능

emmet: li*5{box_0$}