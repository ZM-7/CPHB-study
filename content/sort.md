+++
date = '2024-12-15T23:40:15Z'
title = 'Sort'
+++

## Sorting 

### O(n²): Bubble Sort

    '
    #include <iostream>

    #define LP(i, a, b) for ( i = a; i<= n; i++)

    using namespace std;

    void Bubble_sort(int a[], int n){
      int i = 0;
      int j = 0;
      int tmp = 0;
      
      LP(i, 0, n){
        LP(j, i+1, n){ //fix the first index scroll through the second
          if(a[i]>a[j]){
            tmp = a[i];
            a[i] = a[j];
            a[j] = tmp;
          }
        }
      }
    }

    int main(){
      int n = 0; int i = 0;
      printf("enter the size of the array: \t");
      scanf("\n %d", &n);
      int a[n];
      printf("the values of your array: \n");
      LP(i, 0, n){
        scanf("%d", &a[i]);
      }
      printf("\nyour array is : ");
      LP(i, 0, n){
        printf("%d ", a[i]);
      }
      printf("\nyour sorted array is : ");
      Bubble_sort(a, n);
      LP(i, 0, n){
           printf("%d ", a[i]);
         }

      
      return 0;
    }
    '
### O(n logn): Merge Sort
