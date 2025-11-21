## EXP NO:6 C PROGRAM TO PRINT THE 6th TERM OF THE SERIES,S(n). 
### Aim:
To write a C program to print the 6th term of the series,S(n).
### Algorithm:

1. Start the program and read the value of n (the term to be found) and the first three terms a, b, and c of the series.
2. If n is 1, 2, or 3, directly return the corresponding value (a, b, or c).
3. If n is greater than 3, define a recursive function S(n) that returns the sum of the previous three terms:
S(n) = S(n-1) + S(n-2) + S(n-3).
4. Call the recursive function with the value n to compute the required term.
5. Display the result returned by the recursive function and end the program.
 
### Program:
```
#include<stdio.h>
int series(int n,int a,int b,int c)
{
    if(n==a||n==b||n==c)
    return n;
    else
    return series(n-1,a,b,c)+series(n-2,a,b,c)+series(n-3,a,b,c);
}
int main()
{
    int n,a,b,c;
    scanf("%d%d%d%d",&n,&a,&b,&c);
    int res=series(n,a,b,c);
    printf("%d",res);
}
```
### Output:
<img width="298" height="129" alt="image" src="https://github.com/user-attachments/assets/022b709d-a9ed-4984-97f2-b5253eac54f3" />

### Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT THE GREATEST OF THE FOUR INTEGERS.
### Aim:
To write a C program to print the greatest of the four integers using a function int max_of_four(int a, int b, int c, int d) which reads four arguments and returns.

### Algorithm:

1. Start the program and read the four integer values: a, b, c, and d.
2. Create a function max_of_four(a, b, c, d) to find the largest value.
3. Inside the function, first compare a and b, store the larger one.
4. Compare this larger value with c, then compare the new larger value with d.
5. Return the final maximum value and print it as the output.
 
### Program:
```
#include<stdio.h>
int max_of_four(int a, int b, int c, int d)
{
    if(a>b && a>c && a>d)
    return a;
    else if(b>a && b>c && b>d)
    return b;
    else if(c>a && c>b && c>d)
    return c;
    else 
    return d;
}
int main()
{
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    int res=max_of_four(a,b,c,d);
    printf("%d",res);
}

```


### Output:
<img width="248" height="247" alt="image" src="https://github.com/user-attachments/assets/8494bc36-8d9a-45d5-b7ae-6174c102f164" />

### Result:
Thus, the program is verified successfully

## EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
### Aim:
To write a C program to print all of its permutations in strict lexicographical order.

### Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
### Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
void swap(char **a,char**b)
{   char *temp=*a;
    *a=*b;
    *b=temp;
}
int next_permutation(char *arr[],int n)
{
    int i=n-2;
    while (i>=0 && strcmp(arr[i],arr[i+1])>=0)
    {
        i--;
    }
    if(i<0)
    {
        return 0;
    }
    int j=n-1;
    while(strcmp(arr[j],arr[i])<=0)
    {
        j--;
    }
    swap(&arr[i],&arr[j]);
    int left=i+1,right=n-1;
    while(left<right)
    {
        swap(&arr[left],&arr[right]);
        left++;
        right--;
    }
    return 1;   
}
int main()
{    int n,i;
    scanf("%d",&n);
    char *arr[n];
    for(i=0;i<n;i++)
    { arr[i]=(char *)malloc(101*sizeof(char));
      scanf("%s",arr[i]);
    }
    do
    {
        for(i=0;i<n;i++)
        {
            printf("%s ",arr[i]);
        }
        printf("\n");
    }
    while(next_permutation(arr,n));
    for(i=0;i<n;i++)
    {
        free(arr[i]);
    }
    return 0;
}
```
### Output:
![Screenshot 2025-04-27 162054](https://github.com/user-attachments/assets/e601eb92-39fd-4907-906a-ec6daed3bfde)

### Result:
Thus, the program is verified successfully
 
## EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.
### Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
### Program:
```
#include<stdio.h>
int main()
{
    int n,i,j,min,len;
    scanf("%d",&n);
    len=2*n-1;
    for(i=0;i<len;i++)
    {
        for(j=0;j<len;j++)
        {
            if(i<j)
             min=i;
            else
             min=j;
            if(min>=len-i-1)
             min=len-i-1;
            if(min>=len-j-1)
             min=len-j-1;
            printf("%d ",n-min);
        }
        printf("\n");
    }
    return 0;
}
```
### Output:

![Screenshot 2025-04-27 162647](https://github.com/user-attachments/assets/8cd9093b-7a2e-4ea9-85ad-17007a460e3c)



Result:
Thus, the program is verified successfully

## EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

### Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

### Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

### Program:
```
#include <stdio.h>
int main()
{
    int a;
    scanf("%d", &a);
    float num;
    scanf("%f", &num);
    
    num=a*a;
    printf("The square of %d is : %.2f", a,num);
}
```
### Output:
![image](https://github.com/user-attachments/assets/4db6cb40-f2d1-4ecb-8354-5a833d1818c8)

### Result:
Thus, the program is verified successfully



























