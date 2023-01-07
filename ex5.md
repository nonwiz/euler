# Smallest multiple

At first glance, I thought it's easy, actually it actually is just need to read a little bit careful. I thought I could just simply divide from even number from 10 to 20 but yeah turned out nope! Luckily I managed to read it few more times again when entering the wrong ans.

```dart
bool isDivisible(int num) {
  for (int i = 11; i <= 20; i++) {
    if (num % i != 0) {
      return false;
    }
  }
  return true;
}

void main(List<String> arguments) {
  bool found = false;
  int num = 20;
  int limit = 0;
  while (!found && limit < 100000000000) {
    if (isDivisible(num)) {
      print("Divisible by ${num}");
      found = true;
      break;
    }
    num += 2;
    limit++;
  }
}

```

