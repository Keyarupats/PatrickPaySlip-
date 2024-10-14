# PatrickPaySlip-
PatrickPaySlip 
import java.util.Scanner;

public class PaySlipniPat {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		System.out.print("Input employee name:");
		    String name = scan.nextLine();
		    System.out.println();
		
		System.out.print("Monthly Salary:" );
		    double Msalary = scan.nextDouble();
		    System.out.println();
		
		System.out.print("Input daily rate:");
		    double dailyRate = scan.nextDouble();
		    System.out.println();
		
		System.out.print("Input number of working days:");
		    double WorkingDays = scan.nextDouble();
		    System.out.println();
		    
		System.out.print("Input leave credit left:");
		    double leaveCreditsLeft = scan.nextDouble();
		    System.out.println();
		    
	    System.out.print("Pag-ibig Contribution:");
	        double pagibigContributed = scan.nextDouble(); 
	        System.out.println();
		    
		System.out.print("Total of late in minutes:");
		    double lateinMinutes = scan.nextDouble();
		   System.out.println();
		    
	    System.out.print("SSS Contribution:");
	        double SSSContribution = scan.nextDouble();
	        System.out.println();
	        
	    System.out.print("Withholding Tax:");
	        double withholdingTax = scan.nextDouble();
	        System.out.println();
		
		
		//Computation of Deductions
		double perMinute = dailyRate / (8 * 60);
	    double Leave_Deduction = dailyRate * leaveCreditsLeft;
		double Late_Deduction = perMinute * lateinMinutes;
		double DLA = Leave_Deduction + Late_Deduction;
		double Gpay = Msalary - Leave_Deduction - Late_Deduction;
		double SSS_Deduction = Gpay * SSSContribution;
		double Holding_Tax = Gpay * withholdingTax;
		double Total_Deduction = SSS_Deduction + pagibigContributed + Holding_Tax;
	    double Npay = Gpay - Total_Deduction;
		
		
		
		
		System.out.println("–––––––––––––––––––––––––––––––––––––––––––––––");
		System.out.println("Employee Name:                " + name);
		System.out.println("His/Her Monthly Salary:       " + Msalary);
		System.out.println("His/Her Gross Pay:            " + Gpay);
		System.out.println("–––––––––––––––––––––––––––––––––––––––––––––––");
		System.out.println (" Deduction                       Amount");
		System.out.println("Withholding Tax:              " + Holding_Tax);
		System.out.println("SSS Deduction:                " + SSS_Deduction);
		System.out.println("Total Deduction:              " + Total_Deduction);
		System.out.println("Deduction for late/absent:    " + DLA);
		System.out.println("–––––––––––––––––––––––––––––––––––––––––––––––");
		System.out.println("Net Pay:                      " + Npay);
		System.out.println("–––––––––––––––––––––––––––––––––––––––––––––––");
		
	}
}
