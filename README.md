# Advanced-C-Lab-Manual
## EXP NO:1 C PROGRAM TO ADD TWO DISTANCE IN THE INCH-FEET SYSTEM USING POINTER TO STRUCTURE.

### Aim:
To write a C program to add two distances in the inch-feet system using pointer to structure
### Algorithm:

1. Start and define a structure named Distance with two members: feet and inch.
2. Read two distances (feet and inches) from the user into structure variables.
3. Use pointers to access the structure members and add the feet and inches separately.
4. Normalize inches: if total inches ≥ 12, convert extra inches into feet.
5. Display the final total distance and stop.
 
### Program:
```
#include<stdio.h>
struct distance
{
    int feet;
    float inch;
};
int main()
{
    struct distance d1,d2,result;
    struct distance *presult=&result;
    scanf("%d %f",&d1.feet,&d1.inch);
    scanf("%d %f",&d2.feet,&d2.inch);
    presult->feet=d1.feet+d2.feet;
    presult->inch=d1.inch+d2.inch;
    while(presult->inch>=12.0)
    presult->inch*=0.83;
    printf("Sum of distances = %d'-%.1f\"\n ",presult->feet,presult->inch);
}
```


### Output:
<img width="486" height="242" alt="image" src="https://github.com/user-attachments/assets/79fe6d0a-21b4-4308-93f0-5584e567ff55" />


### Result:
Thus, the program is verified successfully. 



## EXP NO:2 C PROGRAM TO CALCULATE SIMPLE INTEREST FOR 5 YEARS USING POINTER TO STRUCTURE.
Aim:
To write a C program to calculate Simple Interest for 5 years using pointer to structure 

### Algorithm:

1. Begin the program and create a structure to store principal, rate, and time.
2. Assign time as 5 years and read the principal and rate values from the user.
3. Use a pointer to access the structure members.
4. Calculate simple interest using the formula: Principal × Rate × Time ÷ 100.
5. Display the simple interest and end the program.
 
### Program:

```
#include<stdio.h>
struct interest{
    float principle;
   float rate;
   float year;
   float SI;
};
int main(){
   struct interest *resultptr, res;
   resultptr = &res;  
   scanf("%f", &resultptr->principle);
 resultptr->year=5.0;   
   scanf("%f", &resultptr->rate);
   resultptr->SI = (resultptr->principle * resultptr->year* resultptr->rate) /100;
   printf("Simple Interest: %.2f", resultptr->SI);
   return 0;
}
```

### Output:

<img width="490" height="134" alt="image" src="https://github.com/user-attachments/assets/a7763b47-3d60-462c-aa06-dd04a3ba0967" />

### Result:
Thus, the program is verified successfully


 
## EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

### Aim:
To write a C program to read a file name from user

### Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
### Program:
```
#include <stdio.h>
int main() {
    char filename[100];
    FILE *file;
    scanf("%s", filename);
    file = fopen(filename, "w");
    if (file == NULL) {
        printf("Failed to create the file %s\n", filename);
        return 1;
    }
    printf("%s File Created Successfully\n", filename);
    printf("%s File Opened\n", filename);
    fclose(file);
    printf("%s File Closed\n", filename);
    return 0;
}
```
### Output:
![Screenshot 2025-04-27 155500](https://github.com/user-attachments/assets/c2e8ab04-6108-4d99-ae04-18c366f09826)

### Result:
Thus, the program is verified successfully
 


## EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
### Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
### Program:
```
#include <stdio.h>
#include <stdlib.h>
int main() {
    char filename[100];
    FILE *file;
    scanf("%s", filename);
    file = fopen(filename, "w");
    if (file == NULL) {
        printf("Failed to create the file %s\n", filename);
        return 1;
    }
    printf("%s Opened\n", filename);
    int num_lines;
    scanf("%d", &num_lines);
    char line[100];
    getchar();
    for (int i = 0; i < num_lines; i++) {
        fgets(line, sizeof(line), stdin);
        fprintf(file, "%s", line);
    }
    fclose(file);
    printf("Data added Successfully\n");
    return 0;
}

```
### Output:

![Screenshot 2025-04-27 155429](https://github.com/user-attachments/assets/d20c8411-4ecc-4b6e-93b9-fa22d7dff541)

### Result:
Thus, the program is verified successfully



## Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

### Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

### Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

### Program:

```
#include<stdio.h>
struct store
{
    char code[60];
    char name[90];
    int mark;
}s[3];
int main()
{
    for(int i=0;i<3;i++)
    scanf("%s %s %d",s[i].code,s[i].name,&s[i].mark);
    for(int i=0;i<3;i++)
    if(s[i].mark>=95)
    printf("Staff Name:%s\n",s[i].name);
   
}
```
### Output:

![Screenshot 2025-04-27 160148](https://github.com/user-attachments/assets/3f633adf-7b0e-406a-a829-8de3d0aa35e5)
### Result:
Thus, the program is verified successfully
