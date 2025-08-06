# 🧮 Decimal to Binary Conversion in Java (Without Using Arrays)

This project demonstrates how to convert a **decimal number to binary** in **Java** without using arrays, lists, or built-in conversion methods.

## 🚀 Features

- Converts a decimal number to binary
- Does **not use arrays**, strings, or collections
- Binary number is computed using **mathematics only**

## 📌 How It Works

The program repeatedly divides the decimal number by 2 and builds the binary result by placing remainders in their correct place using powers of 10.

### 📘 Example

**Input:** `13`  
**Output:** `1101`

## 💡 Java Logic (No Arrays)

```java
import java.util.Scanner;

public class DecimalToBinary {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a decimal number: ");
        int num = sc.nextInt();
        int binary = 0;
        int place = 1;

        while (num > 0) {
            int remainder = num % 2;
            binary += remainder * place;
            place *= 10;
            num /= 2;
        }

        System.out.println("Binary: " + binary);
    }
}
