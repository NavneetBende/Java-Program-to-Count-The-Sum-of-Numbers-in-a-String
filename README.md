Count the sum of number in a string
For counting the sum of a digit in a given string, we’re going to code a java program in this article. Take a string input from the user and store it in a variable called “s” in this case. We are using isdigit method of Character class to check that particular character is a digit or not if that character is a digit then add that character to the sum variable to find sum.
 

Capitalize The First and Last Letter in java
Here we need to count the sum of the number present in the string in the string we can have alphabets as well as some digits so we need to find the sum of the digits. Lets take one example to understand this.

Input string :- “4PREP2INSTAA6”
Output :- 12
As in the given string “4PREP2INSTAA6” the number of character that is a number is 4+2+6=12 hence the output is 12.

First we can iterate through the string and check if the character is in range of ‘0’ to ‘9’ if that is the case we will add it to the sum and then print the result.

Using inbuild function we can do the same that is iterate throughout the string and check if the character is a digit or not using isdigit() function.

Algorithm​
Take a string input from user and store it in the variable called “s”.
Take a i for loop start from i=0 to i<s.length().
Check the condition that character is digit or not.
Calculate sum of each digit and store it in the sum variable.
After that simply print the value of sum.
Java​ Code (Count the sum of number in a string)
Run
import java.util.Scanner;
public class Main {
   public static void main(String[] args) {
   String s ="4PREP2INSTAA6";
   int sum=0;
   for (int i = 0; i < s.length(); i++) {
      if(Character.isDigit(s.charAt(i))) 
      sum=sum+Character.getNumericValue(s.charAt(i));
      }
   System.out.println("Sum of all the digit present in String : "+sum);
  }
}
Output
Sum of all the digit present in String : 12
Method 2
Run

public class Main {
public static void main(String[] args) {
String str="4PREP2INSTAA6";
int sum=0;
for(int i=0;i<str.length();i++){ 
if(str.charAt(i)>='0' && str.charAt(i)<='9'){
sum+=(str.charAt(i)-'0');
}
}
System.out.println("Sum of all digits " +sum );
}
}
Output
Sum of all digits 12
