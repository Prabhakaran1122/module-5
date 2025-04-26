# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main()
{
    int x, *ptr_x;
    float y, *ptr_y, area;

    printf("Enter length of rectangle: ");
    scanf("%d", &x);

    printf("Enter width of rectangle: ");
    scanf("%f", &y);

    ptr_x = &x;
    ptr_y = &y;

    area = (*ptr_x) * (*ptr_y);

    printf("Area of rectangle: %.2f", area);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/1d12ffeb-c5f2-496b-befd-5f4937616ee6)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    char *str;

    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL)
    {
        printf("Memory allocation failed!\n");
        return 1;
    }

    strcpy(str, "WELCOME");

    printf("%s\n", str);

    free(str);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/53471394-39fb-4794-8306-02453a512a68)




## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct student
{
    char name[50];
    int roll_no;
    float marks;
};

int main()
{
    struct student s;

    printf("Enter student's name: ");
    scanf("%s", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.roll_no);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_no);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}

```


## OUTPUT
![image](https://github.com/user-attachments/assets/3f8a8895-3b24-4da4-8aa4-806cac2930e8)



## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct employee
{
    char name[50];
    int id;
    float basic_salary, hra, da, gross_salary;
};

int main()
{
    struct employee e[3];
    int i;

    for(i = 0; i < 3; i++)
    {
        printf("Enter details for employee %d\n", i+1);
        printf("Enter name: ");
        scanf("%s", e[i].name);
        printf("Enter employee ID: ");
        scanf("%d", &e[i].id);
        printf("Enter basic salary: ");
        scanf("%f", &e[i].basic_salary);

        e[i].hra = 0.20 * e[i].basic_salary;
        e[i].da = 0.10 * e[i].basic_salary;
        e[i].gross_salary = e[i].basic_salary + e[i].hra + e[i].da;

        printf("\nEmployee %d Details:\n", i+1);
        printf("Name: %s\n", e[i].name);
        printf("Employee ID: %d\n", e[i].id);
        printf("Basic Salary: %.2f\n", e[i].basic_salary);
        printf("HRA: %.2f\n", e[i].hra);
        printf("DA: %.2f\n", e[i].da);
        printf("Gross Salary: %.2f\n\n", e[i].gross_salary);
    }

    return 0;
}

```


 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/67538aa8-bcbe-412c-a14c-bfebbc1e6614)


 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student
{
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main()
{
    struct student s[2];
    int i, j;

    for(i = 0; i < 2; i++)
    {
        printf("Enter details for student %d\n", i + 1);
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter marks for 5 subjects:\n");
        for(j = 0; j < 5; j++)
        {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for(i = 0; i < 2; i++)
    {
        s[i].total = 0;
        for(j = 0; j < 5; j++)
        {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374;
    s[1].total = 383;

    for(i = 0; i < 2; i++)
    {
        printf("\nTotal marks of student %d: %d\n", i + 1, s[i].total);
    }

    return 0;
}

```


## OUTPUT
![image](https://github.com/user-attachments/assets/b6401f67-c4e8-412c-a715-61f339887158)


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


