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

