Part 3 에서 배운 것을 간단하게 정리합니다.

## 1. URL Routing


- polls 앱의 라우팅은 polls/urls.py에 작성
- urlpatterns에 path() 함수를 사용하여 URL 패턴을 정의
  - urlpatterns를 이용해야 Django가 인식합니다.
  - ROOT_URLCONF를 더 자세히 보면 바꿀 수도 있겠지만, 범위를 넘어가므로 우선 패스
- path()는 urlpattern, view 함수를 필수로 받고, 추가적으로 name을 넣습니다. (Url naming에 사용)

## 2. View

### 2.1 Shortcut

- 기본은 django.template.loader.get_template, template.render를 통해 View를 반환
  - django.shortcuts.render를 사용하면 위 두 과정을 한번에 처리
  - render(request, \[template_name\], context)
    - example) render(request, 'polls/index.html', context)
- 위와 비슷하게, 기본적으로 404 에러는 django.http.Http404를 통해 처리
  - django.shortcuts.get_object_or_404 사용하면 한 번에 처리
  - get_object_or_404(Model, \[조건\])
    - example) get_object_or_404(Question, pk=question_id)

### 2.2 Template

- {{ }}로 변수 출력
- {% %}로 제어문 사용
- {% url 'app_name:view_name' \[parameter\] %}로 URL 생성
  - example) {% url 'polls:detail' question.id %}