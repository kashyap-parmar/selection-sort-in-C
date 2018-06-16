# selection-sort-in-C
//Selection Sort is a method of sortring an array of integers generally and is one of the common method of sorting the integers/floating point numbers

#include<stdio.h>

void main()
{
    int i,j,k;
    int A[50],n,index,temp;

    printf("Enter the size of the array:");
    scanf("%d",&n);

    for(i=0;i<n;i++)
    {
        printf("Enter the A[%d] element :",i);
        scanf("%d",&A[i]);
    }

    for(i=0;i<n;i++)
    {
        index=i;

        for(j=i+1;j<n;j++)
        {
            if(A[j]<A[index]) {index=j;}
        }

        temp=A[index];
        A[index]=A[i];
        A[i]=temp;
    }


    for(k=0;k<n;k++)
    {
        printf("%d\n",A[k]);
    }

    getch();
}
