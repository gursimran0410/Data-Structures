#include<iostream>
using namespace std;
void insertionSort(int a[], int n)
{
   int i, key, j;
   for (i = 1; i < n; i++)
   {
       key = a[i];
       j = i-1;

       while (j >= 0 && a[j] > key)
       {
           a[j+1] = a[j];
           j = j-1;
       }
       a[j+1] = key;
   }
}

void printArray(int a[], int n)
{
   int i;
   for (i=0; i < n; i++)
       cout<< a[i]<<"\t";
   cout<<endl;
}

void Merge(int arr[], int l, int m, int r)
{
    int i, j, k;
    int n1 = m - l + 1;
    int n2 =  r - m;
    int L[n1], R[n2];
    for (i = 0; i < n1; i++)
        L[i] = arr[l + i];
    for (j = 0; j < n2; j++)
        R[j] = arr[m + 1+ j];
    i = 0;
    j = 0;
    k = l;
    while (i < n1 && j < n2)
    {
        if (L[i] <= R[j])
        {
            arr[k] = L[i];
            i++;
        }
        else
        {
            arr[k] = R[j];
            j++;
        }
        k++;
    }
    while (i < n1)
    {
        arr[k] = L[i];
        i++;
        k++;
    }
    while (j < n2)
    {
        arr[k] = R[j];
        j++;
        k++;
    }
}
void mergeSort(int arr[], int l, int r)
{
    if (l < r)
    {

        int m = l+(r-l)/2;

        mergeSort(arr, l, m);
        mergeSort(arr, m+1, r);
        Merge(arr, l, m, r);
    }
}
void printarray(int A[], int n)
{
    int i;
    for (i=0; i < n; i++)
        cout<<A[i]<<"\t";
    cout<<endl;
}

int main()
{
 int n;
 int a[100];
 cout<<"enter length of array"<<endl;
 cin>>n;
 cout<<"enter the array"<<endl;
 for(int i=0;i<n;i++)
 {
     cin>>a[i];
 }
 cout<<"sorted array:"<<endl;
    insertionSort(a, n);
      cout<<"enter length of second array"<<endl;
      int m;
 cin>>m;
 int arr[m+n];
 cout<<"enter the array"<<endl;
 for(int i=n;i<m+n;i++)
 {
     cin>>arr[i];
 }
 for(int i=0;i<n;i++)
 {
     arr[i]=a[i];
 }
mergeSort(arr,0,n+m - 1);
printarray(arr, n+m);
    return 0;
}

