// Count the number of elements strictly greater than x.
#include<iostream>
using namespace std;
int main()
{
    int n;
    cout<<"Enter array size : ";
    cin>>n;
    int x;
    cout<<"Enter the value of x : ";
    cin>>x;
    int arr[n];
    int count=0;
    cout<<"Enter Your Elements : ";
    for(int i=0;i<n;i++)
    cin>>arr[i];
    for(int i=0;i<n;i++){
        if(arr[i]>x){
            count++;
        }
    }cout<<count;
}


// WAP to find the largest three elements in the array.
#include<iostream>
#include <climits>
using namespace std;
int main()
{
    int n;
    cout<<"Enter the size of Array : ";
    cin>>n;
    int arr[n];
    cout<<"Enter Elements : ";
    for(int i=0;i<n;i++)
    cin>>arr[i];
    int max=INT_MIN;
    int smax=INT_MIN;
    int tmax=INT_MIN;
    for(int i=0;i<n;i++){
        if(arr[i]>max) max=arr[i];
    }
    for(int i=0;i<n;i++){
        if(arr[i]>smax && arr[i]!=max) smax=arr[i];
    }
    for(int i=0;i<n;i++){
        if(arr[i]>tmax && arr[i]!=max && arr[i]!=smax) tmax=arr[i];
    }
    cout<<"Largest element is "<<max<<endl;
    cout<<"Second Largest element is "<<smax<<endl;
    cout<<"Third Largest element is "<<tmax<<endl;
}


// Check if the given array is sorted or not
#include<iostream>
using namespace std;
int main()
{
    int n;
    cout<<"Enter Array size : ";
    cin>>n;
    int arr[n];
    for(int i=1;i<=n;i++)
    cin>>arr[i];
    bool flag=true;
    for(int i=0;i<n-1;i++){
        if(arr[i]>arr[i+1]){
        flag=false;
        break;
        }
    }
    if(flag==true) 
    cout<<"Array is sorted";
    else
    cout<<"Array is Unsorted";
}
