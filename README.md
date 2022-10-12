# binary-search-program-in-c
#include<stdio.h>
int binarysearch(int arr[],int element,int size)
{
     int low,mid,high;
     low=0;
     high=size-1;

     while(low<=high)
     {
          mid=(low+high)/2;
       if(arr[mid]==element)
       {
           return mid;
       }
           if(arr[mid]<element)
        {
            low=mid+1;
        }
        else
        {
            high=mid-1;
        }
       }

      return -1;
}


int main()
{
int arr[100]={7,20,50,60,80};
 int element=50;
 int size=sizeof(arr)/sizeof(int);
 int searchindex=binarysearch(arr,size,element);
 printf("the element%d was found at index%d\n",element,searchindex);
 return 0;
}
