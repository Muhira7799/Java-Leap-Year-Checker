# Java Leap Year Checker

A small Java console program that reads a year from the user and tells whether it is a leap year.

## Leap Year Rules

A year is a leap year if:

- it is divisible by **400**, or
- it is divisible by **4** but **not** by **100**

```java
if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)) {
    System.out.println(year + " is a leap year.");
} else {
    System.out.println(year + " is not a leap year.");
}
```

## Examples

| Year | Result | Why |
|------|--------|-----|
| 2024 | Leap year | Divisible by 4, not by 100 |
| 2023 | Not a leap year | Not divisible by 4 |
| 1900 | Not a leap year | Divisible by 100 but not by 400 |
| 2000 | Leap year | Divisible by 400 |

## Sample Run

```
Enter a year: 2024
2024 is a leap year.
```

## Requirements

- Java Development Kit (JDK) 8 or higher

## Getting Started

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
javac LeapYear.java
java LeapYear
```

## Notes

- Entering something that is not a whole number, such as `abc`, throws an `InputMismatchException`.
- The program does not reject zero or negative years.

## Project Structure

```
.
├── LeapYear.java
└── README.md
```

## Possible Improvements

- Handle invalid input with `hasNextInt()` or `try-catch`
- Move the check into a separate method such as `isLeapYear(int year)`
- Check a whole range of years and print the leap years
