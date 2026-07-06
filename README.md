# code
First Git Repository
<br>
#include <iostream>

bool isPalindrome(int num) {
    if (num < 0) return false;

    int originalNum = num;
    long reversedNum = 0; 

    while (num > 0) {
        int lastDigit = num % 10;
        reversedNum = (reversedNum * 10) + lastDigit;
        num /= 10;
    }

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
