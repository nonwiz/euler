# Find the special pythagorean

> A Pythagorean triplet is a set of three natural numbers, a < b < c, for which, a2 + b2 = c2. 
> For example, 32 + 42 = 9 + 16 = 25 = 52.
> There exists exactly one Pythagorean triplet for which a + b + c = 1000.
> Find the product abc.

```dart
void findPytha() {
  int limit = 1000;
  num ap, bp, cp;
  double c, result;
  for (int i = 1; i <= limit; i++) {
    for (int l = 2; l <= limit; l++) {
      ap = pow(i, 2);
      bp = pow(l, 2);
      cp = ap + bp;
      c = sqrt(cp);
      result = i + l + c;
      if (result == 1000) {
        print("a: $i, b: $l, c: $c => $ap + $bp = $cp; sum: $result");
      }
    }
  }
}
```
