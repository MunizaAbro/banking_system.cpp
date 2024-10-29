# banking_system.cpp
This is a console-based banking system written in C++.<br> It allows users to: - Check their balance - Deposit money - Withdraw money

#include <iostream>
using namespace std;

int main(){
	
	double balance=0.0;
	int choice;
	
	do{
		cout<<" *welcome to simple bankng system* "<<endl;
		cout<<"1. check balance"<<endl;
		cout<<"2. deposite money"<<endl;
		cout<<"3. withdraw money"<<endl;
		cout<<"4. exit"<<endl;
		cout<<"enter your choice..."<<endl;
		cin>>choice;
		
		switch(choice){
			case 1:
				cout<<"your current balance is $"<<balance<<endl;
				break;
			
			case 2: {
				double deposite;
				cout<<"enter your amount to deposite : ";
				cin>>deposite;
				if(deposite>0){
					balance+=deposite;
					cout<<"you have successfully deposite your amount"<<deposite<<endl;
				}
				else{
					cout<<"invailed deposite amount"<<endl;
				}
				break;
			}
			case 3:{
				double withdraw;
				cout<<"enter the amount to withdraw: ";
				cin>>withdraw;
				if(withdraw> 0 && withdraw <= balance){
					balance-=withdraw;
					cout<<"you have successfully withdraw the amount"<<withdraw<<endl;
				}
				else{
					cout<<"invailed withdraw amount"<<endl;
				}
				break;
			}
			case 4:{
				cout<<"thank you for visiting the bank"<<endl;
				break;
				
				default:
					cout<<"invaild choice please try again "<<endl;
					break;
			}
			cout<<endl;
		
		}
			
	}
	while (choice != 4);
    return 0;
}
