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
        - --source-map true => stylesheet의 변화를 sass파일로 알려줌

    3. Sass-lint
      - VSCode SassLint extension 다운
      - npm i -D sass-lin : sass-lint 설치
      - .sass-lint.yml 파일추가

### Asset image

    1. Images
      1.1 Vector Images(최근 권장)
        - svg(Scalable Vector Graphics) ex) Icon
            - 사이즈 축소확대와 상관없이 깨지지 않는 이미지를 제공
            - 파일사이즈가 픽셀사이즈와 상관없이 일정
            - ie 6 7 8 (x)
            - site Logo와 같이 중요한 이미지는 svg로 권장
        => 사이즈에 상관없이 사용하고 싶을 때

        - webP

      1.2 Raster Images(확대했을 경우 깨짐)
        - png
            - 투명한 배경 가능
            - 이미지의 퀄리티 손실이 거의 없음
            - 용량이 크다.

        - jpg
            - 압축이 잘 된다 = 용량이 작음 = 퍼포먼스 좋아짐
            - 이미지의 풍부한 표현이 덜함, 퀄리티가 상대적으로 떨어짐
            - : 투명한 배경 지원하지 않음

        => target에 따라 (퍼포먼스가 우선인가 이미지 퀄리티가 우선인가)
          ex) apple.com ,ohouse

      #issue
        하나의 웹사이트에 리소스 용량 50-60%를 차지하는 이미지
        용량파일이 크다? = 랜더링할때 오래걸린다 = 사용성이 구리다.
        퍼포먼스에 해를 끼치지 않는 이미지를 찾아서 사용해야!

    2. Figma
      - Figma image 바꾸는 단축키 : ctrl + R -> rename to 작성
        ex) image-user, image-recommendation, img-review, img-product
      - 이미지 파일 저장 : assets / images

    3. svg -> Icon Font 생성
      site : https://icomoon.io/app/#/select
      import Icons click - upload - select All - 하단에 generate Font - 하단에 download하기전에 setting 하기

      다운받은 icon font - fonts파일에 fonts파일 옮기기 - style.css 옮기기

    4. Favicon 넣기
      site : https://realfavicongenerator.net/
      select your favicon image - 업로드 - Generate yout Favicons and HTML code
      code 복사 붙혀넣기 - root에 favicon asset 옮겨넣기

ref: https://edu.goorm.io/lecture/25681/%EA%B9%80%EB%B2%84%EA%B7%B8%EC%9D%98-ui-%EA%B0%9C%EB%B0%9C-%EB%B6%80%ED%8A%B8%EC%BA%A0%ED%94%84-%EA%B2%BD%EB%A0%A5%EA%B0%99%EC%9D%80-%EC%8B%A0%EC%9E%85%EC%9C%BC%EB%A1%9C-%EB%A0%88%EB%B2%A8%EC%97%85
