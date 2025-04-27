## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
### Aim:
To write a C program print the lowercase English word corresponding to the number
### Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
### Program:
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[1000];
    scanf("%999s",str);
    int digits[10]={0};
    for(int i=0;i<strlen(str);i++)
    {
        if(str[i]>=48 && str[i]<=57)
        digits[str[i]-48]++;
    }
    for(int i=0;i<10;i++)
    {
        printf("%d ",digits[i]);
    }
    return 0;
}

```
### Output:
![Screenshot 2025-04-27 161206](https://github.com/user-attachments/assets/a9404f71-85f9-4ed0-9d41-db5ea6782ee0)

### Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
### Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
### Program:
```
#include<stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int freq[10]={0};
    scanf("%s",str);
    for(int i=0;i<strlen(str);i++)
    {
        freq[str[i]-'0']++;
    }
    for(int i=0;i<10;i++)
    {
        printf("%d ",freq[i]);
    }
    return 0;
}
```


### Output:

![Screenshot 2025-04-27 161820](https://github.com/user-attachments/assets/4939c1c4-751f-434a-b8dd-c53f7869b329)

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



























