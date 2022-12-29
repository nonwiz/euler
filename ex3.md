# Find largest prime factor of a number

- Prime number is a number that is divisible by 1 and itself only. 
- Prime factor refer to a number that is divisible by list of prime number like 13915 : 5 x 7 x 13 x 29


## Approach I.

A divisble number would be less than sqrt of the target_number. With this in mind, i store the sqrt of target number. I can find other prime number by looping from 2 and above until the sqrt of target_number. In each loop if target_number % i == 0; I updated the target_number divided by i. 

To find the largest prime number of the factor, I just return when target_number becomes 1 as it divided the final number.

```dart
int findLargestPrimeFactor(int num) {
  int root = sqrt(num).floor();
  for (int i = 2; i <= root; i++) {
    if (num % i == 0) {
      num = (num / i).floor();
      if (num == 1) {
        return i;
      }
    }

  }

  return 0;
}
```
