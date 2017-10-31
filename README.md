# Ordinal-order

Ordinal order

Problem Description

有n(n<=100)个整数，已经按照从小到大顺序排列好，现在另外给一个整数x，请将该数插入到序列中，并使新的序列仍然有序。 


Input

输入数据包含多个测试实例，每组数据由两行组成，第一行是n和m，第二行是已经有序的n个数的数列。n和m同时为0标示输入数据的结束，本行不做处理。 


Output

对于每个测试实例，输出插入新的元素后的数列。 


Sample Input

3 3

1 2 4

0 0

 
Sample Output

1 2 3 4 


解答：

#include<stdio.h>

main()

{

    int n,m,a[100],b[100],i,j,k,s,w,d;
    
    scanf("%d%d",&n,&m);
    
    while(!(n==0&&m==0))
    
    {
    
        w=0;
        
        for(i=0;i<n;i++)
        
        scanf("%d",&a[i]);
        
        s=a[0];
        
            if(m<s)
            
            {
            
                printf("%d",m);
                
                for(j=0;j<n;j++)
                
                {
                
                 printf(" ");
                 
                printf("%d",a[j]);
                
                }
                
            }
            
            else
            
            {
            
                for(j=0;j<n;j++)
                
                {
                
                    if(m>a[j])
                    
                    w=w+1;
                    
                }
                
                for(j=0;j<w;j++)
                
               {
               
                printf("%d",a[j]);
                
                printf(" ");
                
               }
               
                printf("%d",m);
                
                for(j=w;j<n;j++)
                
                {
                
                    printf(" ");
                    
                printf("%d",a[j]);
                
                }
                
            }
            
        printf("\n");
        
       scanf("%d%d",&n,&m);
       
        
    }
    
}
