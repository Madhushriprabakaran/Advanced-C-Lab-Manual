# EXP NO:6 C PROGRAM TO GIVE A FIVE DIGIT INTEGER N,PRINT THE SUM OF ITS DIGITS.

Aim:
To given a five digit integer n, print the sum of its digits.

Algorithm:

1.Start the program.

2.Read an integer value a from the user.

3.Initialize sum = 0.

4.Repeat while a is not zero:

5.Extract the last digit using a % 10 and add it to sum.

6.Remove the last digit using a / 10.

7.Print the final value of sum.

8.Stop the program.
 
Program:

```
#include <stdio.h>
int main()
{
    int a,sum=0;
    scanf("%d",&a);
    while(a!=0)
    {
        sum+=a%10;
        a/=10;
    }
    printf("%d",sum);
}


```
Output:

<img width="424" height="249" alt="image" src="https://github.com/user-attachments/assets/0f2150d5-99c3-403e-b89a-91adedd08975" />



Result:

Thus, the program is verified successfully

 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE.
Aim:

To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

Algorithm:

1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

```
#include<stdio.h> #include<string.h> int main()
{
char a[50]; scanf("%s",a); int l=strlen(a); char h='0';
for(int i=0;i<4;i++)
{
int c=0;
for(int j=0;j<l;j++)
{
if(a[j]==h)
{
c+=1;
}
}
printf("%d ",c); h++;
}
}



```
Output:


![image](https://github.com/user-attachments/assets/12bccdb8-b8b4-498f-aab1-a2cd31adfdcc)


Result:

Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

Aim:

To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
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
 
Program:
```
#include<stdio.h> #include<string.h> #include<stdlib.h>
int next_per(int n, char **s)
{
for(int i = n - 1 ; i > 0 ; i--) if(strcmp(s[i],s[i-1]) > 0)
{
int j=i+1;
for(;j<n;j++) if (strcmp(s[j],s[i-1])<=0) break; char *t=s[i-1];
s[i-1]=s[j-1];
s[j-1]=t;
for(;i<n-1;i++,n--)
{
t=s[i]; s[i]=s[n-1]; s[n-1]=t;
}
return 1;
}
for(int i=0;i<n-1;i++,n--)
{
char *t=s[i]; s[i]=s[n-1]; s[n-1]=t;
}
return 0;
}
int main()
{
char **s; int n;
scanf("%d",&n); s=calloc(n,sizeof(char*)); for(int i=0;i<n;i++)
{
s[i]=calloc(n,sizeof(char*)*5); scanf("%s",s[i]);
}
do
{
for(int i=0;i<n;i++) printf("%s%c",s[i],i==n-1?'\n':' ');
}
while(next_per(n,s));
 
{
for(int i=0;i<n;i++) free (s[i]);
free(s); return 0;
}
}



```
Output:

![image](https://github.com/user-attachments/assets/b76024b3-2267-4403-bcb0-430d4bba9ebd)


Result:

Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM TO PRINT A PATTERN OF NUMBERS FROM 1 TO N 

Aim:

To write a C program to print a pattern of numbers from 1 to n as shown below.

Algorithm:

1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include<stdio.h> int main()
{
int n,i,j,min; scanf("%d",&n);
int len=n*2-1; for (i=0;i<len;i++)
{
for (j=0;j<len;j++)
{
min=i<j?i:j;
min=min<len-i-1?min:len-1-i; min=min<len-j-1?min:len-1-j; printf("%d ",n-min);
}
printf("\n");
}
return 0;
}



```
Output:


![image](https://github.com/user-attachments/assets/2a1e29c2-674c-4db6-98ff-ec75254ec16b)


Result:

Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

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

Program:

```
#include <stdio.h>
void square();
int main(){
    
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}



```
Output:


![image](https://github.com/user-attachments/assets/4bae1a73-c122-47ea-a3b2-e6887d990718)

Result:

Thus, the program is verified successfully
