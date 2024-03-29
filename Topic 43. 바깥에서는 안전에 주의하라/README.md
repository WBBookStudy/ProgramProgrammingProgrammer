# Topic 43. 바깥에서는 안전에 주의하라

## 나무지 90%
코드가 완성이 되면 90% 완성한 것이다. 하지만 이제는 나머지 90%를 고려해야 한다.  
이제 코드가 잘못될 수 있는 경우를 찾아보고, 각 경우에 대한 단위 테스트를 추가하는 것이다.  
잘못된 매개 변수를 넘기거나 리소스를 흘리거나 리소스가 모자라는 경우 따위를 생각해야함.  
내부오류 뿐 아니라 외부에서 시스템을 망가트리려 하는 시도까지 고려해야한다.

## 기본 보안 원칙
1. 공격 표면을 최소화하라.
2. 최소한의 권한 원칙
3. 안전한 기본값
4. 민감 정보를 암호화 하라.
5. 보안 업데이트를 적용하라

### 공격 표면을 최소화 하라
시스템의 공격표면 영역은 공격자가 데이터를 입력, 추출하거나 서비스를 실행시킬 수 있는 모든 접근 지점을 합한것이다.

#### 코드의 복잡성은 공격 매개체를 유발한다.
복잡한 코드는 예상 외의 부작용이 일어날 확률을 높이고, 결과적으로 공격 표면을 넓힌다.

#### 입력 데이터는 공격 매개체다.
외부의 데이터를 절대 신뢰하지 말라. DB나 화면 렌더링, 그밖의 다른 처리 루틴에 전달하기 전에 언제나 나쁜 내용을 제거하라.  
ex) 
```
글자 수를 셀 파일명을 입력하시오:
test.dat; rm rf /
```
#### 인증이 없는 서비스는 공격 매개체다.
인증이 없는 서비스는 전 세게 누구든지 호출할 수 있다.

#### 인증을 요구하는 서비스도 공격 매개체다.
인증 받은 사용자의 수를 언제나 최소로 유지하라. 쓰이지 않거나, 오래되고, 유효하지 않은 사용자나 서비스를 정리하라.

#### 출력 데이터는 공격 매개체다
시스템에 비밀번호를 등록하려고 했더니 "다른 사용자가 사용 중인 비밀번호입니다."라는 오류 메시지를 출력했다는 전설이 있음. 정보를 누설하지 말라....

#### 디버깅 정보는 공격 매개체다.
ATM 기계 화면이나 공항 키오스크, 웹 브라우저 화면에 스택트레이스와 데이터가 가득 나타난다? 해커를 돕는 행위

### 최소한의 권한원칙 
최소한의 권한만을 꼭 필요한 시간만큼 제일 짧게 부여하라. 생각 없이 root나 Administrator같은 최고 권한을 주지 말라. 권한이야 말로 적을수록 낫다.

### 안전한 기본값
기본 설정은 가장 안전한 값이어야 한다. 불편하다고 생각한다면 각 사용자가 보안과 편리함 사이에서 고르도록 하는 편이 낫다.

### 민감 정보를 암호화하라
개인 식별 정보나 금융 데이터, 비밀번호, 다른 인증 정보를 일반 텍스트로 남기지 말라. 설사 데이터가 유출되더라도 암호화가 안정장치를 할것

### 보안 업데이트를 적용하라
업데이트 안하면 알려진 공격 방법으로 뚫린다.


## 상식 대 암호
암호학에 있어서 나의 상식이 맞지 않을 수 있다는 점을 명심하자. 암호화에 있어서 첫 번째 규칙이자 가장 중요한 규칙은 절대 직접 만들지 말라는 것이다.  
암호화의 세계에서는 엄청나게 작고 아주 사소해 보이는 오류가 전체 암호화를 무용지물로 만들어 버릴 수 있다.  























