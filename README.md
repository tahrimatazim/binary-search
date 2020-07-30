#include<stdio.h>
int main()
{
    int n,i,a[100], key;

    printf("Enter Array Size : ");
    scanf("%d",&n);

    printf("Enter array elements: ");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }

    printf("Enter Search Key : ");
    scanf("%d",&key);

    int left,right,mid;
    left=0;
    right=n-1;
    mid=(left+right)/2;

    while(left<=right)
    {
            if(key<a[mid])
            {
                right=mid-1;
            }
            else if(key>a[mid])
            {
                left=mid+1;
            }
            else if(key==a[mid])
            {
                printf("Found %d at Location",mid);
                break;
            }
        mid=(left+right)/2;
    }
    if(left>right)
    {
        printf("Not Found");
    }
}
