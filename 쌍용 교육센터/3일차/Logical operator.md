==**Basic Logical**==

	1) &&(AND)
		true && true == true
		true && false == false
		false && true == false
		false && false == false
		
	2) ||(OR)
		true || true == true
		true || false == true
		false || true == true
		false || false == false
	3) !(NOT)
		!true == false
		!false == true
```java
System.out.println(!3>5);  
//이거 오류나는 이유 : comperison operator보다 logical operator 우선순위가 더 높아서
```

==BIt Logical==

	1) &(Bit AND)
	2) |(Bit OR)
	3) ^(XOR)
	4) ~ (틸드부정)

```java
package days03;  
  
public class Ex05_04 {  
  public static void main(String[] args) {  
  
    System.out.println(10 & 3);  
	//0000 1010 & 0000 0011 == 0000 0010이므로 10진수로는 2
	
	System.out.println(10 | 3);
	// 0000 1010 | 0000 0011
	// 0000 1011이 되므로 11

	System.out.println(10 ^ 3);//XOR  
	//10 == 0000 1010  
	//3 == 0000 0011  
	//결과 == 0000 1001

	System.out.println(~10);  
	//0000 1010  
	//1111 0101이 되는 것  
	//그러니 음수니까 1을 빼서 1111 0100으로 봐야하고  
	//보수를 취하면 0000 1011이 되는거고  
	//이건 11이니까 -11이 되는 거
  }  
}
```
