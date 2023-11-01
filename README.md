# vite를 이용한 포트폴리오 사이트 만들기

## vite를 사용하는 이유
[vite](https://vitejs.dev/)

## 설치
1. npm create vite@latest
2. cd 폴더명
3. npm install
4. npm run dev
5. src폴더를 생성 src폴더안으로 index.html을 이동, assets폴더를 생성
6. vite.config.js를 생성
`export default {
    root: "src",
    build: {
        outDir: "../public",
    }
}`