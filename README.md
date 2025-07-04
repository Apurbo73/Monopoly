### Monopoly CC:
 
 

```cpp
#include <iostream>
using namespace std;
```

* These lines include the input/output library and use the standard namespace so we can use `cin`, `cout`, etc., without prefixing them with `std::`.

---

```cpp
int main() {
```

* This is the entry point of the C++ program.

---

```cpp
    int T;
    cin >> T; // Number of test cases
```

* `T` is the number of test cases you want to run.
* The user inputs how many times the program should check for monopoly conditions.

---

```cpp
    while (T--) {
```

* This loop runs `T` times, once for each test case.
* `T--` decreases the value of `T` after each iteration.

---

```cpp
        int P, Q, R, S;
        cin >> P >> Q >> R >> S;
```

* These four integers represent the profits of companies A, B, C, and D respectively for one test case.

---

```cpp
        if (P > Q + R + S || Q > P + R + S || R > P + Q + S || S > P + Q + R) {
            cout << "YES" << endl;
        } else {
            cout << "NO" << endl;
        }
```

* This `if` condition checks if **any one** company made **more profit** than the **sum of all the other three**.

  * For example, `P > Q + R + S` means company A made more than B + C + D combined.
* If any of these conditions are true, it prints `"YES"` (monopoly exists).
* Otherwise, it prints `"NO"`.

---

```cpp
    return 0;
}
```

* This marks the end of the program...

