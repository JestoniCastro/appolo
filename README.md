# hello Apollo
 
       Welcome to the world the fews are well knowd about this path
#include <stdio.h>


int main()
{

    int size, temp;
    printf("Input the number of elements to be stored in the first array: ");
      scanf("%d",&size);
    printf("Input %d elements in the array: \n", size);
   
    
    int arr1[size];
    for(int i=0;i<size;i++){
        printf("element - %d : ",i);
        scanf("%d",&arr1[i]);
    }
    printf("Input the number of elements to be stored in the second array: ");
    scanf("%d",&size);
    printf("Input %d elements in the array: \n", size);
    
    
    int arr2[size];
    for(int i=0;i<size;i++)
    {
        printf("element - %d : ",i);
        scanf("%d",&arr2[i]);
    }
    
    int arr3[size*2];
    for(int i = 0;i<size;i++)
    {
      arr3[i]=arr1[i];
    }
    for(int i = size ;i<size*2;i++)
    {
      arr3[i]=arr2[i-size];
    }
    for(int i=0;i<(size*2); i++)
        {
           for(int j=0; j<(size*2)-1; j++)
             {
         
                if(arr3[j]<=arr3[j+1])
                 {
                   temp=arr3[j+1];
                   arr3[j+1]=arr3[j];
                   arr3[j]=temp;
                 }  
              }
         } 
        
    printf("The merged array in descending order is: \n");    
    for(int i = 0; i<size*2;i++)
    { 
        
        printf("%d ", arr3[i]);
    }
    return 0;
}
