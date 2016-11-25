package Test.pacakge.practise;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Student {
	String name;
	int rollNum;
	int numOfSub;
    double total;
    int mark;
    double percent;
	String result;
	public Student(String name,int rollNum,int numOfSub) throws IOException{
		this.name = name;
		this.rollNum = rollNum;
		this.numOfSub = numOfSub;
		this.getTotMarks(numOfSub);
	}
	public void getTotMarks(int numOfsub) throws IOException{
		
		percent = 0;
		for(int j=0;j<numOfSub;j++){
		System.out.println("Enter Sub" +(j+1)+ "marks:" );	
		InputStreamReader isr = new InputStreamReader(System.in);
		BufferedReader br = new BufferedReader(isr);		
		mark = Integer.parseInt(br.readLine());
		total = total + mark;
	 }
		
	percent = total/numOfSub;
	
	if (percent>= 50){
		result = "Pass";
	}
	else
	{
		result = "Fail";
	}
		
	}

public static void main(String[] args) throws IOException {

int numOfStudent;
InputStreamReader isr1 = new InputStreamReader(System.in);
BufferedReader br1 = new BufferedReader(isr1);
System.out.println("Enter the number of students:" );			
numOfStudent = Integer.parseInt(br1.readLine());
for(int i=0;i<numOfStudent;i++)
{

System.out.println("Enter Roll Number: ");
InputStreamReader isr5 = new InputStreamReader(System.in);
BufferedReader br5 = new BufferedReader(isr5);
 int rollNum  = Integer.parseInt(br5.readLine());
System.out.println("Enter Name: ");
InputStreamReader isr3 = new InputStreamReader(System.in);
BufferedReader br3 = new BufferedReader(isr3);
String name=br3.readLine();
System.out.println("Enter No of Subject: ");
InputStreamReader isr4 = new InputStreamReader(System.in);
BufferedReader br4 = new BufferedReader(isr4);
int numOfSub =Integer.parseInt(br4.readLine());
 Student S1 = (Student) new Student(name, rollNum,numOfSub);	
System.out.println ("student Roll No. = "+ S1.rollNum);
System.out.println ("Name = "+S1.name);
System.out.println("total marks: " +S1.total );
System.out.println("percent: " +S1.percent +"%" );
System.out.println("Result: " +S1.result );		
}
}

}
   
