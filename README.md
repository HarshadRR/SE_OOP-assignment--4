# SE_OOP-assignment--4 [Design a base class shape with two double type values and member functions to input the data and
compute_area() for calculating area of shape. Derive two classes: triangle and rectangle. Make
compute_area() as abstract function and redefine this function in the derived class to suit their
requirements. Write a program that accepts dimensions of triangle/rectangle and display calculated area. Implement dynamic binding for given case study.]




import java.util.*;
abstract class shape
{
double val1,val2;
void input()
{
Scanner s =new Scanner(System.in);
System.out.println("Enter the first value");
val1= s.nextDouble();
System.out.println("Enter the second value");
val2= s.nextDouble();
}
abstract void compute_area();
}
class Triangle extends shape
{
void compute_area()
{
double area;
area = 0.5 * val1 * val2;
System.out.println("--Calculate Traingle Area--");
System.out.println("Traingle area:" + area);
}
}
class Rectangle extends shape
{
void compute_area()
{
double area;
area = val1*val2;
System.out.println("--Calculate Rectangle Area--");
System.out.println(" Rectangle area"+ area);
}
}
class Dynamic
{
public static void main(String []args)
{
shape s;
Triangle t= new Triangle();
Rectangle r = new Rectangle();
s=t;
s.input();
s.compute_area();
s=r;
s.input();
s.compute_area();
}
}
