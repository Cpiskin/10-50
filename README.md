import java.util.Scanner;
public class MyClass {
    public static void main(String args[]) {
      
        Scanner s = new Scanner(System.in);
      
        // print line 1
        System.out.println("How many digits are there: ");
        int one = s.nextInt();
        String onee = String.valueOf(one);
        int b=0;
        for(int a=1; a<= onee.length(); a++){
            a++;
            b=a;
        }
        System.out.println(b);
        
        // print line 2
        System.out.println("Sum of all digits: ");
        int two = s.nextInt();
        int sum = 0;
        while(two>0){
            sum += two%10;
            two/=10;
        }
        System.out.println(sum);
        

        // print line 3
        System.out.println("Sum of digits at odd locations: ");
        int three = s.nextInt();
        String threestring = String.valueOf(three);
        int totalOdd = 0;
        for (int i = 0; i < threestring.length(); i += 2) {
            totalOdd += Character.getNumericValue(threestring.charAt(i));
        }
        System.out.println(totalOdd);


        // print line 4
        System.out.println("How many times does the digit 4 appear: ");
        int four = s.nextInt();
        String fourstring = String.valueOf(four);        
        int counterfour = 0;
        for(int i=0; i<fourstring.length(); i++){
            if (fourstring.charAt(i) == '4') {
                counterfour++;
            }
        }
        System.out.println(counterfour);
        
        // print line 5
        System.out.println("What is the middle digit: ");
        int five = s.nextInt(); 
        String fivestring = String.valueOf(five);
        int middleDigit=0;
        if (fivestring.length() % 2 == 0) {
            middleDigit = Character.getNumericValue(fivestring.charAt(fivestring.length() / 2 - 1));
        } else {
            middleDigit = Character.getNumericValue(fivestring.charAt(fivestring.length() / 2));
        }
        System.out.println(middleDigit);

        }
    }
