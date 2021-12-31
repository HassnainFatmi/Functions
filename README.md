//Program to calculate the LCM and HCF of two numbers using functions
#include <iostream>
using namespace std;
int lcm(int a, int b);
int hcf(int a, int b);
int main()
{
	int x, y, max, min;
	cout << "Enter two numbers : ";
	cin >> x >> y;
	max = x > y ? x : y;  //determination of maximum of two numbers
	min = x < y ? x : y;  //determination of minimum of two numbers
	cout << "The LCM of " << x << " and " << y << " is " << lcm(max,min) << endl;
	cout << "The HCF of " << x << " and " << y << " is " << hcf(max,min) << endl;
}

/*below function takes two numbers and finds the smallest multiple 
of the highest number which  is divisible it by smaller number 
and returns it to main function*/
int lcm(int a, int b)
{
	for (int i = 1; i >= a; i++)
	{
		if ((a * i) % b == 0)
		{
			return a * i;
		}
	}
}
	int hcf(int a, int b)
	{
		for (int i = b; i >= b; i--)
		{
			if (b % i == 0 && a % i == 0)
			{
				return i;
			}
		}
	}
