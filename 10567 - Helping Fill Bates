import java.util.*;
import java.lang.*;
import java.io.*;

public class Main
{
	public static void main(String[] args) throws IOException
	{
		Scanner sc=new Scanner(System.in);
		String s=sc.next();
		int q=sc.nextInt();
		ArrayList<ArrayList<Integer>> a=new ArrayList<ArrayList<Integer>>(256);
		for(int i = 0; i < 256; i++)
		{
			a.add(new ArrayList<Integer>());
		}
		for(int i = 0; i < s.length(); i++)
		{
			a.get((int)s.charAt(i)).add(i);
		}
		while(q-->0)
		{
			String str=sc.next();
			int index=-1,first=0,f=1;
			for(int i=0;i<str.length();i++)
			{
				ArrayList<Integer> b=a.get((int)str.charAt(i));
				index=binary_search(b,index);
				if(index==-1)
				{
					f=0;
					break;
				}
				index=b.get(index);
				if(i==0)
				{
					first=index;
				}
			}
			if(f==1)
				System.out.println("Matched " + first + " " + index);
			else
				System.out.println("Not matched");
		}
	}
	public static int binary_search(ArrayList<Integer> b, int index)
	{
		int l=0,h=b.size()-1,m=0,answer=-1;
		while(l<=h)
		{
			m=l+(h-l)/2;
			if(b.get(m)>index)
			{
				answer=m;
				h=m-1;
			}
			else
			{
				l=m+1;
			}
		}
		return answer;
	}
}
