---

title: Jekyll 블로그에 Utterances 코멘트 적용하기
categories: devlog
tags: [ jekyll, utterances, comments ]

---

Jekyll 블로그를 다시 시작하면서, 기존에 사용하던 Disqus가 좀 난잡하다는 느낌을 받았다.
Minimalist 테마에서 지원하던 Comment Provider들을 둘러다가 Utterances가 제일 심플하고
깃헙 이슈를 이용하고 있어 데이터가 한 곳에 모여있다는 느낌이 들어 적용하기로 했다.

설치는 너무 간단하다.
[Utternaces](https://utteranc.es/?installation_id=15235555&setup_action=install)를 참조하면 된다.

먼저 Github Pages가 있는 저장소를 public으로 설정해야한다. 물론 이건 당연히 되어있어야 Github Pages를 이용할 수 있다. 

그리고 저장소의 Issue 기능을 활성화한다. 활성화 되어있는 것이 기본값이다.

[Utterances Github App](https://github.com/apps/utterances)를 설치한다.

{{page.name}}

{{page.path}}

{{page.categories}}

{{page.url}}

{{page.title}}

{{page.id}}

{{page.dir}}