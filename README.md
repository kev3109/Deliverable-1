# Deliverable-1
Grand Circus Deliverable 1 

import java.util.Scanner;

public class PartyClass{
	public static void main(String[]args)
	{
		String result = "Since you are hosting a ";
		@SuppressWarnings("resource")
		Scanner inputUserScannerObj = new Scanner(System.in);
		System.out.println("Please Choose Option(Event Type): \n1: Casual\n2: Semi Formal\n3: Formal");
		String eventType = inputUserScannerObj.next();
		String furtherInvest = "" ;
		if ("1".equalsIgnoreCase(eventType)) {
			furtherInvest = "sandwiches";
			result  =result + "Casual event for ";
		}
		if ("2".equalsIgnoreCase(eventType)) {
			result  =result + "Semi-Formal event for ";
			furtherInvest = "fried chicken";
		}
		if ("3".equalsIgnoreCase(eventType)) {
			result  =result + "Formal event for ";
			furtherInvest = "chicken parmesan";
		}
		System.out.println("Please Enter (Party Size): ");
		int partySize = inputUserScannerObj.nextInt(); 
		if (partySize == 1) {
			result  = result + String.valueOf(partySize) + " participants, you should serve " + furtherInvest+" prepared in your microwave.";
		}
		if (partySize > 1 && partySize <= 12) {
			result  = result  + String.valueOf(partySize) + " participants, you should serve " + furtherInvest+" prepared in your kitchen.";
		}
		if (partySize > 12) {
			result  = result  + String.valueOf(partySize) + " participants, you should serve " + furtherInvest+" prepared by a caterer.";
		}
		System.out.println(result);
	}
}
