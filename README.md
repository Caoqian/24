24
==

24
#include<stdio.h> 

int chu(int p,int q) 

{ 

    if(p%q==0)return p/q; 

    else 

        return 111111; 

} 

int fun(int i,int j,int c) 

{ 

    int s; 

    switch(c) 

    { 

    case 1:s=i+j;break; 

    case 2:s=i-j;break; 

    case 3:s=i*j;break; 

    case 4:s=chu(i,j);break; 

    } 

    return s; 

} 

void print(int c) 

{ 

    if(c==1)printf("+"); 

    else if(c==2)printf("-"); 

    else if(c==3)printf("*"); 

    else printf("/"); 

} 

int main() 

{ 

    int f[4]; //四个1-14的数 

    int i,j,m,n; 

    int a,b,c; //符号 

    int d1,d2,d3; //每步的结果 

    scanf("%d%d%d%d",&f[0],&f[1],&f[2],&f[3]); 

    for(i=0;i<4;i++)   

        for(j=0;j<4;j++) 

            if(j!=i) 

                for(m=0;m<4;m++) 

                    if(m!=i&&m!=j) 

                        for(n=0;n<4;n++) 

                            if(n!=i&&n!=j&&n!=m) 

    for(a=1;a<5;a++) 

        for(b=1;b<5;b++) 

            for(c=1;c<5;c++) 

            { 

                d1=fun(f[i],f[j],a); 

                d2=fun(d1,f[m],b); 

                d3=fun(d2,f[n],c); 

                if(d3==24) 

                { 

                    printf("%d",f[i]); 

                    print(a); 

                    printf("%d",f[j]); 

                    print(b); 

                    printf("%d",f[m]); 

                    print(c); 

                    printf("%d=24\n",f[n]); 

                } 

            } 

            return 0;
