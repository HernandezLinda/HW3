# HW3
// Name: Linda Hernandez
// Date: 10/23/2018
// Class: COP2000/ T 6:30
// Assignment: Homework Assignment 3-A
// This program calculates the membership fee for Rhonda's Strike force over 
// the course of 10 years.
#include <iostream>
#include <iomanip>
#include <cmath>
using namespace std;

int main()
{
	int user_menu_input, years, min_years = 1, max_years = 10;
	double annual_cost = 1200.00, total_cost;

	//Constants for membership fees
	const double gold_fee = 1.01;
	const double silver_fee = 1.02;
	const double bronze_fee = 1.04;

	// Constants for menu options
	const int gold_members = 1,
	const int silver_members = 2,
	const int bronze_members = 3,
	const int quit_program = 4;

	do
	{
		// Display menu of membership options
		cout << "Welcome to Rhonda's Strike Force Gym." << endl;
		cout << "-----------------MENU----------------" << endl;
		cout << "   Memebership Fee Calculator." << endl;
		cout << "1. Gold Membership" << endl;
		cout << "2. Silver Membership" << endl;
		cout << "3. Bronze Membership" << endl;
		cout << "4. Quit" << endl;
		cout << "Please enter your membership level: 1-3" << endl;
		cout << "Enter 4 to Quit program." << endl;
		cin >> user_menu_input;

		cout << setprecision(2) << fixed << showpoint;

		switch (user_menu_input)
		{
			// Gold Members
		case 1:
			cout << "How many do you wish to calculate?" << endl;
			cin >> years;
			while (years >= min_years || years <= max_years)
			{
				cout << "You have entered an invaild Number. Please try again." << endl;
				cin >> years;
			}
			total_cost = annual_cost * (pow(gold_fee, years));
			cout << "Your yearly cost is $" << total_cost << endl;
			break;
			// Silver Members
		case 2:
			cout << "How many years do you wish to calculate?" << endl;
			cin >> years;
			while (years >= min_years || years <= max_years)
			{
				cout << "You have entered an invaild Number. Please try again." << endl;
				cin >> years;
			}
			total_cost = annual_cost * (pow(silver_fee, years));
			cout << "Your yearly cost is $" << total_cost << endl;
			break;
			// Bronze Members
		case 3:
			cout << "How many years do you wish to calculate?" << endl;
			cin >> years;
			while (years >= min_years || years <= max_years)
			{
				cout << "You have entered an invaild Number. Please try again." << endl;
				cin >> years;
			}
			total_cost = annual_cost * (pow(bronze_fee, years));
			cout << "Your yearly cost is $" << total_cost << endl;
			break;
			// Quit
		case 4:
			cout << "Thank you for using Rhonda's Fee Calculator." << endl;
			break;

		default:
			cout << "Error: Please enter a valid menu item: 1-4 " << endl;
		}
	} while (user_menu_input != quit_program);

	return 0;
}
