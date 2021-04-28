# Sass

### Sass 환경설정

    1. git 설정
      - github에서 repository 생성 / code의 HTTPS 경로 복사
      - cmd : 프로젝트를 저장할 경로로 이동 - git clone + HTTPS 경로

    2. node-sass 설치 & 설정

      - node-sass

        - node js 설치 with npm
        - npm init => package.json 생성됨
        - npm i node-sass => node_modules directory, package-lock.json이 생성됨
            ref : https://www.npmjs.com/package/node-sass
        - package.json에 script에 "node-sass" : "node-sass" 작성
        - npm run node-sass => node-sass가 실행됨
        - package.json에 script에 "sass" : "node-sass styles/main.scss ./style.css" 작성
            (node-sass [options] input [output] Or: cat input | node-sass > output,
            npmjs.com에 node-sass page에서 command line interface 부분을 확인)
        - npm run sass => sass가 실행됨(sass가 css로 변환하여 css파일이 생성됨)

      - Sass update
        - -w, --watch Watch a directory or file => main.scss의 변화 감지
        - -r, --recursive Recursively watch directories or files => 모든 파일변화 감지

    3. Sass-lint
      - VSCode SassLint extension 다운
      - npm i -D sass-lin : sass-lint 설치
      - .sass-lint.yml 파일추가

### Sass Variable
