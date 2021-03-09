---
title: Jekyll에 Utterances 코멘트 적용하기
categories: devlog
tags: [ jekyll, utterances, comments ]
---

## Utterances
Jekyll 블로그를 다시 시작하면서, 기존에 사용하던 Disqus가 좀 난잡하다는 느낌을 받았다.
Minimalist 테마에서 지원하던 Comment Provider들을 둘러다가 Utterances가 제일 심플하고
깃헙 이슈를 이용하고 있어 데이터가 한 곳에 모여있다는 느낌이 들어 적용하기로 했다.

## 설치
설치는 너무 간단하다.
[Utternaces 매뉴얼](https://utteranc.es/?installation_id=15235555&setup_action=install)를 참조하면 된다.

### Github Pages가 있는 저장소를 public으로 설정
물론 이건 당연히 되어있어야 Github Pages를 이용할 수 있다.

![Github Public 설정]({{site.url}}/devlog/images/2021-03-09-apply-utterances/github-public.png)

### 저장소의 Issue 기능을 활성화
활성화 되어있는 것이 기본값이다.

![Github Issue 설정]({{site.url}}/devlog/images/2021-03-09-apply-utterances/github-issue-setting.png)

### [Utterances Github App](https://github.com/apps/utterances)를 설치
원래는 **Install** 버튼이지만, 나는 이미 설치가 되어있어서 **Configure** 버튼으로 바뀌어있다.
설치하면서 접근 권한을 전체 저장소로 할지, 해당 저장소에만 할지 설정하는 화면이 뜬다. 편한대로 설정하도록 하자.

![Utterances 설치]({{site.url}}/devlog/images/2021-03-09-apply-utterances/utterances-install.png)

### _config.yml 수정
이제 Jekyll의 설정을 변경할 차례다. comments 부분을 찾아서 수정하면 된다.
theme는 여러가지가 있으니 위의 Utterances 매뉴얼 하단을 참조하면 된다.
issue_term은 github issue에 등록되는 issue 이름인데 pathname으로 하는것이 좋다길래 그대로 놔뒀다.

```
comments:
  provider               : utterances
  utterances:
    theme                : "dark-blue"
    issue_term           : "pathname"
```

## 결과

설정 완료 후에 저장소로 push해서 반영해주면 포스트에 아래와 같이 나타난다.

![설치완료]({{site.url}}/devlog/images/2021-03-09-apply-utterances/installed.png)

그리고 누군가가 댓글을 남기면 저장소 issue에 등록되는 것을 볼 수 있다.

![Github Issue 결과]({{site.url}}/devlog/images/2021-03-09-apply-utterances/github-issue-result.png)