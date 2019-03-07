# InfoOf3
This program reads in three numbers and checks their relations to one another.

import java.util.Scanner;

public class InfoOf3 {
    public static void main(String [] arg) {
        Scanner sc = new Scanner(System.in);
        System.out.print("first number?");
        int num1 = sc.nextInt();
       // System.out.println(num1);
        System.out.print("second number?");
        int num2 = sc.nextInt();
       // System.out.println(num2);
        System.out.print("third number?");
        int num3 = sc.nextInt();
       // System.out.println(num3);
        System.out.println("allAreEqual: " + allAreEqual(num1, num2, num3) +"\ntwoAreEqual: " + twoAreEqual(num1, num2, num3)
                + "\nnoneAreEqual: " + noneAreEqual(num1, num2, num3) + "\nareAscending: " + areAscending(num1, num2, num3)
                + "\nareDescending: " + areDescending(num1, num2, num3) + "\nstrictlyAscending: " + strictlyAscending(num1, num2, num3)
                + "\nstrictlyDescending: " + strictlyDescending(num1, num2, num3));
    }

    public static boolean allAreEqual(int num1, int num2, int num3) {
        return num1 == num2 && num2 == num3;
    }
    public static boolean twoAreEqual(int num1, int num2, int num3) {
        return (num1 == num2 && num1 !=num3)|| (num1 == num3 && num1 != num2) || (num2 == num3 && num2 != num1);
    }
    public static boolean noneAreEqual(int num1, int num2, int num3) {
        return num1 != num2 && num1 != num3 && num2 != num3;
    }
    public static boolean areAscending(int num1, int num2, int num3) {
        return num1 <= num2 && num2 <= num3;
    }
    public static boolean areDescending(int num1, int num2, int num3) {
        return num1 >= num2 && num2 >= num3;
    }
    public static boolean strictlyAscending(int num1, int num2, int num3) {

        return num1 < num2 && num2 < num3;
    }
    public static boolean strictlyDescending(int num1, int num2, int num3) {
        return num1 > num2 && num2 > num3;
    }

}
