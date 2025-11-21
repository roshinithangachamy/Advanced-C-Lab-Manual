## EXP NO:21 C PROGRAM TO REVERSE A STRING.
### Aim:
To write a C program to  reverse a String.

### Algorithm:

1. Start the program and read the string from the user.
2. Find the length of the string using a loop (count characters until '\0').
3. Set two indices: one at the beginning (start = 0) and one at the end (end = length - 1).
4. Swap the characters at start and end, then move start forward and end backward until both meet.
5. Print the reversed string and end the program.

### Program:
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],temp;
    int i,j;
    scanf("%s",str);
    printf("Input String: %s\n",str);
    i=0;
    j=strlen(str)-1;
    while(i<j)
    {
        temp=str[i];
        str[i]=str[j];
        str[j]=temp;
        i++;
        j--;
    }
    printf("Reverse String: %s\n",str);
    return 0;
}

```
### Output:
<img width="450" height="187" alt="image" src="https://github.com/user-attachments/assets/221f0996-99ea-4e3c-ab02-afc4812f718f" />


### Result:
Thus, the program  that create a function to find the greatest number is verified successfully.

## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
### Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

### Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
### Program:
```
#include<stdio.h>
void calculate_the_max(int a,int b)
{
    int mand=0,mor=0,mxor=0;
    for(int i=1;i<=a;i++)
    {
        for(int j=i+1;j<=a;j++)
        {
            int cand=i&j;
            int cor=i|j;
            int cxor=i^j;
            if(cand>mand && cand<b) mand=cand;
            if(cor>mor && cor<b) mor=cor;
            if(cxor>mxor && cxor<b) mxor=cxor;
        }
    }
    printf("%d\n%d\n%d",mand,mor,mxor);
}
int main()
{
    int a,b;
    scanf("%d%d",&a,&b);
    calculate_the_max(a,b);
    if(a < 2 || a > 1000 || b < 2 || b > a){ 
        
        return 1;
}
}
```
### Output:
![image](https://github.com/user-attachments/assets/d90ad302-5977-4c53-993a-70751d9a41f1)

### Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
### Aim:
To write a C program to write the logic for the requests

### Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
### Program:
```
#include <stdio.h>
#include <stdlib.h>
typedef struct {
    int *books; 
    int size;  
    int capacity; 
} Shelf;
void initialize_shelf(Shelf *shelf, int capacity) {
    shelf->books = (int *)malloc(capacity * sizeof(int));
    shelf->size = 0;
    shelf->capacity = capacity;
}
void add_book(Shelf *shelf, int pages) {
    if (shelf->size == shelf->capacity) {
        shelf->capacity *= 2;
        shelf->books = (int *)realloc(shelf->books, shelf->capacity * sizeof(int));
    }
    shelf->books[shelf->size] = pages;
    shelf->size++;
}
int get_pages(Shelf *shelves, int x, int y) {
    return shelves[x].books[y];
}
int get_number_of_books(Shelf *shelves, int x) {
    return shelves[x].size;
}

int main() {
    int n, q;
    scanf("%d", &n); 
    scanf("%d", &q);
    Shelf *shelves = (Shelf *)malloc(n * sizeof(Shelf));
    for (int i = 0; i < n; i++) {
        initialize_shelf(&shelves[i], 1);
    }
    for (int i = 0; i < q; i++) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            add_book(&shelves[x], y);
        } else if (type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", get_pages(shelves, x, y));
        } else if (type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", get_number_of_books(shelves, x));
        }
    }
    for (int i = 0; i < n; i++) {
        free(shelves[i].books);
    }
    free(shelves);

    return 0;
}
```
### Output:
![image](https://github.com/user-attachments/assets/29e7fb8d-8c4c-41f2-9b1f-97e14133aa79)

### Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
### Aim:
To write a C program print the sum of the integers in the array.

### Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



### Program:
```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int a[n],sum;
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
        sum=sum+a[i];
    }
    printf("%d",sum);
    
}
```
### Output:
![image](https://github.com/user-attachments/assets/7ff13825-cfac-4536-9a17-e4d904b0c847)

### Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE
### Aim:

To write a C program that counts the number of words in a given sentence.

### Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



### Program:
```
#include<stdio.h>
int main()
{
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    int sum;
    for(int i=4;i<=a;i++)
    {
        sum=b+c+d;
        b=c;
        c=d;
        d=sum;
    }
    printf("%d",sum);
}
```

### Output:
![image](https://github.com/user-attachments/assets/c671bfd8-e54c-4c11-98ee-18e20c325866)



### Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
