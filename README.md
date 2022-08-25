# codes#include<iostream>
using namespace std;
bool isSorted(int arr[],int n)
{
    if(n == 0 || n == 1)
    {
        return true;
    }
    if(arr[0] > arr[1])
    {
        return false;
    }
  bool ans = isSorted(arr +1,n-1);
    return ans;
    
}
int main()
{
    int arr[] = {2,3,4,5,6,7,8};
    bool result =isSorted(arr,7);
    if(result == 1){
        std::cout << "array is sorted" << std::endl;
    }
    else
    cout<<"array is not sorted"<<endl;
    return 0;
}
