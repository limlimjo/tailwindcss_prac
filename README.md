## TailwindCSS 학습

- TailwindCSS 강의를 들으며 학습한 내용을 정리하였습니다.

### TailwindCSS 설치

- 학습할 때는 CDN을 사용

```html
<script src="<https://cdn.tailwindcss.com>"></script>
```

- 그외 방법은 [TailwindCSS 공식문서](https://tailwindcss.com/docs/installation) 참고

---

### TailwindCSS 기초

1. Typography 스타일링

- 폰트 크기 조절: `text-sm`, `text-lg`, `text-xl`
- 폰트 두께 설정: `font-light`, `font-normal`, `font-bold`
- 텍스트 정렬: `text-left`, `text-center`, `text-right`
- 라인 높이 조절: `leading-none`, `leading-normal`, `leading-loose`
- 텍스트 색상: `text-black`, `text-gray-500`, `text-blue-600`

2. 컬러 및 배경, 보더 처리

- 배경색 설정: `bg-white`, `bg-gray-100`, `bg-blue-500`
- 텍스트 색상 설정: `text-gray-500`, `text-blue-600`
- 보더 스타일 설정: `border`, `border-2`, `border-gray-300`, `rounded-lg`, `rounded-full`

3. 간격 조절 (Margin, Padding, Spacing)

- 패딩 설정: `p-4` (모든 방향에 1rem 패딩 적용), `px-4` (좌우에만 1rem 패딩 적용)
- 마진 설정: `m-4` (모든 방향에 1rem 마진 적용), `mt-4` (상단에만 1rem 마진 적용)
- 요소 간의 공간 조정: `space-x-4` (좌우 1rem), `space-y-4` (상하 1rem)

4. Utility-First CSS

- Utility-First CSS (유틸리티-우선 접근 방식)는 미리 정의된 작은 유틸리티 클래스들을 사용하여 HTML 요소에 스타일을 직접 적용하는 방식임

- TailwindCSS의 장점<br/>
  : 클래스 이름 발명의 필요성 없음<br/>
  : CSS 파일 확장 방지<br/>
  : 안전한 변경 (HTML 내에서 로컬로 작용하므로)

---

### 레이아웃 시스템 이해

1. 컨테이너(Container)

- `container` 클래스는 웹 레이아웃에서 콘텐츠 영역을 깔끔하게 정리하고 중앙에 배치하는 데 주로 사용됨
- 컨테이너는 웹 페이지에서 콘텐츠가 화면 크기에 맞춰 잘 정리되도록 도와줌
- 컨테이너 속성 값<br/>
  : `sm` (최대 너비: 640px)<br/>
  : `md` (최대 너비: 768px)<br/>
  : `lg` (최대 너비: 1024px)<br/>
  : `xl` (최대 너비: 1280px)<br/>
  : `2xl` (최대 너비: 1536px)

2. Flexbox와 Grid 레이아웃

- Flexbox는 수평 및 수직 정렬을 위한 CSS 레이아웃 모델임
- 주요 Flexbox 유틸리티 클래스<br/>
  : `flex` (Flexbox 컨테이너 활성화함)<br/>
  : `justify-start`, `justify-center`, `justify-end` (아이템을 수평으로 정렬)<br/>
  : `items-start`, `items-center`, `items-end` (아이템을 수직으로 정렬)<br/>
  : `gap-x-N`, `gap-y-N` (Flexbox 아이템 간의 간격 조절)

- Grid는 복잡한 2차원 레이아웃을 구성하기에 적합한 CSS 레이아웃 시스템임
- 주요 Grid 유틸리티 클래스<br/>
  : `grid` (Grid 레이아웃을 활성화함)<br/>
  : `grid-cols-N` (Grid 컨테이너에 N개의 열을 지정함)<br/>
  : `gap-x-N`, `gap-y-N` (Grid 아이템 간의 수평 및 수직 간격을 설정함)

3. 포지션(Position)

- Position-`fixed`
  : `fixed`는 요소를 뷰포트에 고정하여, 스크롤 시에도 해당 요소가 고정된 위치에 머무르도록 함

- Position-`sticky`
  : `stickey`는 스크롤할 때 요소가 지정된 위치에 도달하면 고정되며, 그 이후에는 부모의 요소의 끝에 도달할 때까지 고정된 상태를 유지함

---

### 반응형 디자인

1. 반응형 디자인 기초

- TailwindCSS는 미디어 쿼리를 사용하지 않고, 미리 정의된 브레이크포인트 유틸리티를 통해 손쉽게 반응형 디자인 구현 가능

- Tailwind의 반응형 유틸리티를 사용하기 전에 반드시 메타 태그를 아래처럼 추가해줘야함

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- TailwindCSS는 모바일 우선 접근 방식 사용함. 이는 브레이크포인트가 없는 기본 유틸리티가 모바일 장치부터 모든 화면 크기에 적용된다는 뜻임

2. 반응형 디자인 실습

- github 실습 코드 참고

---

### Transition & Animation

1. 트랜지션 효과

- 트랜지션은 CSS에서 요소가 상태(값)를 변경할 때, 그 변화를 일정 시간 동안 부드럽게 처리하는 애니메이션임

- 관련 속성 사용법은 [TailwindCSS 공식문서](https://tailwindcss.com/docs/installation) 참고

2. 애니메이션 효과

- 애니메이션은 요소가 시각적으로 움직이거나 변화하는 것을 말함

- 관련 속성 사용법은 [TailwindCSS 공식문서](https://tailwindcss.com/docs/installation) 참고

---

### 다크 모드

- 다크 모드는 현대 운영 체제에서 기본적으로 제공하는 기능으로 TailwindCss를 사용하면 손쉽게 스타일링 가능

- github 실습 코드 참고

---
