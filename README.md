#include <stdio.h>
#include <math.h>

double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
double sine(double angle);
double cosine(double angle);
double tangent(double angle);
double arcsine(double value);
double arccosine(double value);
double arctangent(double value);
double exponentiation(double base, double exponent);
double squareRoot(double operand);
double cubeRoot(double operand);
double nthRoot(double operand, double n);
double factorial(double n);
double absoluteValue(double operand);
double logarithm(double operand);
double naturalLogarithm(double operand);
double customBaseLogarithm(double operand, double base);

#include <stdio.h>
#include <math.h>

// Function prototypes
// ... (functions remain unchanged)

int main() {
    char choice;
    double a, b, result;

    do {
        printf("\nScientific Calculator Menu:\n");
        printf("A. Basic Operations\n");
        printf("B. Trigonometric Operations\n");
        printf("C. Algebraic Operations\n");
        printf("D. Logarithmic Operations\n");
        printf("E. Quit\n");

        printf("Enter your choice (A, B, C, D, E): ");
        scanf(" %c", &choice);

        switch (choice) {
            case 'A':
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);

                printf("Choose operation:\n");
                printf("   1. Addition\n");
                printf("   2. Subtraction\n");
                printf("   3. Multiplication\n");
                printf("   4. Division\n");
                printf("Enter your choice (1, 2, 3, 4): ");
                int operationChoiceA;
                scanf("%d", &operationChoiceA);

                switch (operationChoiceA) {
                    case 1:
                        result = add(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    case 2:
                        result = subtract(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    case 3:
                        result = multiply(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    case 4:
                        result = divide(a, b);
                        if (b != 0) {
                            printf("Result: %lf\n", result);
                        } else {
                            printf("Error: Division by zero!\n");
                        }
                        break;
                    default:
                        printf("Invalid operation choice.\n");
                }
                break;

            case 'B':
                printf("Enter an angle in radians: ");
                scanf("%lf", &a);
                printf("Choose trigonometric operation:\n");
                printf("   5. Sine\n");
                printf("   6. Cosine\n");
                printf("   7. Tangent\n");
                printf("   8. Arcsine\n");
                printf("   9. Arccosine\n");
                printf("   10. Arctangent\n");
                printf("Enter your choice (5, 6, 7, 8, 9, 10): ");
                int operationChoiceB;
                scanf("%d", &operationChoiceB);

                switch (operationChoiceB) {
                    case 5:
                        result = sine(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 6:
                        result = cosine(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 7:
                        result = tangent(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 8:
                        result = arcsine(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 9:
                        result = arccosine(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 10:
                        result = arctangent(a);
                        printf("Result: %lf\n", result);
                        break;
                    default:
                        printf("Invalid trigonometric operation.\n");
                }
                break;

            case 'C':
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);
                printf("Choose algebraic operation:\n");
                printf("   11. Exponentiation\n");
                printf("   12. Square root\n");
                printf("   13. Cube root\n");
                printf("   14. nth root\n");
                printf("   15. Factorial\n");
                printf("   16. Absolute value\n");
                printf("Enter your choice (11, 12, 13, 14, 15, 16): ");
                int operationChoiceC;
                scanf("%d", &operationChoiceC);

                switch (operationChoiceC) {
                    case 11:
                        result = exponentiation(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    case 12:
                        result = squareRoot(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 13:
                        result = cubeRoot(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 14:
                        printf("Enter the value and the root (nth): ");
                        scanf("%lf %lf", &a, &b);
                        result = nthRoot(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    case 15:
                        result = factorial(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 16:
                        result = absoluteValue(a);
                        printf("Result: %lf\n", result);
                        break;
                    default:
                        printf("Invalid algebraic operation.\n");
                }
                break;

            case 'D':
                printf("Enter a number: ");
                scanf("%lf", &a);
                printf("Choose logarithmic operation:\n");
                printf("   17. Logarithm (base 10)\n");
                printf("   18. Natural logarithm (base e)\n");
                printf("   19. Custom base logarithm\n");
                printf("Enter your choice (17, 18, 19): ");
                int operationChoiceD;
                scanf("%d", &operationChoiceD);

                switch (operationChoiceD) {
                    case 17:
                        result = logarithm(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 18:
                        result = naturalLogarithm(a);
                        printf("Result: %lf\n", result);
                        break;
                    case 19:
                        printf("Enter the number and the base: ");
                        scanf("%lf %lf", &a, &b);
                        result = customBaseLogarithm(a, b);
                        printf("Result: %lf\n", result);
                        break;
                    default:
                        printf("Invalid logarithmic operation.\n");
                }
                break;

            case 'E':
                printf("Exiting the calculator.\n");
                break;

            default:
                printf("Invalid choice. Please enter a valid option.\n");
        }

    } while (choice != 'E');

    return 0;
}


double add(double a, double b) {
    return a + b;
}

double subtract(double a, double b) {
    return a - b;
}

double multiply(double a, double b) {
    return a * b;
}

double divide(double a, double b) {
    if (b != 0) {
        return a / b;
    } else {
        printf("Error: Division by zero.\n");
        return NAN;
    }
}

double sine(double angle) {
    return sin(angle);
}

double cosine(double angle) {
    return cos(angle);
}

double tangent(double angle) {
    return tan(angle);
}

double arcsine(double value) {
    return asin(value);
}

double arccosine(double value) {
    return acos(value);
}

double arctangent(double value) {
    return atan(value);
}

double exponentiation(double base, double exponent) {
    return pow(base, exponent);
}

double squareRoot(double value) {
    return sqrt(value);
}

double cubeRoot(double value) {
    return cbrt(value);
}

double nthRoot(double value, double n) {
    return pow(value, 1.0 / n);
}

double factorial(double n) {
    if (n < 0) {
        printf("Error: Factorial is undefined for negative numbers.\n");
        return NAN;
    }
    if (n == 0) {
        return 1;
    }
    return n * factorial(n - 1);
}

double absoluteValue(double x) {
    return fabs(x);
}


double logarithm(double x) {
    if (x <= 0) {
        printf("Error: Logarithm is undefined for non-positive numbers.\n");
        return NAN;
    }
    return log10(x);
}

double naturalLogarithm(double x) {
    if (x <= 0) {
        printf("Error: Natural logarithm is undefined for non-positive numbers.\n");
        return NAN;
    }
    return log(x);
}

double customBaseLogarithm(double x, double base) {
    if (x <= 0 || base <= 0 || base == 1) {
        printf("Error: Logarithm is undefined for non-positive numbers or base 1.\n");
        return NAN;
    }
    return log(x) / log(base);
}

