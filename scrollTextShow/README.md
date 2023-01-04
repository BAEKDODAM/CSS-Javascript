# scroll 실행되면 글자가 보이는 animation

## 스크롤을 부드럽게

`scroll-behavior: smooth`
- 스크롤을 부드럽게 만들어줌

## 스크롤 시 새로운 컴포넌트 나타나게
`IntersectionObserver()`
- 내가 원하는 특정 html 요소가 화면에 등장하는지 감시
- `<div>`가 현재 화면에 보이는지 파악 
쉬워짐
- `let observer = new IntersectionObserver((e)=>{}`
IntersectionObserver 함수 안에 감시중인 박스가 화면에 등장하면 실행할 코드 작성 (e는 현재 감시중인 모든 박스(div 등))
