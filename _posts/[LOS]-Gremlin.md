---
title: "[LOS] - Gremlin"
image: 
  path: /images/gremlin_question.png
  thumbnail: /images/gremlin_question-3000x300.png
  caption: ""
categories:
  - Practice
tags:
  
last_modified_at: 2019-09-21T17:11:50-05:00
---
문제 : 
<img src="gremlin_question.png" class="align-center" alt="">

정리 : 
- Injection 문제
- line 10의 if문을 고려했을 때, 이 코드는 id 값의 결과가 존재하면 solve 함수가 실행되는 구조인 것 같다.
- 하지만 맨 윗단의 쿼리문을 봤을 때, id와 pw가 모두 참이어야 한다.

풀이 : 
<img src="gremlin_answer.png" class="align-center" alt="">
