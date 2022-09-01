---
title:  "[JWT] 인증방식? JWT란?"
excerpt: "인증방식이 필요한 이유와 토큰 기반 인증 방식 JWT"

categories:
  - Web
tags:
  - [Web, JWT, Spring]

permalink: /web/what-is-jwt/

toc: true
toc_sticky: true

date: 2022-09-01
last_modified_at: 2022-09-01
---

😁 

웹 사이트를 개발할 때 마다 너무나 당연하게 사용했던 쿠키+세션 방식이 이제는 사용되지 않고있다~
그리고 이를 대체하고 있는 토큰 기반의 인증 방식이 어떻게 사용되고 있는지 궁금해서 간단하게 조사해 보았다
<br/><br/>

## 1. 인증 방식이 필요한 이유?

- 사용자가 웹 사이트에 로그인하면 페이지 전환이 일어나도 정보는 그대로 유지되어야 함
- 그렇기 때문에 사용자의 정보를 유지해야함
- 또한, 그 정보가 유효한지 확인하기 위한 절차가 필요
<br/><br/>

## 2. 서버(세션) 기반 인증 시스템

- 서버에서 클라이언트의 Session 정보를 메모리나 디스크 또는 DB 등을 통해 저장
- 클라이언트의 상태를 계속해서 유지시켜야 하는 Stateful 서버
<br/><br/>

## 3. 토큰 기반 인증 시스템

- 로그인 시 토큰을 발급하고, 서버로 요청이 있을 때 마다 헤더에 토큰을 함께 보내 유효성을 검사한다
- 사용자의 정보를 서버나 세션에 유지하지 않고 클라이언트 측에서 들어오는 요청만으로 작업을 처리하기 때문에 Stateless
<br/><br/>

## 4. JWT의 특징

- Json 포맷을 이용하여 사용자에 대한 속성을 저장
- Header, Payload, Signature의 3 부분으로 이루어짐
    - Header : 토큰의 타입, Signature를 해싱하기 위한 알고리즘 방식 지정
    - Payload : 토큰에 대한 정보(발급자, 만료 시간 등등)
    - Signature : 토큰을 인코딩하거나 유효성 검증을 할 때 사용하는 고유한 암호화 코드
<br/><br/>

참고

- [https://surprisecomputer.tistory.com/36](https://surprisecomputer.tistory.com/36)
- [https://mangkyu.tistory.com/55](https://mangkyu.tistory.com/55)
- [https://mangkyu.tistory.com/56](https://mangkyu.tistory.com/56)
