# 개발 관련

## Web API 

### View Transitions API

- 화면 전환 효과를 제공하는 API다.
- HTML에 `<meta name="view-transition">`을 설정하는 것만으로도 기본 옵션(fade)으로 동작한다.
- 이전 페이지와 새 페이지의 스크린샷을 찍고 비교하는 방식이다.
- CSS를 활용해서 효과를 커스텀할 수 있다. 자세한 내용은 [mdn](https://developer.mozilla.org/en-US/docs/Web/API/View_Transitions_API) 참고

### Crypto

- 외부 모듈 없이 UUID를 생성할 때 활용할 수 있다.
- 모던 브라우저: `randomUUID()`
- IE11: `getRandomValues()`
- IE10 이하: 지원 가능한 Crypto 메서드가 없어 대안으로 `Math.random()`을 활용한다. 다만, `Math.random()`은 암호학상 안전하지 않아 timestamp, string 등을 조합해서 중복 가능성을 낮출 수 있다.

### CustomEvent

- `Event()` 생성자와 동일하지만 커스텀을 명시적으로 나타낼 수 있고 두 번쨰 인수로 이벤트에 대한 옵션을 디테일하게 설정할 수 있다는 차이
- 이벤트 버블링을 활성화하기 위해서는 옵션으로 `bubbles: true`를 반드시 넘겨야 한다.
- [JavaScript Info](https://ko.javascript.info/dispatch-events) 참고

## HTML

### `<noscript></noscript>`

- 페이지에서 스크립트를 지원하지 않거나 브라우저가 스크립트를 비활성화한 경우 보여지는 HTML 구문이다.
- `<head>` `<body>` 두 곳 모두에서 정의될 수 있지만 `<head>`에 속하면 `<link>`, `<meta>`, `<style>` 요소만 포함된다.

### Programming Language (feat. Markup Language)

- 컴퓨터에게 일을 시키기 위한, 컴퓨터 시스템을 구동시키는 소프트웨어를 작성하기 위한 언어.
- 메모리에서 데이터를 읽고, 데이터에 대한 조건부 논리를 제공하고, 반복적으로 논리를 실행하는 프로그래밍이 가능해야 한다.
- HTML은 프로그래밍 언어인가? No, 마크업 언어다. (= 문서/데이터 구조를 표현하는 언어)

### inert 속성

- 비활성화 하고싶은 요소에 적용할 수 있다. disabled 속성이나 CSS로 핸들링하는 것보다 접근성 측면에서 낫다.
  - 단, disabled처럼 CSS를 바꿔주지는 않음
  - 참고 링크: [HTML 요소 inert 속성에 대해 알아보자](https://ui.toast.com/posts/ko_20220603)

### contenteditable 속성

- textarea나 input처럼 사용자가 텍스트를 입력, 수정할 수 있도록 하는 요소다.
- textarea나 input과 달리 텍스트뿐 아니라 이미지, 비디오, HTML 코드 등 다양한 유형을 편집할 수 있고 유형이 다양하니 복잡도가 높은 내용도 편집할 수 있다는 차이가 있다.
- 보안상 취약할 수 있어 사용자의 입력 데이터를 검증하고 보안 처리하는 후처리가 필요할 것 같다.
