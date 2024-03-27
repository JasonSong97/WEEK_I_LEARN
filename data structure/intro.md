# 📍Calculating complexity

```java
// Given an integer array "arr" with length n,
// O(n)

for (int num: arr) {
    print(num)
}
```

```java
// Given an integer array "arr" with length n,
// O(n), take time more than number 1 code

for (int num: arr) {
    for (int i = 0; i < 500,000; i++) {
        print(num)
    }
}
```

```java
// Given an integer array "arr" with length n,
// O(n^2)

for (int num: arr) {
    for (int num2: arr) {
        print(num * num2)
    }
}
```

```java
// Given integer arrays "arr" with length n and "arr2" with length m,
// O(n + m)

for (int num: arr) {
    print(num)
}

for (int num: arr) {
    print(num)
}

for (int num: arr2) {
    print(num)
}
```

```java
// Given an integer array "arr" with length n,
// O(n^2)
// 1 + 2 + 3 + 4 + ... + n
// (n * (n + 1)) / 2

for (int i = 0; i < arr.length; i++) {
    for (int j = i; j < arr.length; j++) {
        print(arr[i] + arr[j])
    }
}
```

## logarithmic time

절반씩 줄어드는 경우는 O(logn), 상당히 빠르다. binary search가 예시이다.

# 📍Analyzing space complexity

```java
// Given an integer array "arr" with length n
// 공간복잡도 O(1)

for (int num: arr) {
    print(num)
}
````

```java
// Given an integer array "arr" with length n
// 공간복잡도 O(n)

Array doubledNums = int[]

for (int num: arr) {
    doubledNums.add(num * 2)
}
```

```java
// Given an integer array "arr" with length n
// 공간복잡도 O(n)

Array nums = int[]
int oneHundredth = n / 100

for (int i = 0; i < oneHundredth; i++) {
    nums.add(arr[i])
}
```

```java
// Given integer arrays "arr" with length n and "arr2" with length m,
// 공간복잡도 O(n * m)

Array grid = int[n][m]

for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr2.length; j++) {
        grid[i][j] = arr[i] * arr2[j]
    }
}
```

# 📍Recursion

```javascript
function fn(i):
1.  if i > 3:
2.    return

3.  print(i)
4.  fn(i + 1)
5.  print(f"End of call where i = {i}")
6.  return

fn(1)
```

```
// 1
// 2
// 3
// End of call where i = 3
// End of call where i = 2
// End of call where i = 1
```

## 피보나치

0, 1, 1, 2, 3, 5, 8

Fn = F(n - 1) + F(n - 2) -> `recurrence relation`

```
function F(n):
    if n <= 1:
        return n

    oneBack = F(n - 1)
    twoBack = F(n - 2)
    return oneBack + twoBack
```

```
oneBack = F(2)
    oneBack = F(1)
        F(1) = 1
    twoBack = F(0)
        F(0) = 0
    F(2) = oneBack + twoBack = 1
twoBack = F(1)
    F(1) = 1
F(3) = oneBack + twoBack = 2
```