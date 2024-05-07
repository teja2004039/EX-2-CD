## EX-2-CD

## IMPLEMENTATION OF SYMBOL TABLE

Register Number :212221040067

Date : 07/05/2024

## AIM

To write a C program to implement a symbol table.

## ALGORITHM

Start the program.

Get the input from the user with the terminating symbol ‘$’.

Allocate memory for the variable by dynamic memory allocation function.

If the next character of the symbol is an operator then only the memory is allocated.

While reading, the input symbol is inserted into symbol table along with its memory address.

The steps are repeated till ‘$’ is reached.

To reach a variable, enter the variable to be searched and symbol table has been checked for corresponding variable, the variable along with its address is displayed as result.

Stop the program

## PROGRAM
```C
#include<stdio.h> #include<conio.h> #include<ctype.h> #include<stdlib.h> 
void main()
{
    int i=0,j=0,x=0,n,flag=0; 
    void *p,*add[5];
    char ch,srch,b[15],d[15],c;
    printf("Enter the Expression terminated by $:");
    while((c=getchar())!='$')
    {
        b[i]=c; i++;
    }
    n=i-1;
    printf("Given Expression:");
    i=0;
    while(i<=n)
    {
        printf("%c",b[i]); 
        i++;
    }
    printf("\n Symbol Table\n"); 
    printf("Symbol\taddr\t\ttype"); 
    while(j<=n)
    {
        c=b[j]; 
        if(isalpha(toascii(c)))
        {
            if(j==n)
            {           
                p=malloc(c); 
                add[x]=p;
                d[x]=c;
                printf("%c\t%d\tidentifier",c,p);
            }   
            else
            {
                ch=b[j+1];
                if(ch=='+'||ch=='-'||ch=='*'||ch=='=')
                {
                    p=malloc(c); 
                    add[x]=p;
                    d[x]=c; 
                    printf("\n%c\t%d\tidentifier\n",c,p); 
                    x++;
                }
            }
        } 
        j++;
    }
    printf("\n The symbol is to be searched"); 
    srch='B';
    for(i=0;i<=x;i++)
    {
        if(srch==d[i])
        {
            printf("\n Symbol Found"); 
            printf("\n%c @address %d\n",srch,add[i]); 
            flag=1;
        }
    }
    if(flag==0)
        printf("\nSymbol Not Found"); 
    getch();
}
```

## OUTPUT

![image](https://github.com/teja2004039/EX-2-CD/assets/151063592/d276c81b-ba63-4a19-8e7a-e0a6b81a269d)




RESULT

The program to implement a symbol table is executed and the output is verified.

