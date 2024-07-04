```java
public class Ex02_02 {  
  public static void main(String[] args) throws IOException {  
    BufferedReader test = new BufferedReader(new InputStreamReader(System.in));  
  
    byte age;  
  
    System.out.println("이름 입력하세요");  
    String name = test.readLine();  
    System.out.println("나이 입력하세요");  
    age = Byte.parseByte(test.readLine());
	//readLine은 String을 return해주기 때문에 age는 byte,
	//type casting이 필요  
    System.out.printf("이름 \"%s\", 나이 = %d", name, age);  
    //문제점 : 나이 입력이 잘못된 경우 NumberFormatException이 발생  
  
  }  
  
}```
1) Implicit Conversion
	 큰 자료형 = 작은 자료형 값
	
```java 
int i = 100; // [] [] [] [] (4byte)
long l = i;  // [] [] [] [] [] [] [] [] (8byte)
//작은 곳에서 큰 곳으로 가는 건 괜찮아

long k = l + i; // 큰 자료형 + 작은 자료형 = 큰 자료형
```
2) Explicit Conversion - (변환하고자 하는 타입) cast operator
	작은 자료형 = 큰 자료형 값
``` java
i = (int)100L;
```

예를 들면 float a = 3.14;인 경우에, 기본적으로는 double을 쓰기 때문에 오류
float a = 3.14F;를 하든 float a = (float)3.14를 하든 ㅇㅋ

``` java
byte kor, eng, math;  
short total;  
double aver;
total = kor + eng + math;
//이런 경우에 kor + eng + math가 자동으로 int가 되어버려 그래서 cast 해주어야 해
//같은 ()여도 최우선 operator냐 / cast operator냐가 갈려
```
 %\[argument_index$]\[flags]\[width]\[.precision]conversion
 ```java
 
System.out.printf("[%10s]\t\t%d\t%d\t%d\t%d\t%f\n", name, kor, eng, math, total, aver);  
System.out.printf("[%-10s]\t\t%d\t%d\t%d\t%d\t%f\n", name, kor, eng, math, total, aver);

//console 기준 정렬
```
[[문자 타입]]
[[Data]]
[[Data type]]
[[Java 자료형과 타입]]
