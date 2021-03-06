# BCMS(Business Card Management System, 명함관리시스템)

## 1. 프로젝트 소개

```
1) 소속 : 계명대학교 경영정보학과 소프트웨어 개발 동아리 '수은불망'
2) 목표 : 아날로그 명함의 효과적인 관리와 그룹원들간의 공유를 통한 일의 효율성 증대를 목적으로 함
3) 기간 : 2015.12 ~ 2016.03
4) 구성원 : 6명
5) 참여도 : 100%
6) 담당업무 : 기획, 분석 및 설계, 개발
7) 주요실적 : 기획, 분석 및 설계, 명함관리 메인 프레임 및 명함 변경 내역 개발
```

## 2. 개발환경

```
언어: Java
IDE: Eclipse
WAS: Apache Tomcat 7.0.73
DBMS: MySQL
버전관리: SVN
기타: HTML5, CSS3, Bootstrap, JSP, MyBatis, JavaScript, JQuery, Ajax
```
### Spring Framework 3.2.4
```
<dependencies>
  <!-- Spring -->
  <dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>${org.springframework-version}</version>
    <exclusions>
    <!-- Exclude Commons Logging in favor of SLF4j -->
      <exclusion>
      <groupId>commons-logging</groupId>
      <artifactId>commons-logging</artifactId>
      </exclusion>
    </exclusions>
	</dependency>
	<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-webmvc</artifactId>
    <version>${org.springframework-version}</version>
  </dependency>				
  <!-- AspectJ -->
  <dependency>
    <groupId>org.aspectj</groupId>
    <artifactId>aspectjrt</artifactId>
    <version>${org.aspectj-version}</version>
  </dependency>			
  <!-- Logging -->
  <dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>${org.slf4j-version}</version>
  </dependency>
  <dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>jcl-over-slf4j</artifactId>
    <version>${org.slf4j-version}</version>
    <scope>runtime</scope>
  </dependency>
  <dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-log4j12</artifactId>
    <version>${org.slf4j-version}</version>
    <scope>runtime</scope>
  </dependency>
  <dependency>
    <groupId>log4j</groupId>
    <artifactId>log4j</artifactId>
    <version>1.2.15</version>
    <exclusions>
      <exclusion>
        <groupId>javax.mail</groupId>
        <artifactId>mail</artifactId>
      </exclusion>
      <exclusion>
        <groupId>javax.jms</groupId>
        <artifactId>jms</artifactId>
      </exclusion>
      <exclusion>
        <groupId>com.sun.jdmk</groupId>
        <artifactId>jmxtools</artifactId>
      </exclusion>
      <exclusion>
        <groupId>com.sun.jmx</groupId>
        <artifactId>jmxri</artifactId>
      </exclusion>
    </exclusions>
    <scope>runtime</scope>
  </dependency>		
  <dependency>
    <groupId>jstl</groupId>
    <artifactId>jstl</artifactId>
    <version>1.2</version>
    <scope>compile</scope>
  </dependency>
  <dependency>
    <groupId>taglibs</groupId>
    <artifactId>standard</artifactId>
    <version>1.1.2</version>
    <scope>compile</scope>
  </dependency>
  <!-- @Inject -->
  <dependency>
    <groupId>javax.inject</groupId>
    <artifactId>javax.inject</artifactId>
    <version>1</version>
  </dependency>				
  <!-- Servlet -->
  <dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>servlet-api</artifactId>
    <version>2.5</version>
    <scope>provided</scope>
  </dependency>
  <dependency>
    <groupId>javax.servlet.jsp</groupId>
    <artifactId>jsp-api</artifactId>
    <version>2.1</version>
    <scope>provided</scope>
  </dependency>
  <dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>jstl</artifactId>
    <version>1.2</version>
  </dependency>	
  <!-- Test -->
  <dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.7</version>
    <scope>test</scope>
  </dependency>		
  <!-- Mysql -->
  <dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-jdbc</artifactId>
    <version>3.2.4.RELEASE</version>
  </dependency>         
  <dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>5.1.26</version>
  </dependency>    
  <dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis</artifactId>
    <version>3.2.2</version>
  </dependency>	         
  <dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis-spring</artifactId>
    <version>1.1.1</version>
  </dependency>		
  <!--보기편한로그 -->
  <dependency>
    <groupId>org.lazyluke</groupId>
    <artifactId>log4jdbc-remix</artifactId>
    <version>0.2.7</version>
  </dependency>
  <!-- JSON -->
  <dependency> 
    <groupId>com.fasterxml.jackson.core</groupId> 
    <artifactId>jackson-core</artifactId> 
    <version>2.4.1</version>
  </dependency> 
  <dependency> 
    <groupId>com.fasterxml.jackson.core</groupId> 
    <artifactId>jackson-databind</artifactId> 
    <version>2.4.1.1</version>
  </dependency>
</dependencies>
```
## 3. 주요기능

* [회원 관리](/bcms/src/main/webapp/WEB-INF/views/login)
* [명함 등록/검색/수정/삭제](/bcms/src/main/webapp/WEB-INF/views/nmeCard)
* [명함 숨기기, 완전 삭제](/bcms/src/main/webapp/WEB-INF/views/nmeCard)
* [명함 공유](/bcms/src/main/webapp/WEB-INF/views/shar)
	* 그룹원끼리 공유
	* 커뮤니케이션 등록/수정/삭제
		* 해당 명함에 대한 의견이나 정보를 남겨 그룹원끼리 공유하며 볼 수 있음
* [명함 보내기](/bcms/src/main/webapp/WEB-INF/views/shar)
	* 명함을 공유하는 것이 아닌, 단순히 보여주기 위한 용도로 만들어진 기능(수정/삭제 불가능)
* [명함 변경 내역](/bcms/src/main/webapp/WEB-INF/views/nmeCard/nmeCardHistrSelectForm.jsp)
	* 해당 명함에 대한 수정 내역들을 볼 수 있음
* [그룹 관리](/bcms/src/main/webapp/WEB-INF/views/group)
	* 전체 그룹원 목록을 볼 수 있음
	* 즐겨찾는 그룹
		* 원하는 그룹원을 선택한 후 추가 버튼을 통해 원하는 즐겨찾기에 추가할 수 있음
