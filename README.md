# README.md

### 🍰 프로젝트 개요 🍰

- "JJ cake"는 케잌 주문제작 매칭 플랫폼을 제공하는 서비스입니다. 

  

##### 기능

1. 한 곳에서 케이크를 비교하고 주문할 수 있으며 주문 상태를 확인할 수 있는 기능

2. 한 곳에서 여러 판매자와 헷갈리지 않고 연락할 수 있는 기능

3. 자유로운 케이크 커스토마이징 기능

4. 원하는 마감 기한과 가격대, 수령 방식대로 주문할 수 있는 기능

5. 텍스트로 전달하기 어려운 점은 이미지로 전달할 수 있는 기능



##### 케잌 매칭 방법이란?

- 구매자가 사진이 원하는 케이크를 커스터마이징 하여 주문서를 제작하면, 판매자가 견적서를 제출하게됩니다. 구매자가 여러 판매자의 견적서를 읽은 후 판매자 한 명을 선택하면 매칭이 이루어집니다.



### 🛠 주요 기술스택 🛠

##### 프레임워크

- spring boot, vue.js mybatis, spring security

##### 클라우드

- gcp, aws

##### 데이터베이스

- mysql, redis

##### 데브옵스

- jenkins

##### 언어

- java, javasciprt, html5, css

**이슈관리 및 형상관리**

- git, gitbash, gitkraken, jira, notion



### ⚒기술특이점⚒

##### api

- axios, element, JWT





### 💻실행법💻

#### Git Clone

```bash
git clone https://lab.ssafy.com/s02-final/s02p31d105.git
```



#### nodejs 설치

```
https://nodejs.org/ko/
```



#### 패키지 설치

각 폴더에서 설치해야합니다.

```
npm install
```



#### Jenkins 배포



**JENKINS 설정방법**

[[jenkins\] gitlab 과 jenkins webhook 으로 자동빌드 연결](https://lemontia.tistory.com/882)

**JENKINS 빌드 스크립트**

```bash
cd build/libs

if [ -f program.pid ] 
then 
  if kill -9 `cat program.pid` 
  then echo "kill success" 
  else echo "kill failure"
  fi
fi

nohup java -jar ./jjc-1.0.0-CAKE.jar > nohup.out 2>&1 & echo $! > program.pid
```

**PORT 디폴트는 80 → 8080으로 강제 포워딩 방법**

```bash
sudo iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080
```

