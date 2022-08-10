# Commission
# The small and simple program to calculate working commission
# The commission differ according the calculated amount of sales


/**
 * The program to calculate the commission for workers.
 *
 * @author Nathi Mayekiso
 * @version 08/08/2022
 */
import java.util.Scanner;
import java.lang.Math;
public class Commisions
{
    public static void main(String[]args){
    System.out.printf("\f");
    Scanner input=new Scanner(System.in);
    double sales, commision,initial,amount_left;
    System.out.println("Please Enter commision ");
    commision=input.nextDouble();
    
    initial = 5000*0.08;
    if (initial <commision )
    {
      initial = initial + (5000*0.1);
      if(initial <commision)
      {
          amount_left = commision - initial;
          sales = (amount_left/0.12)+10000;
          sales=Math.round(sales*100)/100;
          System.out.println("The sales amount of R"+sales+" is needed to make a commision of "+commision);          
      }
      else if(initial >commision)
      {
          sales=((commision-initial)/0.1)+5000;
           System.out.println("The sales amount of R"+sales+" is needed to make a commision of "+commision);
      }
    }
    else
    {
        sales = ((commision-(5000*0.8))/0.10);
        sales=Math.round(sales*100)/100;
        System.out.println("The sales amount of R"+sales+" is needed to make a commision of "+commision);
    }
    
    
    
    
    
}
}