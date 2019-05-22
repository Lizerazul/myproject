import java.util.Scanner;
import java.util.Arrays; 
import java.util.*;
public class Bukvata {
	static Scanner sc = new Scanner(System.in);
	public static int GetInteger()
	{
	while (true)
	{
	try
	{
	return sc.nextInt();
	}
	catch (InputMismatchException e)
	{
	sc.next();
	System.out.print("That’s not an integer. "
	+ "Try again: ");
	}
	}
	}
	public static void main(String[] args) {
		System.out.print("Enter an odd integer from 1 to 10000: ");
		
		int N = GetInteger();
		if (N>10000||N<1)
			System.out.println("The integer is out of limits"+"Try again" );
		int g = N % 2;
		if (g != 1)
			System.out.println("The integer is not odd."+"Try again" );
		
		else 
		System.out.println("You entered" +" "+ N );
		
		// TODO Auto-generated method stub
String a[][] = new String [N+1][N*10];

{for (int i = 0; i <N+1 ; i++) {
	for (int j = 0; j < N*10 ; j++) {
		if(j>=N-i && j<N*2-i ||
				j>=N*3-i && j<N*4-i ||
				j>=N*6-i && j<N*7-i ||
				j>=N*8-i && j<N*9-i ||
				j>=N+i   && j<N*2+i ||
				j>=N*3+i && j<N*4+i ||
				j>=N*6+i && j<N*7+i ||
				j>=N*8+i && j<N*9+i
				)
			a[i][j]="*";
		else a[i][j]="-";
			
		}
		
		}
		


{for (int i = 0; i <N+1 ; i++) {
	for (int j = 0; j < N*10 ; j++) {
		System.out.print(a[i][j] + " ");
		}
		System.out.println();
		}
		

}}}}

