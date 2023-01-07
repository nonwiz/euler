# Finding the largest palindrome product

> A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99.
> Find the largest palindrome made from the product of two 3-digit numbers.

I don't really like the solution I come up with yet but well for temporary (hopefully) my future me will patch it up once again:

```dart
bool isPalindrome(int num) {
  int tmp = num;
  int reverseNum = 0;
  while (tmp > 0) {
    int remainder = tmp % 10;
    reverseNum = (reverseNum * 10).toInt() + remainder;
    tmp = (tmp / 10).floor();
  }
  if (reverseNum == num) {
    return true;
  }
  return false;
}

bool checkPalindrome(int a, int b) {
  if (isPalindrome(a * b)) {
    print('Found: a: ${a}, b: ${b} = ${(a) * (b)}');
    return true;
  }
  return false;
}

void findPalindrome(int digit) {
int upper = pow(10, digit).toInt() - 1;
int lower = pow(10, digit - 1).toInt();
int largest = 0;

  for (int a = lower; a <= upper; a++) {
    for (int b = upper; b >= lower; b--) {
      if (checkPalindrome(a, b)) {

          largest = a * b > largest ?  a * b : largest;
      }
    }
  }
print("largest: ${largest}");
}

```
