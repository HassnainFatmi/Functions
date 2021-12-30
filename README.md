//Check whether a number is prime or not
#include <iostream>
using namespace std;
bool primeChecker(int x);
int main()
{
	int a;
	char op = 'y';
	bool pFlag;
	while (op == 'y')
	{
		cout << "Enter a number : ";
		cin >> a;
		if (a > 0)
		{
			pFlag = primeChecker(a);
			switch (pFlag)
			{
			case 0:
				cout << "It is not a prime number.\n";
				break;
			default:
				cout << "It is a prime number.\n";
				break;
			}
		}
		else
		{
			cout << "Error! the number must be a positive number>\n";
		}
		cout << "Do you want to countinue (y/n).";
		cin >> op;
	}
}
bool primeChecker(int x)
{
	bool flag = 1;
	for (int i = 2; i <= x / 2; i++)
	{
		if (x % i == 0)
		{
			flag = 0;
			break;
		}
	}
	return flag;
}
