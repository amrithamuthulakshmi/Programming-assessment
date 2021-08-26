#include<stdio.h>
#include<string.h>
int main()
{
	int n,i,a[100],temp,j,l;
	char s[100],c[100];
	printf("Enter the number of passengers going to travel for a day");
	{
		scanf("%d",&n);
	}
	
		for(i=1;i<=n;i++)
		{
			
			printf("Enter the age and starting station of the passengers%d",i);
			scanf(" %d %c",&a[i],&c[i]);
		}
		for(i=1;i<n;i++)
		{
			for(j=i+1;j<=n;j++)
			{
				if(a[i]<a[j])
				{
					temp=a[i];
					a[i]=a[j];
					a[j]=temp;
					l=c[i];
					c[i]=c[j];
					c[j]=l;
				}
			}
		}
	for(i=1;i<=n;i++)
		{
			printf("%d\n",a[i]);
					    
	   }
	   printf("The highest priority has to be given to passenger%d-%c",a[1],c[1]);
printf("The remaining persons in the queue\n");
{
	for(i=2;i<=n;i++)
		{
			printf("%d-%c\t",a[i],c[i]);
					    
	   }
}
}
