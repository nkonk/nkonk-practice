
int main()
{
	int inputs;
	int preR=0,Rcount=0,postR=0,i,j,k,l,o,maxlen=0,len,cur=0;
	char a[10000000];
	scanf("%d",&inputs);
	if(inputs <= 10)
	{
		for(o=0;o<inputs;o++)
			{	
			scanf("%s",a);
			len = strlen(a);
			for(i=0;i<len;i++)
				{
					if(i!=0)
					{
						if(a[i-1]=='R')
						{
							preR++;
						}
					}
					for(j=i;j<len;j++)
					{
						for(k=i;k<j+1;k++)
						{
							if(a[k] == 'K')
								Rcount++;
						}
					
					for(k=j+1;k<len;k++)
					{
						if(a[k]=='R')
							postR++;
					}
					cur = preR+Rcount+postR;
					if(cur > maxlen)
						{
							maxlen = cur;
						}
					}
				}
				printf("%d",maxlen);
				}
			}
	}




# nkonk-practice
practice
#include <iostream>

int main()
{
	unsigned  int A[100];

	unsigned  int N;
	unsigned int i=0, j, k;
	int currentXOR = 0, chkXOR = 0;
	printf("asdfkj\n");
	scanf_s("%d", &N);
	int count = 0;
	printf("dnnxnx \n");
	while (i < N && scanf_s("%d", &A[i++]) == 1);
	for (k = 0; k<N; k++){
		currentXOR = 0;
		for (i = k; i<N; i++)
		{
			currentXOR ^= A[i];
			chkXOR = 0;
			for (j = i + 1; j<N; j++)
			{

				chkXOR ^= A[j];

				if (currentXOR == chkXOR)
					count++;

			}
		}
	}
	printf("%d", count);
	scanf_s("%d");
}

