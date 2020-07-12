---
title: 리액트 웹 어플리케이션 배포하기
---

회사에서 작업 중인 프론트 작업물을 실 서버에 배포할 시기가 다가오고 있다.
인터넷과 이전 작업물을 뒤져보면서 많이 보이는 단어 위주로 정보 수집부터 해 보자..!

### EC2
- Elastic Compute Cloud
- 서버로 쓸 수 있는 환경을 클라우드로 제공하는 아마존 웹 서비스

### NGINX
- 동시 접속 처리에 특화된 웹 서버 프로그램
- 전달자 역할만 한다

### pm2
- 프로세스 매니저  역할
- 어플리케이션의 변경을 반영하기 위해 재시작해야 할 때 무중단으로 배포하기 위해 사용된다

-----

- 서버 쪽에서 프론트 소스를 올려둔 깃 레포를 클론한다.
- node -v, npm -v 체크하여 노드와 npm이 설치되었는지 확인한다.
- npm i
- (프론트 소스에서) `npm i pm2`

-----

```
	"scripts": {
		"prestart": "npm run build",
		"dev": "react-scripts start",
		"build": "react-scripts build",
		"test": "react-scripts test",
		"eject": "react-scripts eject",
		"start": "pm2 start npm --name test"
	},

```
