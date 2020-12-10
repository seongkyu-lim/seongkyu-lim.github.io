---
title: 'upsteam과 fork한 저장소 동기화'
date: 2020-09-10
tags:
  - git
---

pull-request를 하기 위해서는 당연하게도 우선 upsteam repository에서 fork한 repository를 upstream 과 동기화하는 과정이 선행되어야합니다.

제가 만약 월요일날 처음 fork를 땄고 금요일 날 까지 자신이 맡은 부분의 코드를 완성하여 pull-request를 하려하는 상황일 때,

upstream repository에는 월요일부터 금요일 사이에 자신말고도 다른 누군가에 의해 많은 부분이 수정,추가,제거 되었을 수 있습니다.

따라서 pr을 날리기 전에는 반드시 upstream과 동기화를 거친 후 pr을 할 필요가 있습니다.

동기화를하는 방법은 다음과 같습니다.
<br>
<br>

```
Git fetch upstream

Git checkout master or git Checkout -b master —track origin/master

Git merge upstream/master

Git push
```
