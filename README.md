//Bubble Sort
#include<iostream>
using namespace std;
void bSort(int a[], int n)
 {
    int flag = 0,temp = 0;
    for (int k =0; k < n-1;k++)
    {
        for(int m =0; m <n-1-k;m++)
        {
            if(a[m] > a[m+1])
            {
                // swap(a[m],a[m+1]);
                temp = a[m];
                a[m] = a[m+1];
                a[m+1] = temp;
                flag =1;
            }
        }
        if (flag == 0) break;
    }
 }

 void sortedArr(int a[], int n)
 {
  for ( int i = 0; i < n; i++)
     {
      cout<< " " <<a[i];
     }
 }
int main()
{
int i,n,a[100],key,count = 0;
cout<<"Enter the size of array: ";
cin>>n;
cout<<"Enter the values in array:"<<endl;
    for ( i = 0; i < n; i++) cin>>a[i];
bSort(a,n);
cout << "Sorted Array: ";
sortedArr(a,n);
 return 0;
}
