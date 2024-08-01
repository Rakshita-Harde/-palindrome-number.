# -palindrome-number.
//Write a program to print palindrome number.

public class PalindromeNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the upper limit: ");
        int upperLimit = scanner.nextInt();
        scanner.close();

        System.out.println("Palindrome numbers up to " + upperLimit + " are:");
        for (int number = 0; number <= upperLimit; number++) {
            if (isPalindrome(number)) {
                System.out.print(number + " ");
            }
        }
    }

    public static boolean isPalindrome(int number) {
        int originalNumber = number;
        int reversedNumber = 0;
        while (number != 0) {
            int digit = number % 10;
            reversedNumber = reversedNumber * 10 + digit;
            number /= 10;
        }
        return originalNumber == reversedNumber;
    }
}
