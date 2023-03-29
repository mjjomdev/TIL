# 개발 관련

## Web API

### View Transitions API

- 화면 전환 효과를 제공하는 API다.
- HTML에 `<meta name="view-transition">`을 설정하는 것만으로도 기본 옵션(fade)으로 동작한다.
- 이전 페이지와 새 페이지의 스크린샷을 찍고 비교하는 방식이다.
- CSS를 활용해서 효과를 커스텀할 수 있다. 자세한 내용은 [mdn](https://developer.mozilla.org/en-US/docs/Web/API/View_Transitions_API) 참고

## HTML

### `<noscript></noscript>`

- 페이지에서 스크립트를 지원하지 않거나 브라우저가 스크립트를 비활성화한 경우 보여지는 HTML 구문이다.
- <head> <body> 두 곳 모두에서 정의될 수 있지만 <head>에 속하면 <link>, <meta>, <style> 요소만 포함된다.
