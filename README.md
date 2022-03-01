# Tracklabs-Project
/* ------------------------------------Nany Bhardwaj/Traclabsc++Internship/console app using c++//-------------------------------------------------------
   ------------------------------------EmployeeManagement using console app------------------------------------------------------------------------------  */  
#include<iostream>
#include<iomanip>
#include <bits/stdc++.h>
#define max 20
using namespace std;


class Mainbase
{
 
  public:
struct Management {       // Structure of Employee
    string name;
    long int code;
    string designation;
    int exp;
    int age;
};
int num;

Management arr[max], temparr[max],
    sortarr[max], sortarr1[max];
    
public:
	
void showMenu()
{
	int option;   // Input Options 
  cout << "-----------------------"<< " Management System"<< "-------------------------\n\n";
    cout << "Available Option\n\n";
    cout << "Build Table         (1)\n";
    cout << "Insert New Entry    (2)\n";
    cout << "Delete Entry        (3)\n";
    cout << "Search a Record     (4)\n";
    cout << "Exit                (5)\n";
    cin >> option;
   // Call function on the bases of the above option
    if (option == 1) {
        build();
    }
    else if (option == 2) {
        insert();
    }
    else if (option == 3) {
        deleteRecord();
    }
    else if (option == 4) {
        searchRecord();
    }
    else if (option == 5) {
        return;
    }
    else {
        cout << "Expected Option"<< " are 1/2/3/4/5";
        showMenu();}}
		
		// Function to build the given datatype
void build()
{
	int i;
    cout << "Build The Table\n";
    cout << "Maximum Entries can be "
         << max << "\n";
  
    cout << "Enter the number of "
         << "Entries required";
    cin >> num;
  
    if (num > 20) {
        cout << "Maximum number of "
             << "Entries are 20\n";
        num = 20;
    }
    cout << "Enter the following data:\n";
  
    for (int i = 0; i < num; i++) {
        cout << "Name ";
        cin >> arr[i].name;
  
        cout << "ID ";
        cin >> arr[i].code;
  
        cout << "Designation ";
        cin >> arr[i].designation;
  
        cout << "Experience ";
        cin >> arr[i].exp;
  
        cout << "Age ";
        cin >> arr[i].age;
    }
  cout << " following table can be constructed from the following details ";
  cout<<"\n\n------------------------------------------------------------\n";
   cout << "ID" <<setw(15)<<"Name" <<setw(10)<<"Age" <<setw(10)<<"Address"<<setw(15)<<"Experience"<< endl;
 
 for(i=0;i<num;i++)
    {
      cout << "\n"<< arr[i].code <<setw(15)<< arr[i].name <<setw(10)<< arr[i].age <<setw(10)<< arr[i].designation<<setw(15)<< arr[i].exp;
    }
    cout<<"\n\n------------------------------------------------------------\n";
	showMenu();}
	
	
// Function to insert the data into given data type
void insert()
{
    if (num < max) {
        int i = num;
        num++;
  
        cout << "Enter the information \n";
        cout << "Name ";
        cin >> arr[i].name;
  
        cout << "please enter your ID ";
        cin >> arr[i].code;
  
        cout << "Designation ";
        cin >> arr[i].designation;
  
        cout << "Experience ";
        cin >> arr[i].exp;
  
        cout << "Age ";
        cin >> arr[i].age;
    }
    else {
        cout << "Table Full\n";
    }showMenu();}
// Function to delete record at index i
void deleteIndex(int i)
{
    for (int j = i; j < num - 1; j++) {
        arr[j].name = arr[j + 1].name;
        arr[j].code = arr[j + 1].code;
        arr[j].designation
            = arr[j + 1].designation;
        arr[j].exp = arr[j + 1].exp;
        arr[j].age = arr[j + 1].age;
    }return;}
// Function to delete record
void deleteRecord()
{
    cout << "Enter the ID to Delete Record";
    int code;
    cin >> code;
    for (int i = 0; i < num; i++) {
        if (arr[i].code == code) {
            deleteIndex(i);
            num--;
            break;
        }} showMenu();
}
  
void searchRecord()
{
 cout << "Enter the Employee ID to Search Record";
  int code;
    cin >> code;
  for (int i = 0; i < num; i++) {
        // If the data is found
        if (arr[i].code == code) {
            cout << "Name " << arr[i].name << "\n";
  
            cout << "ID"<< arr[i].code << "\n";
  
            cout << "Designation "<< arr[i].designation << "\n";
  
            cout << "Experience "<< arr[i].exp << "\n";
  
            cout << "Age "<< arr[i].age;
            break;
        }}
		showMenu();
}
};

class Employee:public Mainbase
{

 emp.showMenu();

};

class Department:public Mainbase  
{public:
	Department(){
dep.showMenu();
}
};

int main()
{ 
public:
  Mainbase m;
	Employee emp;
	Department dep;
cout<< "*****management system*****"<<endl;
cout<<"choose one of the given portals to proceed";
cout<<"\n1. Employee management portal\n\n"<<"2.Department management portal\n\n";
int choice;
cin>>choice;
if(choice==1)
{
emp.Employee();
}
else
{
dep.Department();
	}
return 0;
}
