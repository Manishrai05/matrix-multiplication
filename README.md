# matrix-multiplication
#include<stdio.h>


int main() {
    int first[10][10],second[10][10],multiply[10][10];
    int i=0,j=0,c1,r1,c2,r2,k=0,sum=0;
    printf("enter the no. rows in first matrix: ");
    scanf("%d",&r1);
    printf("enter the no. coulumns in first matrix: ");
    scanf("%d",&c1);
    printf("enter the no. rows in second matrix: ");
    scanf("%d",&r2);
    printf("enter the no. coulumns in second matrix: ");
    scanf("%d",&c2);
    while (c1!=r2){
        printf("matrices can\'t be multiplied");
        printf("enter the no. rows in first matrix: ");
        scanf("%d",&r1);
        printf("enter the no. coulumns in first matrix: ");
        scanf("%d",&c1);
        printf("enter the no. rows in second matrix: ");
        scanf("%d",&r2);
         printf("enter the no. coulumns in second matrix: ");
        scanf("%d",&c2);
    }
    printf("enter values of second matrix");
    for (i=0;i<r1;i++){
        for (j=0;j<c1;j++){
            printf("enter the no. on index %d,%d : ",i,j);
            scanf("%d",&first[i][j]);
        }
    }
    for (i=0;i<r1;i++){
        for (j=0;j<c1;j++){
            printf("%d ",first[i][j]);
        }printf("\n");
    }
    printf("enter values of first matrix");
    for (i=0;i<r2;i++){
        for (j=0;j<c2;j++){
            printf("enter the no. on index %d,%d : ",i,j);
            scanf("%d",&second[i][j]);
        }
    }
    for (i=0;i<r2;i++){
        for (j=0;j<c2;j++){
            printf("%d ",second[i][j]);
        }
    }    
        printf("\n");
    for (i=0;i<r1;i++){
        for (j=0;j<c2;j++){
            for (k=0;k<c1;k++){
                sum = sum + first[i][k]*second[k][j];
                multiply[i][j] = sum;
                sum = 0;
            }    
        }     
    }
 
    printf("Product of entered matrices:-\n");
 
    for ( i = 0 ; i <r1  ; i++ ){
        for (j=0;j<c2;j++){
            printf("%d ",multiply[i][j]);
        }
    } 
    return 0;
}    
