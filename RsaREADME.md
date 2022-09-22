# CSA5157
#include<stdio.h>
#include<math.h>
int gcd(int a,int h)
{
	int temp;
	while(1)
	{
		temp=a%h;
		if (temp==0)
		 return h;
		 a=h;
		 h=temp;
	}
}
int main()
{
	double p=3;
	double q=7;
	double n=p*q;
	double e=2;
	double phi=(p-1)*(q-1);
	while(e<phi)
	{
		if(gcd(e,phi)==1)
		break;
		else
		e++;
	}
	int k=2;
	double d=(1+(k*phi))/e;
	double msg=20;
	printf("message data=%lf",msg);
	double c=pow(msg,e);
	c=fmod(c,n);
	printf("\nencrypted data =%lf",c);
	double m=pow(c,d);
	c=fmod(m,n);
	printf("\noriginal message sent=%lf",m);
	 return 0;
}
