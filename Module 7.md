
**C PROGRAM TO FIND THE BIGGEST AMONG THREE NUMBERS USING STRUCTURE.**

Aim:


To write a C program to find the biggest among three numbers using structure.

Algorithm:


1.Start the program.

2.Declare a structure Numbers with three integer members.

3.Read three integer values from the user and store them in the structure variable nums.

4.Compare the three numbers inside the function findBiggest() to determine the largest.

5.Return the biggest number to the main function.

6.Display the biggest number and stop the program.
 
Program:
```
#include <stdio.h>
struct Numbers {
    int num1;
    int num2;
    int num3;
};

int findBiggest(struct Numbers nums) {

    if (nums.num1 >= nums.num2 && nums.num1 >= nums.num3) {
        return nums.num1;
    } else if (nums.num2 >= nums.num1 && nums.num2 >= nums.num3) {
        return nums.num2;
    } else {
        return nums.num3;
    }
}

int main() {
    struct Numbers nums; 

    
    scanf("%d %d %d", &nums.num1, &nums.num2, &nums.num3);

   
    int biggest = findBiggest(nums);
    printf("%d\n", biggest);

    return 0;
}


```


Output:


<img width="522" height="341" alt="image" src="https://github.com/user-attachments/assets/39c72adb-f90a-4d63-8ef8-27bef1472ebe" />





Result:
Thus, the program is verified successfully. 


**EXP NO:2 C PROGRAM TO CALCULATE DIFFERENCE BETWEEN TWO TIME PERIODS USING A USER-DEFINED FUNCTION.**


Aim:


To Write a C Program to Calculate Difference Between Two Time Periods  using a user-defined function.




Algorithm:


1.Start the program and declare three structure variables: start_time, stop_time, and diff.

2.Read the start time and stop time values (hours, minutes, seconds) from the user.

3.Call the function diff_between_time() and pass the start time, stop time, and the address of diff.

4.Inside the function, adjust seconds and minutes if needed (borrow 1 min = 60 sec, borrow 1 hr = 60 min) to ensure valid subtraction.

5.Calculate the difference in hours, minutes, and seconds and store them in the diff structure.

6.Display the start time, stop time, and the final time difference, then end the program.

Program:
```
#include<stdio.h>
struct time {
   int sec;
   int min;
   int hrs;
};
void diff_between_time(struct time t1,
struct time t2,
struct time *diff);
int main(){
   struct time start_time, stop_time, diff;
   scanf("%d %d %d", &start_time.hrs,&start_time.min,&start_time.sec);
   scanf("%d %d %d", &stop_time.hrs,&stop_time.min,&stop_time.sec);

   diff_between_time(start_time, stop_time, &diff);
   printf("Time Difference: %d:%d:%d - ", start_time.hrs,
   start_time.min,
   start_time.sec);
   printf("%d:%d:%d ", stop_time.hrs,
   stop_time.min,
   stop_time.sec);
   printf("= %d:%d:%d", diff.hrs, diff.min, diff.sec);
   return 0;
}

void diff_between_time(struct time start,
struct time stop,
struct time *diff){
   while (stop.sec > start.sec) {
      --start.min;
      start.sec += 60;
   }
   diff->sec = start.sec - stop.sec;
   while (stop.min > start.min) {
      --start.hrs;
      start.min += 60;
   }
   diff->min = start.min - stop.min;
   diff->hrs = start.hrs - stop.hrs;
}



```

Output:



<img width="1083" height="439" alt="image" src="https://github.com/user-attachments/assets/36a598ed-541c-4ccc-9a5d-d318e395af00" />





Result:
Thus, the program is verified successfully


 **EXP.NO:3 C PROGRAM TO CREATE A FILE WITH NAME "Staff.txt"**

 
Aim:


To write a C program to create a file with name "Staff.txt"

Algorithm:


1.Start the program.

2.Declare a file pointer fp.

3.Open the file Staff.txt in write mode.

4.Check if the file opened successfully; if yes, display a success message.

5.Close the file using fclose().

6.Display “File Closed” and end the program.
 
Program:
```
#include <stdio.h>
int main()
{
    FILE *fp;
    fp=fopen("Staff.txt","w");
    if(fp)
    printf("File Created Successfully\nFile Opened");
    fclose(fp);
    printf("\nFile Closed");
}


```


Output:



<img width="752" height="206" alt="image" src="https://github.com/user-attachments/assets/e8d92318-42e6-4008-838a-a2c3bc223d5e" />














Result:
Thus, the program is verified successfully
 


**EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE**


Aim:


To write a C program to read, a file and insert text in that file


Algorithm:


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

 
Program:
```
#include <stdio.h>
int main()
{
FILE *p;
char name[20]; int num;
char text[50]; scanf("%s%d",name,&num); p=fopen("name","w"); printf("%s Opened",name); for(int i=0;i<num;i++)
{
scanf("%s",text); fputs(text,p);
}
printf("\nData added Successfully");

}



```
Output:


![Screenshot 2025-04-25 102406](https://github.com/user-attachments/assets/4a926356-22df-4a11-a5f8-6f7b374e2a86)







Result:
Thus, the program is verified successfully



**Ex No 5 : C PROGRAM TO ADD TWO COMPLEX NUMBERS BY PASSING STRUCTURE TO A FUNCTION**

Aim:


 To write a C Program to Add Two Complex Numbers by Passing Structure to a Function.

Algorithm:


1.Start the program and define a structure Complex with real and imaginary parts.

2.Read the real and imaginary parts of the first complex number (num1).

3.Read the real and imaginary parts of the second complex number (num2).

4.Call the function addComplex() by passing num1 and num2.

5.Compute the sum of the real parts and imaginary parts inside the function and return the result.

6.Display the resulting complex number and end the program.



Program:

```
#include <stdio.h>
struct Complex {
    float real;
    float imag;
};
struct Complex addComplex(struct Complex c1, struct Complex c2) {
    struct Complex result;
    result.real = c1.real + c2.real;
    result.imag = c1.imag + c2.imag;
    return result;
}

int main() {
    struct Complex num1, num2, sum;
    scanf("%f", &num1.real);
    scanf("%f", &num1.imag);
    scanf("%f", &num2.real);
    scanf("%f", &num2.imag);
    sum = addComplex(num1, num2);
    printf("Sum = %.1f + %.1fi\n", sum.real, sum.imag);

    return 0;
}








```

Output:



<img width="556" height="342" alt="image" src="https://github.com/user-attachments/assets/4ee078a4-85d0-4a06-8d0d-b30e3e12367a" />










Result:
Thus, the program is verified successfully
