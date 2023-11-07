# vite를 이용한 포트폴리오 사이트 만들기

## vite를 사용하는 이유
[vite](https://vitejs.dev/)
"Vite"는 JavaScript 프레임워크와 빌드 도구입니다. Vite를 사용하는 이유는 다음과 같습니다.
<details>
<summary>더보기</summary>

1. 빠른 개발 환경 제공: Vite는 개발 중에 신속한 환경을 제공합니다. 빠른 빌드 시간과 빠른 개발 서버를 통해 빠른 개발을 도와줍니다.

2. 모듈 번들링: Vite는 모듈을 필요로 하는 프로젝트에서 각 모듈을 빠르게 번들링할 수 있습니다. 이는 빠른 로딩 속도와 효율적인 번들링을 가능하게 합니다.

3. 다양한 프레임워크 지원: Vite는 다양한 프레임워크와 라이브러리 (예: Vue.js, React, Svelte 등)와 함께 사용할 수 있습니다.

4. Hot Module Replacement (HMR) 지원: HMR은 코드 변경을 감지하고 새로고침 없이 모듈을 교체하여 개발자가 빠르게 개발할 수 있도록 도와줍니다.

5. 플러그인 시스템: Vite는 다양한 플러그인을 지원하여 프로젝트의 요구에 따라 확장할 수 있습니다.

6. 타입스크립트 지원: Vite는 타입스크립트를 기본적으로 지원하며 타입 안정성을 유지하면서 개발할 수 있습니다.

7. 웹 앱 최적화: Vite는 프로덕션 빌드를 위한 최적화 도구를 제공하여 더 작고 빠른 앱을 만들 수 있습니다.

8. 빠른 첫 화면 로딩 (Fast Initial Load): Vite는 첫 화면 로딩 속도를 빠르게 만들어 사용자 경험을 향상시킬 수 있습니다.
</details>

## 구현 기능
1. [구글폰트](https://fonts.google.com/)
    - 구글 폰트 적용
2. [Lenis](https://lenis.studiofreight.com/)
    - smooth 효과 적용
3. [GSAP](https://gsap.com/)
    - GSAP를 이용한 가로 효과
4. [Javascript]
    - Javascript 메뉴 클릭 이동 효과
    - JavaScript 모듈 기능 적용
5. [기타]
    - 웹표준 준수를 위한 스킵 메뉴 및 aria, role 적용
    - vite 빌드 작업 `npm run build`
    - netilfy 배포 작업

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

## Github 페이지 주소 생성
1. Settings -> Pages에서 Branch에서 none을 main으로 변경

## 트러블 슈팅
[403에러](https://beagle-dev.tistory.com/244#google_vignette)
- Unable to access 'https://github.com/github_id/git_reposit_name.git'/ The requested URL returned error: 403
1. 인증하기
    1. git remote set-url origin "https://github-username@github.com/github-username/github-repository-name.git" 를 입력해주세요.
    2. github-username 에는 본인이 github 에서 사용하는 username 을 적으시면 되고 github-repository-name 에는 git reposit 이름을 입력하시면됩니다.. “” 큰따음표는 제거해야합니다.
    3. 제일 처음에 git remote add origin git_reposit_주소.git 을 통해 origin 명칭을 만들었지만 해당 주소에 대한 권한이 없어서 푸쉬를 할 때 에러가 납니다.

2. 소스코드 푸쉬하기
    1. 터미널에서 git push -u origin master 를 입력합니다.
    2. 깃헙 패스워드 입력을 하라는 창이 나오고 입력을 하시면 본인의 깃주소에 소스코드가 올라갑니다.
    3. 인증이 끝난 후부터는 git push만 하면 기존의 세팅한 주소로 바로 푸쉬가 됩니다. 변경을 원하시면 git remote "set-url" "any_name" "git_reposit_주소"를 사용하시면 됩니다.

- Window에서 Github 자격증명 토큰 설정하기
1. 제어판 - 사용자계정 - Windows 자격 증명 관리자 탭으로 이동
2. git:https://github.com의 자격정보를 찾아 편집버튼을 클릭
3. 암호에 발급된 access token을 붙여넣고 저장