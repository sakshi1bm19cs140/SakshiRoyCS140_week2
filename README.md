# SakshiRoyCS140_week2
//Hello World
public class Hello{

    public static void main(String[] args) {
System.out.println("Hello World");
    }
}

//To find the largest of three numbers
public class Great {
    public static void main (String[] args){
        int a=2, b=4, c=7;
        if(a>b&&a>c)
        {
            System.out.println("Largest number is:" + a);
        }
        else if(b>a&&b>c){
            System.out.println("Largest number is:" + b);
        }
        else
        {
            System.out.println("Largest number is:" + c);
        }
    }
}

//To print prime numbers
import java.util.Scanner;

public class Prime {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        System.out.println("Enter low range");
        int low = in.nextInt();
        System.out.println("Enter high range");
        int high = in.nextInt();

        while (low < high) {
            boolean flag = false;

            for(int i = 2; i <= low/2; ++i) {
                if(low % i == 0) {
                    flag = true;
                    break;
                }
            }

            if (!flag && low != 0 && low != 1)
                System.out.print(low + " ");

            ++low;
        }
    }
}

//To print 1 to n numbers
import java.util.Scanner;

public class Print {
    public static void main(String[] args)
    {
        int i;
        Scanner in = new Scanner(System.in);
        System.out.println("Enter a number");
        int n = in.nextInt();
        for(i=1;i<=n;i++)
        {
            System.out.println(i);
        }

    }
}

//To print grades
import java.util.Scanner;

public class Grades {
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter CIE marks");
    int cie[] = new int[5];
    int i;
    float total=0, total2=0, avg;

        for(i=0; i<5; i++) {
            System.out.print("Enter Marks of Subject" + (i + 1) + ":");
            cie[i] = in.nextInt();
            if(cie[i]>50){
                System.out.println("Invalid Marks");
            }
            total = total + cie[i];
        }
        System.out.println("Enter SEE marks");
        int see[] = new int[5];
        int j;
        for(j=0;j<5;j++) {
            System.out.println("Marks of SEE subject" + (j + 1) + ":");
            see[j] = in.nextInt();
            if(see[j]>100){
                System.out.println("Invalid marks");
            }
            total2 = total2 + see[j];
        }
    avg = (total+total2)/5;
        System.out.print("The student Grade is: ");
        if(avg>=80)
    {
        System.out.print("A");
    }
        else if(avg>=60 && avg<80)
    {
        System.out.print("B");
    }
        else if(avg>=40 && avg<60)
    {
        System.out.print("C");
    }
        else
    {
        System.out.print("D");
    }
}
}

//To print half pyramid pattern
import java.util.Scanner;
public class Pattern {
    public static void main(String[] args) {
         Scanner in = new Scanner(System.in);
         System.out.println("Enter number of rows:");
        int rows= in.nextInt();
        int number = 1;
        for(int i = 1; i <= rows; i++) {

            for(int j = 1; j <= i; j++) {
                System.out.print(number + " ");
                ++number;
            }

            System.out.println();
        }
    }
}
