# Docker ๐ณ

๋ง์ ๋ด์ฉ ๋ฐ ์ต์์ด ์์ง๋ง ์์ฃผ ์ฐ์ผ ๋ช๋ น์ด๋ง ๋ชจ์๋จ์ต๋๋ค,


Docker [์ค์น](https://www.docker.com/get-started) (+ DockerHub ๊ฐ์๊น์ง)


  0. ์ด๋ฏธ์ง ๋ค์ด๋ก๋
  
  <code> $ docker pull ubuntu:18.04 </code>

  1. ์ด๋ฏธ์ง ํ์ธ

  <code> $ docker images </code>

  2. ์ด๋ฏธ์ง ๋ฐ ์ปจํ์ด๋ ์คํ

  <code> $ dockr run -dit -p --name myu -p 3000:80 ubuntu:18.04 </code>

  3. ํ์ธ

  <code> $ docker ps </code>

  <code> $ docker ps -a </code>

  <code> $ docker network ls </code>

  4. ์ปจํ์ด๋ ์ค์ง / (์ฌ)์คํ / bash ์ ๋ฌ  / bash ์ฐ๊ฒฐ

  <code> $ docker stop [NAME] </code>

  <code> $ docker start [NAME] </code>

  <code> $ docker exec [NAME] ls </code>

  <code> $ docker attach myu </code>
  
  5. ์ปจํ์ด๋ ์ญ์ 

  <code> $ docker rm [NAME] </code>

------

  1. ์ด๋ฏธ์ง๋ก ์คํ ํ ์ปจํ์ด๋์์ ์์ ํ ๋ค์ ์ด๋ฏธ์ง๋ก ๋ง๋ค๊ธฐ

  <code> docker commit -a "readme" [:ContainerID] [:ImageName]/[:TagName] </code>

  <code> $ docker commit -a "sudo, curl, nodeLTS(v14), nano" [:ContainerID] [:ImageName]/[:TagName] </code>

  <code> > sha256 ...  ๋ด์ฉ์ด ๋จ๋ฉด ์ ์ </code>

  2. ํ๋ธ์ ํธ์ฌํ๊ธฐ ์ํด ๋ก๊ทธ์ธ

  <code> $ docker login </code>

  3. ํ๊ทธ ๋ช ๋ณ๊ฒฝํ๊ธฐ( ํธ์ฌ ์ด๋ฏธ์ง๋ช๊ณผ ์์ด๋๋ฅผ ์ผ์น )

  <code> docker tag ๊ธฐ์กด์ด๋ฏธ์ง๋ช:[ํ๊ทธ] ์ํ๋_์ด๋ฏธ์ง_๋ช:[ํ๊ทธ] </code>

  <code> $ docker tag [:prevContainerName]:[prevTagName] [:newContainerName]:[:newTagName] </code>

  4. ํ๋ธ์ ํธ์ฌํ๊ธฐ ( ํ๋ธ [ ๋ ํฌ ๐ ](https://hub.docker.com/repository) )

  <code> docker push [ํ๋ธ_์์ด๋]/์ด๋ฏธ์ง๋ช:[ํ๊ทธ] </code>

  <code> $ docker push [:newContainerName]:[:newTagName] </code>

------

### ๊ธฐ๋ณธ ์ค์  ํ ๋ฐฐํฌํ Ubuntu 14.08 Image [ ๐ ](https://hub.docker.com/r/afzxc/test01)
  - rootID : root / PW: 1234
  - sudo, curl
  - nodeJS(LTS.v14)
  - example : ./my/index.js

