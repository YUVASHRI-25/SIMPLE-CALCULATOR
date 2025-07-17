# SIMPLE-CALCULATOR
BY C PROGRAMMING LANGUAGE 

#include <stdio.h>
#include <float.h>

int main() 
{
    char op;
    double a, b, ans;
    
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &op);
    
    printf("Enter two operands: ");
    scanf("%lf %lf", &a, &b);
    
    switch (op)
    {
    case '+':
        ans= a + b;
        break;
    case '-':
        ans = a - b;
        break;
    case '*':
         ans = a * b;
        break;
    case '/':
        ans = a / b;
        break;
    default:
        printf("Error! Incorrect Operator Value\n");
        ans = -DBL_MAX;
    }
    
    if(ans!=-DBL_MAX)
      printf("%.2lf", ans);
    
    return 0;
}


ANOTHER METHOD:
#include <float.h>
#include <stdio.h>

int main()
{
    char op;
    double a, b, ans;

    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &op);

    printf("Enter two operands: ");
    scanf("%lf %lf", &a, &b);

    if (op == '+')
        ans = a + b;
    else if (op == '-')
        ans = a - b;
    else if (op == '*')
        ans= a * b;
    else if (op == '/')
        ans= a / b;
    else 
    {
        printf("Error! Operator is not correct.\n");
        ans = -DBL_MAX;
    }
  
    if (ans != -DBL_MAX)
        printf("Result: %.2lf\n", ans);

    return 0;
}

