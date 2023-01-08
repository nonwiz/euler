# Sum Square difference

ALways scared of doing things recursively but for this exercise, I feel like I wanna practice it a bit. Could have been a lot cleaner if I were to combine the two other function but yeah, I think this will let me read and understand easier as well in the future.

```dart
int squareSum(int num) {
  if (num == 1) {
    return 1;
  }
  return (num * num) + squareSum(num - 1);
}

int sum(int num) {
  if (num == 1) {
    return 1;
  }
  return num + sum(num - 1);
}

void main(List<String> arguments) {
  int naturalNumber = 100;
  int sumSquare = pow(sum(naturalNumber), 2).toInt();
  print(sumSquare - squareSum(naturalNumber));
}
```
