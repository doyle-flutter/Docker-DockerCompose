# Docker 🐳

많은 내용 및 옵션이 있지만 자주 쓰일 명령어만 모아놨습니다,


Docker [설치](https://www.docker.com/get-started) (+ DockerHub 가입까지)


  0. 이미지 다운로드
  
  <code> $ docker pull ubuntu:18.04 </code>

  1. 이미지 확인

  <code> $ docker images </code>

  2. 이미지 및 컨테이너 실행

  <code> $ dockr run -dit -p --name myu -p 3000:80 ubuntu:18.04 </code>

  3. 확인

  <code> $ docker ps </code>

  <code> $ docker ps -a </code>

  <code> $ docker network ls </code>

  4. 컨테이너 중지 / (재)실행 / bash 전달  / bash 연결

  <code> $ docker stop [NAME] </code>

  <code> $ docker start [NAME] </code>

  <code> $ docker exec [NAME] ls </code>

  <code> $ docker attach myu </code>
  
  5. 컨테이너 삭제

  <code> $ docker rm [NAME] </code>

------

  1. 이미지로 실행 한 컨테이너에서 작업 후 다시 이미지로 만들기

  <code> docker commit -a "readme" [:ContainerID] [:ImageName]/[:TagName] </code>

  <code> $ docker commit -a "sudo, curl, nodeLTS(v14), nano" [:ContainerID] [:ImageName]/[:TagName] </code>

  <code> > sha256 ...  내용이 뜨면 정상 </code>

  2. 허브에 푸쉬하기 위해 로그인

  <code> $ docker login </code>

  3. 태그 명 변경하기( 푸쉬 이미지명과 아이디를 일치 )

  <code> docker tag 기존이미지명:[태그] 원하는_이미지_명:[태그] </code>

  <code> $ docker tag [:prevContainerName]:[prevTagName] [:newContainerName]:[:newTagName] </code>

  4. 허브에 푸쉬하기 ( 허브 [ 레포 🔗 ](https://hub.docker.com/repository) )

  <code> docker push [허브_아이디]/이미지명:[태그] </code>

  <code> $ docker push [:newContainerName]:[:newTagName] </code>

------

### 기본 설정 후 배포한 Ubuntu 14.08 Image [ 🔗 ](https://hub.docker.com/r/afzxc/test01)
  - rootID : root / PW: 1234
  - sudo, curl
  - nodeJS(LTS.v14)
  - example : ./my/index.js

