# HTML5 기본 문법

## HTML5

> HTML(HyperText Markup Language)는 웹상에서 콘텐츠(content)를 구성(structure)하고 보여주기 위한 마크업 언어이다. → **HTML 태그를 통해서 정보를 구조화**
> 

### HTML5 이전

- **HTML**
- **XHTML**
    
    > eXtendible Hyper Text Markup Language의 약자로 HTML을 대체하기 위한 목적으로 만들어진 언어다. 기본적으로 HTML 문법을 따르지만 더 명확하고 구조적인 특징을 가지고 있다.
    > 
    - 특징
        1. 종료 태그가 없는 빈 태그는 스스로 종료
        2. 빈 태그를 제외한 

### HTML5 이후

| HTML | CSS | JS |
| --- | --- | --- |
| Markup Language | Style sheet Language | Programming Language |
| Content | Presentation | Behavior |

HTML5는 HTML 4.01, XHTML 1.1 등을 대체하는 HTML의 차세대 표준으로 아래 기능들이 추가되었다.

- **멀티미디어** - 플래시와 같은 플러그인의 도움없이 비디오 및 오디오 기능을 자체적으로 지원한다.
- **그래픽** - SVG, 캔버스를 사용한 2차원 그래픽과 CSS3, WebGL을 사용한 3차원 그래픽을 지원한다.
- **통신** - 서버와의 소켓 통신을 지원해서 서버와 양방향 통신이 가능하다.
- **디바이스 접근** - 카메라, 동작센서 등의 하드웨어 기능을 직접적으로 제어할 수 있다.
- **오프라인 및 저장소** - 오프라인 상태에서도 애플리케이션을 동작시킬 수 있다.
- **시맨틱 태그** - 브라우저, 검색엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명할 수 있다. HTML 요소의 의미를 명확히 해석하고 그 데이터를 활용할 수 있는 시맨틱 웹을 실현할 수 있다.
- **CSS3** - HTML5는 CSS3를 완벽하게 지원한다.

## HTML5 문서의 기본 구조

- 문서의 시작이 반드시 `<!DOCTYPE html>` 로 되어야 한다.
- 실제적 HTML document는 `<html>` 과 `</html>` 태그 사이에 기술한다.
- `<head>` 와 `</head>` 사이에는 document title, 외부 파일 참조, 메타데이터의 설정 등이 위치하며 이들은 브라우저에 표시되지 않는다.
- 웹 브라우저에 출력되는 요소는 모두 `<body>` 와 `</body>` 사이에 위치한다.

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Hello World</title>
	</head>
	<body>
		<h1>Hello</h1>
	</body>
</html>
```

- 문자셋의 선언이 간결해졌다.
    - 기존 -  `<meta http-equiv="Content-Type" content="text/html; charset=utf-8">`
    - HTML5 - `<meta charset="utf-8">`
- HTML 문서는 메모장, `vi` , IDE 등을 통해서 작성이 가능하다.
- HTML 문서는 `.html` 확장자를 갖는 순수한 텍스트 파일이다. → 웹 브라우저에서 바로 확인이 가능하다.

## HTML5 기초 문법

### 1. 요소(Element)

- **구성**
    - `<tagname>` - 시작 태그(start tag, opening tag)
    - `</tagname>` - 종료 태그(end tag, closing tag)
    - content - 태그 사이에 위치
    - 예외
        - `<img>`, `<br>` , `<hr>` 등과 같이 종료 태그 없이 시작 태그만을 가지는 태그를 빈 태그(empty tag)라고 한다.
- 태그는 대소문자를 구별하지 않으나 소문자를 사용하는 것이 일반적이다.

### 1.1 요소의 중첩(Nested Element)

- 요소는 다른 요소를 포함할 수 있다.
- 부자 관계가 성립되어 정보를 구조화하여 웹페이지의 구조를 표현한다.
- 부자 관계를 시각적으로 파악하기 쉽도록 **들여쓰기**를 활용한다.

### 1.2 빈 요소(Empty Element)

> content를 가질 수 없는 요소
> 
- `br`
- `hr`
- `img`
- `input`
- `link`
- `meta`

### 1.3 속성(Attribute)

> 요소의 성질, 특징을 정의하는 명세
> 
- 요소는 속성를 가질 수 있다.
- 속성는 요소에 추가적인 정보를 제공한다.(Ex. 이미지 파일 경로, 크기 등)
- 속성는 시작 태그에 위치해야 하며 이름/값(Arguments)으로 쌍을 이룬다.

```html
<p color="red"> 정수연 </p>
```

- **글로벌 어트리뷰트**
    
    > 모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트
    >