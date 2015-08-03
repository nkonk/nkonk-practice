# nkonk-practice
practice
#include <stdio.h>

int main()
{
	unsigned  int A[100];
	
	unsigned  int N;
    int i,j,k;
    int currentXOR = 0,chkXOR=0;
  scanf("%d",&N);
	int count = 0;
  while (i < N && scanf("%d", &A[i++]) == 1);
  for(k=0;k<N;k++){
  	currentXOR = 0;
  for(i=k;i<N;i++)
  {
  	currentXOR ^= A[i];
  	for(j=i+1;j<N;j++)
  		{
  		
  			chkXOR ^= A[j];
  			
  			if (currentXOR == chkXOR)
  				count++;
  			
  		}
  }
  }
  	printf("%d",count);
}
