#include <math.h>
#include <stdio.h>

int main(void) {
  float a, b, c;

  printf("Enter the co-efficient of x^2: ");
  scanf("%f", &a);

  while (a == 0) {
    printf("Invalid! The co-efficient of x^2 can't be 0.\n");
    printf("Please Enter the co-efficient of x^2: ");
    scanf("%f", &a);
  }

  printf("Enter the co-efficient of x: ");
  scanf("%f", &b);

  printf("Enter the constant: ");
  scanf("%f", &c);

  float discriminant, root1, root2;

  discriminant = (b * b) - (4 * a * c);

  if (discriminant > 0) {
    root1 = (-b + sqrt(discriminant)) / (2 * a);
    root2 = (-b - sqrt(discriminant)) / (2 * a);
  } else if (discriminant == 0) {
    root1 = root2 = -b / (2 * a);
  } else {
    discriminant = sqrt(-discriminant) / (2 * a);
    root1 = root2 = -b / (2 * a);
    printf("Root1 = %.2f + %.2fi\n", root1, discriminant);
    printf("Root1 = %.2f - %.2fi\n", root2, discriminant);
    return 0;
  }

  printf("Root1 = %.2f\n", root1);
  printf("Root2 = %.2f\n", root2);

  return 0;
}
