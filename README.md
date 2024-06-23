Program1.Write a C++ program to find the sum of all the natural numbers from 1 to n. 
#include <iostream>
using namespace std;
voidnaturalsum(int n)
  {
int sum=0, i;
for(i=1;i<=n;i++)
sum=sum+i;
cout<<"sum of first "<< n <<" natural numbers : "<<sum<<endl;
    }
int main()
  {
int n;
cout<<"enter the value of n:  ";
cout<<endl;
cin>>n;
naturalsum(n);
}


. Write a C++ program to sort the elements in ascending and descending order.
#include <iostream>
using namespace std;
//method to sort elements in ascending order
void ascending(int a[],int n)
    {
	inti,j,temp;
	for(i=0;i<n-1;i++)
	 {
		for(j=0;j<n-1-i;j++)
		  {
		if(a[j]>a[j+1])
		{
			temp=a[j];
			a[j]=a[j+1];
			a[j+1]=temp;
  }
   }
  }
    }
//method to sort elements in descending order
void descending(int a[],int n)
    {
	inti,j,temp;
	for(i=0;i<n-1;i++)
	  {
		for(j=0;j<n-1-i;j++)
		  {
			if(a[j]<a[j+1])
		 {
			temp=a[j];
			a[j]=a[j+1];
			a[j+1]=temp;
		}
		   }
	   }
    }

//main method
int main() 
{

int a[10],n, i,choice;
charch;
do
    {
		cout<<"enter the size of the array";
		cin>>n;
		cout<<"enter the elements";
		for(i=0;i<n;i++)
		cin>>a[i];
cout<<"elements before sorting";
		cout<<endl;
		for(i=0;i<n;i++)
		cout<<a[i]<<" ";
		cout<<endl;
		cout<<"1. ascending order sort  2. descending order sort";
		cout<<endl<<"enter your choice:  ";
		cin>>choice;
		switch (choice)
		  {
			case 1:
				cout<<"elements after sorting";
				ascending(a,n);
				cout<<endl;
				cout<<endl;
				for(i=0;i<n;i++)
					cout<<a[i]<<" ";
				break;
			case 2:    
				cout<<"elements after sorting";
				descending(a,n);
				cout<<endl;
				cout<<endl;
				for(i=0;i<n;i++)
					cout<<a[i]<<" ";
				break;
			default:  	cout<<"invalid option";               
		  }
cout<<endl<<"do u want to continue y/n";
cin>>ch;
}while(ch=='y'|| ch=='Y');
cout<<"bye";
}

:Write a C++ program to swap 2 values by writing a function that uses call by reference technique 
#include <iostream>
using namespace std;
void swap(int&p,int&q)
{
int temp;
temp=p;
    p=q;
    q=temp;
}
int main()
{
inta,b;
cout<<"enter the two numbers"<<endl;
cin>>a>>b;
cout<<"Elements before swapping"<<endl;
cout<<"a= "<<a<<endl;
cout<<"b= "<<b<<endl;
swap(a,b);
cout<<"Elements after swapping"<<endl;
cout<<"a= "<<a<<endl;
cout<<"b= "<<b<<endl;
return 0;
}


Call by address program
#include <iostream>
using namespace std;
void swap(int *p,int *q)
{
int temp;
temp=*p;
    *p=*q;
    *q=temp;
}

int main()
{
inta,b;
cout<<"enter the two numbers"<<endl;
cin>>a>>b;
cout<<"elements before swapping"<<endl;
cout<<"a= "<<a<<endl;
cout<<"b= "<<b<<endl;
swap(&a,&b);
cout<<"elements after swapping"<<endl;
cout<<"a= "<<a<<endl;
cout<<"b= "<<b<<endl;

return 0;
}

Write a C++ program to demonstrate function overloading for the following prototypes. add(int a, int b)  add(double a, double b) 

#include <iostream>
using namespace std;
void add(intp,int q)
    {
int c;
        c=p+q;
cout<< c;
    }
void add(double p,double q)
    {
double c;
        c=p+q;
cout<< c;
    }
int main()
    {
inta,b;
doublex,y;
cout<<"enter two integer numbers";
cin>>a>>b;
cout<<a<<"+"<<b<<"=";
add(a,b);
cout<<endl<<"enter two double numbers";
cin>>x>>y;
cout<<x<<"+"<<y<<"=";
add(x,y);
return  0;
     }

. Create a class named Shape with a function that prints "This is a shape". Create another class named Polygon inheriting the Shape class with the same function that prints "Polygon is a shape". Create two other classes named Rectangle and Triangle having the same function which prints "Rectangle is a polygon" and "Triangle is a polygon" respectively. Again, make another class named Square having the same function which prints "Square is a rectangle".Now, try calling the function by the object of each of these classes. 
#include <iostream>
using namespace std;
class Shape
{
public:
void display()
    {
cout<<endl<< "This is a shape";
    }
};
classPolygon:public Shape
{
public:
void display()
    {
       Shape::display();
cout<<endl<< "Polygon is a shape";
    }

}; 
classRectangle:public Polygon
{
public:
void display()
    {
               Shape::display();
cout<<endl<<"Rectangle is a Polygon ";
    }

}; 
classTriangle:public Polygon
{
public:
void display()
    {
               Shape::display();
cout<<endl<<"Triangle is a Polygon ";
    }

};
classSquare:public Rectangle
{
public:
void display()
    {
               Shape::display();
cout<<endl<<"Square is Rectangle  ";
    }

};
int main() 
{
        Polygon p;
        Rectangle r;
        Triangle t;
        Square sq;
p.display();
r.display();
t.display();
sq.display();
return 0;
 }

 #include <iostream>
using namespace std;
class Vehicle
{
public:void vehicle()
{
cout<<"i am a vehicle"<<endl;
}
};
class FourWheeler:public Vehicle
{
public:voidfourwheeler()
{
cout<<"i have four wheels"<<endl;
}
};
class Car:public FourWheeler
{
public:void car()
{
cout<<"i am a car"<<endl;
}
};
int main()
{
Car c;
c.vehicle();
c.fourwheeler();
c.car();
return 0;
}

#include <iostream>
using namespace std;
int main()
{
fstream file;
file.open("sample.txt",ios::out);
if(!file)
{
cout<<"Error in creating file!!!"<<endl;
return 0;
}
cout<<"File created successfully."<<endl;
file<<"ABCD.";
file.close();
file.open("sample.txt",ios::in);
if(!file)
{
cout<<"Error in opening file!!!"<<endl;
return 0;
}
charch; 
cout<<"File content: ";
while(!file.eof())
{
file>>ch; 
cout<<ch;
}
file.close();
return 0;
}

#include <iostream>
using namespace std;
void divide(inta,int b)
{
if(b!=0)
{
int c=a/b;
cout<<endl<<"result="<<c;
}
else
throw(b);
}
int main()
{
try
{
divide(4,3);
divide(4,0);
}
catch(int e)
{
cout<<endl<<"divide by zero";
}
return 0;
}

#include <iostream>
using namespace std;
voidcheck_array_index(int a[10],intn,inti)
{
try
{
if (i>=0 &&i<n)
cout<<"the element at position "<<i<<" is: "<<a[i];
else
throwi;
}
catch(int e)
{
cout<<endl<<"array index out of bound";
}
}
int main()
{
int a[10],n,pos;
cout<<"enter the size of an array : ";
cin>>n;
cout<<"enter the elements of an array "<<endl;
for(inti=0;i<n;i++)
cin>>a[i];
cout<<"enter the index of element in an array : ";
cin>>pos;
check_array_index( a, n, pos);
return 0;
}


