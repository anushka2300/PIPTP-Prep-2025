```

import java.util.*;
public class Problem6{
public static int func(int a,int b){
    if(a>0){
         System.out.println("x:"+a+" "+b);
        int x= func(a-2,a+b);
        int y=func(a-3,a+b);
        int z=func(a-4,a+b);
        return x+y+z;
    }
    else{
        int temp=a;
        a=b;
        b=temp;
        return a+b;
    }
}   
public static void main(String[] args){

Scanner sc=new Scanner(System.in);
int ans=func(4,3);
System.out.println(ans);
sc.close();
}
}
```

### Approach
#### I broke the function into steps of x,y and z.Make a call stack and execute each step of recursion inside the call stack.


