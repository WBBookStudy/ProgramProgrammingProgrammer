# Topic 11. 가역성
엔지니어는 문제를 풀 때 단순한 하나의 해결책을 좋아하지만 세상엔 영원한 것은 없다.  
중요한 결정이 많이 내려졌을 즈음엔 목표가 너무 작아져서 목표가 움직이거나, 바람의 방향이 바뀌거나, 도쿄의 나비가 날갯짓을 한다면 여러분의 겨냥은 빗나갈 것이다.  


## 가역성 
이 책의 많은 주제는 유연하고 적용 가능한 소프트웨어를 만드는것. DRY원칙, 결합도 줄이기, 외부 설정 사용하기 등이 그런 예시  
되돌릴 수 없는 결정을 줄이자. 왜냐하면 우리가 프로젝트 초기에 늘 최선의 결정을 내리지 못하기 때문.  

## 유연한 아키텍처
아키텍처, 배포, 외부 제품과의 통합 영역을 유연하기 유지하는 데에 관심을 기울이자.  
우리가 할 수 있는건 바꾸기 쉽게 만드는 것이다. 외부의 API를 우리가 만든 추상화 계층으로 숨겨라. 우리의 코드를 여러 컴포넌트로 쪼개라. 결국에는 하나의 거대한 서버에 배포하게 되더라도, 이 방식이 거대한 단일 모듈 어플리케이션을 가져다 쪼개는 것보다 훨씬 쉽다. 그리고 **유행을 좇지 말라.** 누구도 어떤 미래가 펼쳐질지 알 수 없으며, 우리는 특히 더 그렇다.  






















