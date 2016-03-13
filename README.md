# trial
simple java code
import java.io.*;
public class prac
{
    public static void main(String args[])throws IOException
    {
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
        String s,k;
        int n,i,j,flag;
        char c,c1;
      
        System.out.println("enter string:");
        s=br.readLine();
        n=s.length();
        for(i=0;i<n;i++)
        {
            flag=0;
            c=s.charAt(i);
            //System.out.println(c);
            for(j=(i+1);j<n;j++)
        {
            c1=s.charAt(j);
            if(c==c1)
            {
                flag++;
                k=s.substring(0,j)+s.substring(j+1,s.length());
                s=k;
                n=s.length();
                
            
            }
            
        }
        System.out.println(c+" occurs for "+(flag+1)+" no of times");
            
        }
    }
}
        
