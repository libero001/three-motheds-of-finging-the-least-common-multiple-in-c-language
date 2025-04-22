# three-motheds-of-finging-the-least-common-multiple-in-c-language
//求最小公倍数

# include <stdio.h>
int min_bei1(int a, int b)
{
	int i = a > b ? a : b;
	while ((i % a) != 0 ||(i % b) != 0)
	{
		i++;
	}
	return i;
}
int min_bei2(int a, int b)
{
	
	int c,a1=a,b1=b;
	while (c = a % b)
	{
		a = b;
		b = c;
	}
	return (a1 * b1) / b;
}
int min_bei3(int a, int b)
{

	int i=1;
	while (a * i % b)
	{
		i++;
	}
	return a*i;
}
int main()
{
	int a, b;
	scanf("%d%d",&a,&b);
	int ret =min_bei1(a, b);
	int ret =min_bei2(a, b);
	int ret =min_bei3(a, b);
	printf("%d\n",ret);
	return 0;

 }
