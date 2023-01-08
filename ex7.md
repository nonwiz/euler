# Find 10 001st prime

```dart
void findPrime(int end) {
  // counted: 2 3  
  int current = 5;
  int count = 2;
  while (count < end) {
    if (isPrime(current)) {
      count++;
      if (count == end) {
        print("Prime: ${current}, Count: ${count}");
      }
    }
    current += 2;
  }
}
```
