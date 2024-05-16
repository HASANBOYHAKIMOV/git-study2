# 소게. BlogService

--------------------
- 블로그 검색과 관련된 서비스를 제공합니다.

# 빌드 결과물 
--------------------
- [결과물 다운로드](https://Youtube.com)

# 환경 소게

--------------------
- JAVA 17
- Spring Boot 2.7.3
- Gradle 기반 빌드
- H2 인메모리
- JUnit, MockMvc, FixtureMonkey 기반 테스트 케이스 작성
- REST docs 기반 API 명세 작성

# 인라인 코드

- 인라인 코드와 먹록 

### module - application

--------------------------------
- 도마인 엔티티, 입력 포트, 출력 포트 그리고 서비스 로직이 포함되오 있습니다.
    - `domain`
    - `service`
    - `port/input`
    - `port/output`

### module - adapter

--------------------------------
- 출력 포트에 대한 구현체가 포함되어 있습니다.
  - `adapter-persistance (jpa)`
  - adapter-http (http-client)

### module - app

----------------------------------
- 앱을 동작하기 위한 부분이 포함되어 있습니다.
  - `app/app-api`

### 사용
> $ http GET `http://localhost:8080/api/v1/blogs?keyword=SpringFramework`


### 요청

#### Parameter

| Name | Type | Description | Required |
------ | -----|-------------|---|
| keyword | String | 검색 키워드 | 0 |
| url | String | 블로그 url...| x |
|sort | String | ACCURACY (정확도순), RECENCY(최신순)| x |
| page | Integer | 패이지 번호, 기본값1| x |
| size | Ineger | 한 패이지 보여줄 문서 수| x |