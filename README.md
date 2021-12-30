# inheritance.j
import java.util.*;
class Employee
{
int id;
String name,designation;
Scanner k=new Scanner(System.in);
void reademp()
{
name=k.next();
designation=k.next();
id=k.nextInt();
}
}
class salary extends Employee
{
int BP,HRA,DA,PF,np;
Scanner k=new Scanner(System.in);
void readsal()
{
BP=k.nextInt();
HRA=k.nextInt();
DA=k.nextInt();
PF=k.nextInt();
}
void calculatesal()
{
np=BP+HRA+DA-PF;
System.out.println("the net pay is:"+np);
}
void dispemp()
{
System.out.println("name of the employee is"+name);
System.out.println("designation is"+designation);
System.out.println("id no is"+id);
System.out.println("the net pay is"+np);
}
}
class inheritance
{
public static void main(String[] args)
{
	Scanner k=new Scanner(System.in);
	System.out.println("enter the value of n");
	int n=k.nextInt();
	int i;
Employee e=new Employee();
salary s=new salary();
for(i=0;i<n;i++)
{
s.reademp();
s.readsal();
s.calculatesal();
s.dispemp();
}
}
}
