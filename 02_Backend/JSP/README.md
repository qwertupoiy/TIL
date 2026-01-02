
---

## 1. jsp:param의 개념

`<jsp:param>`은 JSP에서 **페이지 간에 데이터를 전달할 때** 사용하는 태그이다.  
사용 위치에 따라 역할이 달라진다.

- `<jsp:include page="">` 와 함께 사용하면 → **변수를 받는 역할**
- `<jsp:forward page="">` 와 함께 사용하면 → **변수를 보내는 역할**

즉, 페이지 간 데이터 흐름을 제어할 때 활용된다.

---

## 2. jsp:param name="mode"의 의미

다음과 같이 사용할 수 있다.

```jsp
<jsp:param name="mode" value="edit">
<jsp:param name="mode" value="view">
```
mode는 페이지의 동작 모드(편집 / 보기) 를 지정하는 데 사용된다.

input 태그의 disabled 속성과는 다르며, 입력의 “제출” 조건에 영향을 주는 역할을 한다.

모드	설명
edit	편집이 가능한 상태
view	보기 전용 상태

## 3. 입력 관련 주요 이벤트 (JavaScript)

HTML 입력 요소에서 자주 사용하는 주요 이벤트와 **발생 시점**은 다음과 같다.

| 이벤트 | 발생 시점 |
|---------|------------|
| `keydown` | 키를 누르는 순간 |
| `keypress` | 글자가 입력되는 순간 |
| `keyup` | 키를 뗄 때 |
| `input` | 입력 값이 변할 때마다 |
| `change` | 값이 바뀐 뒤 포커스를 잃을 때 |
| `blur` | 포커스를 잃을 때 |
| `focus` | 포커스를 얻을 때 |
| `focusin` / `focusout` | 자식 요소에도 이벤트 전파 |
| `compositionstart` / `compositionend` | 한글 등 IME 조합 입력의 시작 / 끝 |

---

## 4. 참고 요약

- `<jsp:param>`은 JSP 페이지 간 **데이터 전달용 태그**이다.  
- `mode` 파라미터는 페이지 동작을 **보기(view)** 또는 **편집(edit)** 으로 제어할 수 있다.  
- JavaScript 입력 이벤트는 **사용자 입력 흐름을 제어하거나 검증할 때** 유용하게 사용된다.

---
