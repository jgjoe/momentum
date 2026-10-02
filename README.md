# Momentum

**시계·인사말·날씨·할 일을 한 화면에 모은 개인 대시보드 — 바닐라 JS로 상태를 직접 관리했습니다**

[![JS](https://img.shields.io/badge/Vanilla%20JS-no%20framework-F7DF1E?logo=javascript&logoColor=black)](#기술-스택)
[![Storage](https://img.shields.io/badge/localStorage-persist-informational)](#설계-판단)

Momentum 확장 프로그램을 참고해 만든 개인 대시보드입니다.
로그인한 사용자 이름으로 인사하고, 시계·랜덤 배경·현재 위치 날씨·할 일 목록을 한 화면에 둡니다.

## 주요 기능

시계 · 사용자 인사말 · 랜덤 배경 · 랜덤 명언 · 현재 위치 날씨 · 할 일 목록(추가·삭제·유지)

## 설계 판단

- **데이터와 화면을 함께 갱신** — 할 일을 지우면 화면 항목과 배열을 같은 함수에서 함께 지우고 곧바로 저장해, 화면과 데이터가 어긋나지 않게 했습니다
- **새로고침해도 남게** — 사용자 이름과 할 일을 localStorage에 저장하고 시작할 때 복원합니다
- **비동기 API 호출** — Geolocation으로 좌표를 얻고 날씨 API를 호출하는 순서를 다뤘습니다
- **기능별 파일 분리** — 시계·인사말·할 일·배경·명언·날씨를 각각의 JS 파일로 나누고 CSS도 기능별로 분리해 서로 얽히지 않게 했습니다

## 기술 스택

HTML5, CSS3, Vanilla JavaScript, Web Storage API, Geolocation API

## 실행

`js/weather.js`의 `API_KEY`에 [OpenWeatherMap](https://openweathermap.org/api) 무료 키를 넣고,
`index.html`을 브라우저로 열어 이름을 입력하면 됩니다. 날씨는 위치 권한이 필요합니다.

> 클라이언트 전용 정적 페이지라 키가 브라우저에 노출됩니다. **사용량 제한이 걸린 무료 키만 사용하세요.**

## 만든 사람

**Jigwan Joe** — Frontend

- GitHub: [@jgjoe](https://github.com/jgjoe)
- Email: jigwan.joe@gmail.com
