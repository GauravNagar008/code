# code
First Git Repository
#include <iostream>

bool isPalindrome(int num) {
    // Negative numbers are not palindromes (e.g., -121 reversed is 121-)
    if (num < 0) return false;

    int originalNum = num;
    long reversedNum = 0; // Use long to prevent potential integer overflow

    while (num > 0) {
        int lastDigit = num % 10;
        reversedNum = (reversedNum * 10) + lastDigit;
        num /= 10;
    }

    // If the original number and reversed number are equal, it's a palindrome
    return originalNum == reversedNum;
}

int main() {
    int n;
    std::cout << "Enter an integer: ";
    std::cin >> n;

    if (isPalindrome(n)) {
        std::cout << n << " is a palindrome." << std::endl;
    } else {
        std::cout << n << " is NOT a palindrome." << std::endl;
    }

    return 0;
}
