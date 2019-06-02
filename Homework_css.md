# Homework_css

~~~java
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Homework</title>
<style>
	nav{
		width: 100%;
		margin: 20px auto;
		padding: 10px;
		text-align: center;
		background-image: linear-gradient(30deg, #0c0c27, #1e1e62, #0c0c27);
	}
	h1{
		color: #ffffff; 
		font-size: 2em;
		text-shadow: 8px 8px 8px #00001a;
	}
	a{
		color: #ffffff;
		font-size: 20px;
		text-weight: bold;
		text-decoration: none;
		text-shadow: 10px 10px 10px black;
	}
	a:hover{
		color: #99b3ff;
		font-weight: bold;
	}
	article{
		border: 1px dotted #0c0c27;
		border-radius: 15px;
		margin: 10px auto;
		width: 60%;
	}
	header.head1{
		background-color: #ececf9;
		text-align: left;
		margin-left: 20px;
		margin-right: 20px;
		color: #0c0c27;
		font-size: 20px;
		text-shadow: 2px 2px 6px #002b80;
	}
	header.head2{
		background-color: #ececf9;
		text-align: left;
		margin-left: 20px;
		margin-right: 20px;
		color: #0c0c27;
		font-size: 20px;
		text-shadow: 2px 2px 6px #002b80;
	}
	header.head3{
		background-color: #ececf9;
		text-align: left;
		margin-left: 20px;
		margin-right: 20px;
		color: #0c0c27;
		font-size: 20px;
		text-shadow: 2px 2px 6px #002b80;
	}
	table, th, td{
		margin-left: 10px;
		margin-bottom: 10px;
		border: 1px solid black;
		border-collapse: collapse;
		border-color: #002b80;
		width: 40%;
	}
	th{
		background-color: #3366cc;
	}
	td{
		text-align: center;
	}
	p{
		margin-left: 10px;
	}
	span{
		color: purple;
	}
	figure{
		text-align: center;
	}
	a.figureimg:hover{
		opacity: 0.5;
	}
	footer{
		color: white;
		width: 100%;
		margin: 20px auto;
		padding: 10px;
		text-align: center;
		background-color: #0c0c27;
		background-image: linear-gradient(30deg, #0c0c27, #1e1e62, #0c0c27);
	}
</style>
</head>
<nav>
	<h1>HTML5 학습</h1>
	<a href="http://www.w3.org/">W3C</a>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	<a href="http://www.w3schools.com/">W3SCHOOLS</a>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	<a href="http://jquery.com/">jQuery</a><br>
</nav>
<body>
	<section>
		<article>
			<header class="head1">
				<h3>나의 소개</h3>
			</header>
			<ul>
				<li>이름 : 이경준</li>
				<li>성별 : 남</li>
				<li>관심기술 : HTML5</li>
				<li>취미 : 코딩</li>
			</ul>
		</article>

		<article>
			<header class="head2">
				<h3>올해 재미있게 본 영화</h3>
			</header>
			<table border="1">
				<tr>
					<th>제목</th>
					<th>장르</th>
				</tr>
				<tr>
					<td>어벤져스:앤드게임</td>
					<td>액션,SF</td>
				</tr>
				<tr>
					<td>더 보이</td>
					<td>공포</td>
				</tr>
			</table>
		</article>

		<article>
			<header class="head3">
				<h3>자랑하고 싶은 <span>우리동네</span> 아름다운 곳</h3>
			</header>
			<p>
				여의도 공원은 서울 영등포구 여의도동에 위치한 시민공원이다.<br> 한국전통의 숲, 문화의 마당, 잔디마당,
				자연생태의 숲 등 네 개의 공간으로 이루어져 있다.<br> 주변에 자전거 도로와 산책로가 조성되어있어 시민들에게
				휴식공간이자 문화공간의 역할을 하고 있다.
			</p>
			<figure>
				<a><img src="https://t1.daumcdn.net/cfile/tistory/2262C84D541AF64E1A" width="600"></a>
				<figcaption>서울 영등포구 여의도동에 위치한 여의도공원</figcaption>
			</figure>
		</article>
	</section>

	<aside>
		<p align="center"><iframe src="https://www.youtube.com/embed/2TEeUuMUmN0" width="600" height="400"></iframe>
	</aside>
	<footer>
		<i>이 문서는 이경준에 의해 HTML5와 CSS3 기술을 사용하여 2019년 5월 27일에
			작성하였습니다.(ver.1.0)</i>
	</footer>
</body>
</html>
~~~

