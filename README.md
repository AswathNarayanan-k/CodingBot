package aaaaaa;
import java.util.*;
import java.util.Arrays;

public class LargestNum {
	public static void main(String args[])
	{
		Scanner sc = new Scanner(System.in);
	    int n = sc.nextInt();
	    int B[] = new int[n];
		for(int i = 0; i < n;i++)
		{
           B[i] = sc.nextInt();
		}
	     array(B);     
	}
	public static void array(int[] B) {
		for(int i=0;i<B.length;i++)
		{
			int pointer=0;
			boolean flag = true;
			for(int j=1;j<B.length-i;j++)
			{
				if(B[pointer]>B[j])
				{
					
				int temp = B[pointer];
				B[pointer] = B[j];
				B[j] = temp ;
				flag = false;
			    }
				pointer++;
			
		    }
			if(flag)
			{
				break;
			}
		}
		System.out.print(Arrays.toString(B));
	}
}

