#include<iostream>
#include<cmath>
using namespace std;
class person
{
	public:
		char name[20];
		int code;
		public:
		person()
		{
			cout<<"ENTER NAME: ";
			cin>>name;
			cout<<"ENTER CODE: ";
			cin>>code;
		}
		~person()
		{
			cout<<"\nDESRUCTOR CALLED.....";
		}
};
class account:virtual public person
{
	public:
		int pay;
		void setpay()
		{
			cout<<"ENTER PAY: ";
			cin>>pay;
		}
};
class admin:virtual public person
{
	public:
		int experience;
		void setexp()
		{
			cout<<"ENTER YRS OF EXPERIENCE: ";
			cin>>experience;
		}
};
class master:public account,public admin
{
	public:
		void display()
		{
			cout<<"NAME: "<<name<<endl;
			cout<<"CODE: "<<code<<endl;
			cout<<"EXPERIENCE: "<<experience<<" YEARS"<<endl;
			cout<<"PAY: "<<pay;
		}
		friend void compare(class  master&,class master&);
		void operator-(class master&);
};
void compare(class master &m,class master &m1)
{
	if(m.pay>m1.pay)
	{
		cout<<m.name<<" HAS HIGHER PAY."<<endl;
	}
	else
	{
		cout<<m1.name<<" HAS HIGHER PAY."<<endl;
	}
}
void master::operator-(class master&x)
{
	cout<<"DIFFERENCE IN PAYS: "<<abs(pay-x.pay)<<endl;
}
template<class T> 
class Vector
{
	T v[10];
	int size;
	public:
		Vector()
		{
			size=0;
		}
		void create()
		{
			int i,ch;
			T value;
			do
			{
				cout<<"\nENTER THE VALUE: ";
				cin>>value;
				v[size]=value;
				size++;
				cout<<"\nDO YOU WANT TO ADD ELEMENTS? ";
				cin>>ch;
			}while(ch==1);
		}
		void modify()
		{
			int k;
			T n;
			cout<<"\nENTER INDEX FOR MODIFICATION: ";
			cin>>k;
			cout<<"\nENTER VALUE: ";
			cin>>n;
			v[k]=n;
		}
		void multiply()
		{
			int k;
			cout<<"\nENTER SCALAR: ";
			cin>>k;
			for(int i=0;i<size;i++)
			{
				v[i]=v[i]*k;
			}
		}
		void display()
		{
			cout<<"\nSIZE OF VECTOR IS: "<<size;
			cout<<"\nELEMENTS ARE: "<<endl;
			cout<<"(";
			for(int i=0;i<size;i++)
			{
				cout<<v[i]<<",";
			}
			cout<<")";
		}
};
int main()
{
	master m,m1;
	m.setexp();
	m.setpay();
	m.display();
	m1.setpay();
	m1.setexp();
	m1.display();
	compare(m,m1);
	m-m1;
	int c;
	Vector<int>obj;
	do
	{
		cout<<"\n 1.CREATE \n 2.MODIFY \n 3.MULTIPLY \n 4.DISPLAY \n";
		cout<<"ENTER CHOICE: ";
		cin>>c;
		switch(c)
		{
			case 1:
				obj.create();
				break;
			case 2:
				obj.modify();
				break;
			case 3:
				obj.multiply();
				break;
			case 4:
				obj.display();
				break;
			default:
				cout<<"\nINVALID.";
				break;
	    }
	}while(c!=0);
}
