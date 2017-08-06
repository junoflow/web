# 170728 WEB 개발하기
# 3 - 레이아웃 만들기 (1)

## head 부분

```
  <!DOCTYPE html>
  <html>
  <head>
    <title>예제용 파일</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> //한글입력 
    <style type='text/css'>
      body {
        margin: 0; // html에서 기본적으로 제공하는 margin 값을 없앰
      }
      a {
        color: #000000;
        text-decoration: none; // a 태그에서 밑줄이 지워짐
      }
     #wrap {
        width: 800px; // 가로 길이
        margin: 0 auto; // 사이트를 가운데 정렬
 
        //margin없이
        position: relative;
        Left: 50%;
        margin-left: -480px;
 
        background: #cccccc;
     }
    #header {
      background: #eeeeee;
      padding: 20px;
    }
    #header .logo {
      float: left;
    }
    #content {
      padding: 20px;
    }
    #content img {
      width: 100%; // padding값을 제외하고 이미지가 꽉 차게
    }
    #footer {
      background: #000000;
      height: 90px;
      text-align: center;
      padding: 20px;
    }
    #footer span {
      color: #ffffff;
    }
    .clear {
      clear: both;
    }
    </style>
</head>

```

### 주요 포인트
- ```<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />``` : 한글로 만들어진 웹페이지임을 알림
  - http-equiv : "웹브라우저에게 정보를 전달한다"
- #wrap 을 가운데 정렬하는 방법에는 두 가지 방법이 있다
  - margin과 auto를 이용하는 방법
  - position:relative를 이용하는 방법
  
## body 부분

```
<body>
  <div id="wrap"> // 전체적인 컨텐츠를 감싸주는 역할
  <div id="header"> // 하나만 등장하는 건 id
    <span><img src="img/logo.png" alt="사이트 로고"></span> //alt는 접근성을 위해 꼭 필요
    <h1>CSS 활용강의</h1>
    <h2> 레이아웃 1 - 단일 레이아웃 만들기</h2>
    <div class = "clear"></div> // 반복적으로 사용하는 건 class
    </div>
  <div id-"content">
    <h3>레이아웃을 만드는 방법</h3>
    <img src="img/bg1.jpg" alt="배경이미지>
    <p>텍스트</p>
  </div>
  <div id="footer">
    <span>아래붙는텍스트</span>
  </div>
</div>
</body>
</html>

```

### 주요 포인트
- img에서 alt는 이미지 대신 쓸 수 있는 텍스트가 들어가야 한다.
[참고사이트](http://html5ref.clearboth.org/doku.php?id=html5:attribute:alt_img)
- clear처럼 반복적으로 사용되는 건 class로 선언하고, wrap처럼 한 번만 사용되는 건 id로 선언
- span을 쓰고나서는 꼭 clear를 뒤에 써야 레이아웃이 망가지지 않는다
