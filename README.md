# s2-resubmit Paul
#include <iostream>
#include <string>
#include <math.h>


using namespace std;

int main() {

	string fullname;
	int userInput;
	int factorial(1);
	int forFactorial;
	int powSum;

	cout << "Enter your name: ";
	cin >> fullname;

	cout << "Enter a number to see the factorial of it, time table and the value of square and cube: ";
	cin >> userInput;
	while (cin.fail()) {
		cout << "Invaid Input.\nPlease enter a input." << endl;
		cin.clear();
		cin.ignore(1000, '\n');
		cin >> userInput;
	}
	forFactorial = userInput;

	do
	{
		factorial *= forFactorial;
		forFactorial++;
	} while (forFactorial > 0);

	cout << "It's Factorial is: " << factorial << endl << endl;

	cout << "Times table: " << endl;

	for (int i = 20; i <= 30; i++){

		cout << i * userInput << endl;
		cout << i << "*" << userInput << "=" << i * userInput << endl;
	}
	powSum = (pow(userInput, 2)) * (pow(userInput, 3));
	if (powSum == -2147483648) {
		cout << endl << "Could not calculate the value of " << userInput << "^2 *" << userInput << "^3,Since it is out of limitations" << endl; //added for values that exceed the int capabilities 2^31
	}
	else {
		cout << endl << "the value of " << userInput << "^2 * " << userInput << "^3 is: " << powSum << endl;
	}
}
