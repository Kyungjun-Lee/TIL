## JDBC 프로그래밍 정리

- ODBC : C, C++

- JDBC API(Interface)  `java.sql`  + JDBC Driver `DB서버에 따로 추가로 준비`

- JDBC 프로그램의 구현 과정

  1. JDBC 드라이버 로딩(Class.forName(대표클래스이름))

     ```java
     Class.forName("oracle.jdbc.driver.OracleDriver");
     ```

  2. DB서버 접속(DriverManager.getConnection(JDBCURL, ID, PASSWORD))

     ```java
     Connection conn = DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe", "scott", "tiger");
     ```

  3. Statement, PreparedStatement 객체 생성 (차이점 정리!)

     - Statement

       

     - PreparedStatement

       

  4. executeQuery(),  executeUpdate()

     - executeQuery()  - __ResultSet, next(), getXxx()__ 

       

     - executeUpdate() - __int (변화된 행의 갯수)__

       

  5. 연결된 자원 해제 - __close()__

     ```java
     conn.close();
     stmt.close();
     rs.close();
     ```

     

