# simple-calculator
//============================================================================
// Name        : Simple Calculator.cpp
// Author      : 
// Version     :
// Copyright   : Your copyright notice
// Description : Hello World in C++, Ansi-style
//============================================================================

#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {

	int a, b;
	char choice;

	beginning:
	cout << "This is a simple calculator." << endl;
	cout << "Please enter two numbers." << endl;
	cout << "First number: " << endl;
	cin >> a;

	cout << "Second number: " << endl;
	cin >> b;

	cout << "We offer the basic four operations." << endl;
	cout << "+ - addition" << endl;
	cout << "- - subtraction" << endl;
	cout << "* - multiplication" << endl;
	cout << "/ - division" << endl;

	cout << "Please enter what operation you want to use: " << endl;
	cin >> choice;

	system("cls");

	switch (choice) {
		case '+':
			cout << a << " + " << b << " = " << (a + b) << endl;
			break;
		case '-':
			cout << a << " - " << b << " = " << (a - b) << endl;
			break;
		case '*':
			cout << a << " * " << b << " = " << (a * b) << endl;
			break;
		case '/':
			if (b)
			{
				cout << a << " / " << b << " = " << (a / b) << endl;
			}
			else
				cout << "The number cannot be divided by 0!" << endl;
			break;
		default:
			cout << "Please enter a valid operator." << endl;

	}

	char decision2;

	cout << "Do you want to use the calculator again?" << endl;
	cin >> decision2;

	if (decision2 == 'y' || decision2 == 'Y')
		goto beginning;
	else if (decision2 == 'n' || decision2 == 'N')
		cout << "Thanks for using my calculator! Have a nice day!" << endl;

	return 0;
}
