Part 5에서 배운 것 간단하게 정리합니다.

## 1. Test

### 1. 1. Test Class 생성
- TestCase를 상속받아 테스트 클래스 생성
  - example) class QuestionModelTests(TestCase):

### 1. 2. Test Method 생성
- test_로 시작하는 메소드를 생성
  - example) def test_was_published_recently_with_future_question(self):

### 1. 3. Test 실행
- python manage.py test <app_name>
  - example) python manage.py test polls

## 2. Test Client
- Django에서 제공하는 User interacting 테스트 기능
- Test Client를 이용하면 View의 동작을 테스트할 수 있고, response의 context를 직접 테스트 가능
  - example) response = self.client.get(reverse('polls:index'))
- 각 뷰별로 Test Client를 사용하여 여러 상황에 대한 테스트를 할 수 있다.

