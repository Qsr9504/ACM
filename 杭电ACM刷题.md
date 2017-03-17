##1000：A+B问题
		
	#include<stdio.h>
	#include<iostream>
	using namespace std;
	int main(){
		int a,b;
		while(scanf("%d%d",&a,&b)!=EOF){
			printf("a+b\n",sum);
		}
		return 0;
	}


##1001：连续数求和

	#include<stdio.h>
	#include<iostream>
	using namespace std;
	int main(){
		int a;
		while(scanf("%d",&a)!=EOF){
			int sum = 0;
			sum = (1+a) * a / 2; 
			printf("%d\n\n",sum);
		}
		return 0;
	}

##1004 统计输入字符串次数最多
	#include<stdio.h>
	#include<string.h>
	char a[1000][16];
	int b[1000];
	int main()
	{
	 int n,max,i,j,m;
	  
	 while(scanf("%d",&n)!=EOF)
	 { 
	  getchar();    //吸收回车符。
	  if(n==0)break;
	  for(i=1;i<=n;i++)
	  {
	   b[i]=0;
	   gets(a[i]);   //输入字符串
	  }
	   
	  //统计第i个字符串在所有字符串中出现的次数，存在b[i]
	  for(i=1;i<=n;i++)
	  {
	   for(j=1;j<=n;j++)
	    if(strcmp(a[i],a[j])==0)   
	     b[i]++;
	   
	  }
	  m=1;
	  max=b[1];
	  //求出最大的字符串。
	  for(i=2;i<=n;i++)
	   if(max<b[i])
	   {  m=i;max=b[i];}
	  printf("%s\n",a[m]);
	 }
	return 0;
	}