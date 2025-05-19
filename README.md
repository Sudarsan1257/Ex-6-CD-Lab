# Ex-6-IMPLEMENTATION-OF-THE-BACK-END-OF-THE-COMPILER-
IMPLEMENTATION OF THE BACK END OF THE COMPILER 
# Date :
# Aim :
To write a program to implement the back end of the compiler.
# ALGORITHM
1. Start the program.
2. Get the three variables from statements and stored in the text file k.txt.
3. Compile the program and give the path of the source file.
4. Execute the program.
5. Target code for the given statement is produced.
6. Stop the program.
# PROGRAM
## .c
```
#include<stdio.h>  
#include<conio.h>  
#include<ctype.h>  
#include<stdlib.h>  
void main() 
{ 
int i=2,j=0,k=2,k1=0; char ip[10],kk[10]; FILE *fp; 
//clrscr();
printf("\nEnter the filename of the intermediate code");  
scanf("%s",kk); 
fp=fopen(kk,"r"); if(fp==NULL) 
{ 
printf("\nError in opening the file");  
getch(); 
} 
//clrscr();  
while(!feof(fp)) 
{ 
fscanf(fp,"%s\n",ip);  

printf("\t\t%s\n",ip); 
} 
rewind(fp); 
printf("\n \n");  
printf("\tStatement\t\tTarget Code\n"); 
printf("\n \n"); 
while(!feof(fp)) 
{ 
fscanf(fp,"%s",ip); 
printf("\t%s",ip); 
printf("\t\tMOV %c,R%d\n\t",ip[i+k],j);  
if(ip[i+1]=='+') 
printf("\t\tADD"); else printf("\t\tSUB");  
if(islower(ip[i])) 
printf("%c,R%d\n\n",ip[i+k1],j);  
else  
printf("%c,%c\n",ip[i],ip[i+2]);  
j++; 
k1=2; k=0; 
} 
printf("\n       \n"); 
getch(); 
fclose(fp); 
}
```
## .txt
```
t1 = a + b
t2 = t1 - c
```
# OUTPUT
![Screenshot 2025-05-19 203757](https://github.com/user-attachments/assets/0ebad96e-2d12-4911-95a8-05ed0d8bfba9)

# Result
The back end of the compiler is implemented successfully, and the output is verified.
