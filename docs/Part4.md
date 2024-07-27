Part 4에서 배운 것 간단하게 정리합니다.

## 1. {% url ... %} 태그
  - url 태그와 app_name, view_name 사용해서 URL 생성
  - example\) `{% url 'polls:detail' question.id %}` => `/polls/5/`로 생성

## 2. forloop.counter
  - forloop.counter로 for문의 반복 횟수를 가져옴 (index + 1)

## 3. HttpResponseRedirect
  - Post 요청 후에는 HttpResponseRedirect로 리다이렉트
  - 그래야 뒤로가기 또는 새로고침 시 Post 요청이 다시 들어오지 않는다.

## 4. Generic View
  - CRUD는 일반적으로 웹 개발에서 많이 사용, 템플릿을 만들어서 제공 (Less code is better)
  - Django에서는 Generic View를 제공
    - ListView, DetailView: Read
    - ResultsView: Update (의 결과)