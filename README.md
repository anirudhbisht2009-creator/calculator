# calculator
#include <stdio.h>
#include <float.h>
int main() {
   char operator;
   double num1, num2, result;
   // Input operator
   printf("Enter an operator (+, -, *, /): ");
   scanf(" %c", &operator);
   // Input operands
   printf("Enter two numbers: ");
   scanf("%lf %lf", &num1, &num2);
   // Perform operation based on operator
   switch (operator) {
       case '+':
           result = num1 + num2;
           break;
       case '-':
           result = num1 - num2;
           break;
       case '*':
           result = num1 * num2;
           break;
       case '/':
           if (num2 != 0)
               result = num1 / num2;
           else {
               printf("Error! Division by zero.\n");
               return 1;
           }
           break;
       default:
           printf("Error! Invalid operator.\n");
           return 1;
   }
   // Display result
   printf("Result: %.2lf\n", result);
   return 0;
}
