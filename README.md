# bai-tap-chuong-3
#include <stdio.h>
  
void input(int a[], int *n){
    printf("Nhap n: ");
    scanf("%d", n);
    printf("\n---NHAP MANG----\n");
    int i;
    for(i = 0; i< *n;i++){
        printf("a[%d] = ", i);
        scanf("%d", &a[i]);
    }
}
void InterchangeSort(int a[], int n){  
   int i,  j;
    for (i = 0; i < n - 1; i++)
    {
        for (j = i + 1; j < n; j++)
        {
             if(a[i] < a[j]) 
            {
                int temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
    }
}
void printArray(int arr[], int size)
{
    int i;
    for (i=0; i < size; i++)
        printf("%d ", arr[i]);
    printf("\n");
}
int main()
{
    int arr[1000];
    int n;
    input(arr, &n);
    InterchangeSort(arr, n);
    printf("Sorted array: \n");
    printArray(arr, n);
    return 0;
}
