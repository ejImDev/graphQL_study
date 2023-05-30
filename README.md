## grapeQL 독학 실습용 레파지토리

- 2023.05~ 프로젝트 대비용<br><br>

### 프로젝트 빌드 후 h2콘솔 접속 테스트
1. http://localhost:8080/h2-console/ 접속
2. Saved Settings: Generic h2(Server) 선택
3. JDBC URL: jdbc:h2:mem:dbPerson 변경

### 테스트용 데이터 생성

h2-console 에서 테스트 데이터를 직접 insert하는 방법도 있지만, 해당 예제에서 사용하고 있는 h2 db의 경우 memory에 데이터를 저장하고 있어, 빌드시마다 데이터가 초기화 된다.<br>(실제 서비스 적용시에는 별도 DB로 데이터 구성)<br><br>

해당 예제에서는 CommandLineRunner 인터페이스를 사용하여, 빌드시마다 몇가지 데이터가 자동으로 세팅되도록 구성
