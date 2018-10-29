import java.util.*;
public class Management{
	public static void main(String args[]){
		int i,j,l,c=0;
		String[] name=new String[30];
		int[] age=new int[10];
		String[] branch=new String[10];
		int[] year=new int[10];
		int[] semester=new int[10];
		int[] score=new int[10];
		int choice;
		Scanner sc=new Scanner(System.in);
		System.out.println("Management System Application");
		System.out.println("\t\t1.add student\t2.student data\t3.search\t4.exit");
		System.out.println("Enter your choice:");
		choice=sc.nextInt();
		if(choice==1){
		    if(c<30){
			 System.out.println("Name:");
			 String name= sc.nextLine();
               		 System.out.println("Age:");
               		 String age= sc.nextInt();
               		 System.out.println("Branch:");
               		 String course = sc.nextLine();
                 	 System.out.println("Year:");
                         String year = sc.next();
                         System.out.println("Semester:");
                         String semester = sc.next();
			 System.out.println("Score:");
                         String score = sc.next();
			 Management s=new Management(name,age,branch,year,semester,score);
			 management[x]=s;
			 x++;
		}
		else{
			System.out.println("not able to add the student details");
		}
	}
	else if(choice==2){
		 for (int i=0; i<c; i++) {
               Management s = Management[i];
               System.out.println(s.getName() + s.getAge() + s.getBranch() + s.getYear() + s.getSemester() + s.getScore());
           }
       }
       else if(choice < 1 || choice > 4){
           System.out.println("Invalid choice");
       }
   } while (menuChoice != 4);

   sc.close();
}