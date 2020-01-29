# C-
#include <stdio.h>
int number(int p,int n)
{
	int i,num;
	num=p;
	for (i=1;i<n;i++){
		num=num+p*10;
		p*=10;
	}
	return num;
}

int number1(int n)
{
	int i,NUM=1;
	for (i=1;i<n+1;i++){NUM*=10;}
	return NUM;
}

int main()
{
	
	int num[10]={0};
	int i=0,N=0,sum=0,M=1,F,p=0,SUM=0;
	for (i=0;i<10;i++){
		scanf("%d",&num[i]);
						}
	
	for (i=0;i<10;i++){sum=sum+num[i];}
//	printf("sum=%d\n",sum);
	for (i=1;i<sum;i++){M*=10;}
//	printf("M=%d\n",M);
	for (i=1;i<10;i++){
		if (num[i]!=0){F=i*M;num[i]-=1;break;}
						}
//	for (i=9;i>=0;i--){
//		if (num[i]!=0){L=number(i,num[i]);break;}
//	}
//	printf("i=%d",i);
//	p=num[i];
//	i-=1;
//	SUM=L;
	for (i=9;i>=0;i--){
		if (num[i]!=0){N=number(i,num[i]);SUM=SUM+N*number1(p);p+=num[i];}
	}	
	SUM=SUM+F;
	printf("%d",SUM);
	return 0;
}

