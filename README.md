# Golf Enrolment
### 유효성 검사
![image](https://user-images.githubusercontent.com/102803326/207761761-7db42c7c-774c-42f7-90db-3fdbf9188ff2.png)
### 수강신청 실행 화면 및 코드
![image](https://user-images.githubusercontent.com/102803326/207761981-e1bac308-c0c6-47e4-bedb-cc376a586056.png)
#### 값이 누락되거나 잘못 입력된경우 경고창(오류창)이 뜨면서 포커스가 이동한다.
![image](https://user-images.githubusercontent.com/102803326/207762254-202a1604-ddd3-44c0-80ef-16309a40c2e9.png)
#### 회원명과 강의명을 선택한후 회원명을 다시 선택하면 이전의 선택했던 강의명과 수강료가 초기화 된다
![image](https://user-images.githubusercontent.com/102803326/207778125-2bfcef18-3a40-4be6-9977-d01f5dfdff2d.png)
![image](https://user-images.githubusercontent.com/102803326/207777750-ba5a3e82-6d66-497c-8037-1bbafa8ccc6b.png)
#### 강의명을 먼저 선택했을경우 "회원명을 먼저 선택하세요" 라는 문구 출력, 회원명을 먼저 선택했을땐 강의명에 따라 수강료가 자동 입력 된다.
![image](https://user-images.githubusercontent.com/102803326/207778465-31d119bd-b855-4577-bf33-5c8d97d76619.png)
![image](https://user-images.githubusercontent.com/102803326/207778800-b2ed5919-1653-4e7b-b6a0-3b72dce389ec.png)
![image](https://user-images.githubusercontent.com/102803326/207778717-f728eb52-81f7-47df-b639-04c04c761752.png)
#### 회원번호가 2로 시작하면 수강료가 50% 할인된다. 
![image](https://user-images.githubusercontent.com/102803326/207779732-14437e8b-e601-4c6e-82f9-61542cfa36e6.png)
![image](https://user-images.githubusercontent.com/102803326/207779548-c897ad50-13c3-41aa-8071-89be252d6b2b.png)
![image](https://user-images.githubusercontent.com/102803326/207779573-b46d4305-677f-4457-9a94-85383aaf8d19.png)
### 강사조회 페이지 실행화면
![image](https://user-images.githubusercontent.com/102803326/208016867-8a61b0e3-b604-4071-acf3-a72aa0fc830a.png)
### 강사조회 페이지 실행코드
```
<section class="section">
		<h2>강사조회</h2>
		<table class = "table_line">
			<thead>
				<tr>
					<th>강사코드</th>
					<th>강사명</th>
					<th>강의명</th>
					<th>수강료</th>
					<th>강사자격취득일</th>
				</tr>
			</thead>
			<tbody>
				<%
					while(rs.next()) {
				%>
				<tr>
					<td><%= rs.getString(1) %></td>
					<td><%= rs.getString(2) %></td>
					<td><%= rs.getString(3) %></td>
					<td><%= rs.getString(4) %></td>
					<td><%= rs.getString(5) %></td>
				</tr>
				<%
					}
				%>
			</tbody>
		</table>
	</section>

	<footer><jsp:include page="layout/footer.jsp"></jsp:include></footer>
</body>
</html>
<%
	rs.close();
	pstmt.close();
	conn.close();
%>
```
### 회원정보 조회 페이지 실행화면
![image](https://user-images.githubusercontent.com/102803326/208017119-9f2b9ce2-ced3-45a2-ac30-34a6bc147513.png)
### 실행코드
```
<header>
<jsp:include page="layout/header.jsp"></jsp:include>
</header>
<nav>
<jsp:include page="layout/nav.jsp"></jsp:include>
</nav>
<section class="section">
<h2>회원정보조회</h2>
<table class="table_line">
<tr>
<th>수강월</th>
<th>회원번호</th>
<th>회원명</th>
<th>강의명</th>
<th>강의장소</th>
<th>수강료</th>
<th>등급</th>
</tr>
<% while(rs.next()){%>
<tr class="center">
<td><%=rs.getString(1)%></td>
<td><%=rs.getString(2)%></td>
<td><%=rs.getString(3)%></td>
<td><%=rs.getString(4)%></td>
<td><%=rs.getString(5)%></td>
<td><%=rs.getString(6)%></td>
<td><%=rs.getString(7)%></td>
<%
}
%>
</tr>
</table>
</section>
<footer>
<jsp:include page="layout/footer.jsp"></jsp:include>
</footer>
```
### 강사매출 현황 페이지 샐행화면 
![image](https://user-images.githubusercontent.com/102803326/208017219-24ebe6b2-5d5e-489b-ab79-308f3746f1e4.png)
### 강사매출 현황 페이지 실행코드






