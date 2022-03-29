### [스프링 없이 의존성 주입]
* 새성자를 통한 의존성 주입
* 속성을 통한 의존성 주입

### [스프링을 통한 의존성 주입]
* XML 파일 사용
* 스프링 설정 파일(xml)에서 속성 주입
* @Autowired 통한 속성 주입
  - type 기준 매칭 : 같은 타입을 구현한 클래스가 여러개 존재하면 bean 태그 id 로 구분
* @Resource 통한 속성 주입

### 📌 @Autowired vs. @Resource vs.<property> 태그
 | |@Autowired | @Resource | 
  |---|---|---|
  |출처| 스프링 애노테이션 | 자바 애노테이션 | 
  |빈 검색 우선순위 | type > id | id > type | 
  |특이사항 | @Qualifier("") 혐업 | name 애트리뷰트 |
  |byName 강제 | @Qualifier("id") | @Resource(name="id")|
