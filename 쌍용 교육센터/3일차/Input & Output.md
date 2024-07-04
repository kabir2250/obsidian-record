new InputStreamReader ( System.in ) 이름을 standard input divice(키보드)로부터 입력 받아서 출력

// 키보드 -> System.in -> 문자 변환 -> 문자열 변환
//BufferedReader br만 있었다면 BufferedReader가 Reference 자료형이었을거야.(String name처럼)

BufferedReader br = new BufferedReader(new InputStreamReader (System.in));
String name = br.readLine(); //String으로 잡아오기 때문에 String이어야 해

==**에러**==
Unhandled exception type IOException
	method와 exception을 모두 알아야 쓸 수 있음

  
**Question**
	compiler에서 java.lang.*;이 추가되기 때문에
	System에서는 안썼어

System.out.println(name);

[[입력 받기]]
[[Regular Expression(Scanner with Delimiter)]]