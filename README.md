package com.byaj;

import java.util.Scanner;
import java.lang.Long;

public class Main {

    public static void main(String[] args) {

        Scanner cardNumber = new Scanner(System.in);
        System.out.print("Enter a Credit Card Number: ");
        long number;
        number = cardNumber.nextLong();
        System.out.print("Credit Card Number: " + number);
        int sum = 0;

        String cardType = String.valueOf(number);

        if (cardType.startsWith("4")) {
            System.out.print(" a Visa card");
        } else if (cardType.startsWith("5")) {
            System.out.print(" a MasterCard");

        } else if (cardType.startsWith("3")) {
            System.out.print(" an American Express card ");
        }

        while (number > 0)

            number = number / 10;

        if (number % 2 != 0) {
            number *= 2;
        }

        if (number > 9) {
            number = (number % 10) + 1;
        } else
            number *= 1;

        sum += number;

        if (sum % 10 == 0) {
            System.out.println(" is valid.");
        } else
            System.out.println(" is invalid. Please try again.");
    }
}
