# Lab-3: This program competes against a player in Rock, Paper, Scissors. After the player chooses either Rock, Paper, or Scissors, the program randomly generates its own choice that results in a win, loss, or draw for the player.

#include <iostream>
#include <cmath>
#include <iomanip>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{
	char choice;

	cout << "Enter your choice of Rock (R), Paper (P), or Scissors (S): ";
	cin >> choice;

	srand(time(0));
	int ranNum = rand() % 3;

	char comp;

	switch (ranNum)
	{

	case 0:
		comp = 'R';
		break;

	case 1:
		comp = 'P';
		break;

	case 2:
		comp = 'S';
		break;
	}

	switch (choice)
	{

	case 'R':
		if (comp == 'R')
			cout << "The computer is Rock. You are Rock too. It is a draw." << endl;

		if (comp == 'P')
			cout << "The computer is Paper. You are Rock. You lose." << endl;

		if (comp == 'S')
			cout << "The computer is Scissors. You are Rock. You win." << endl;
		break;

	case 'P':
		if (comp == 'R')
			cout << "The computer is Rock. You are Paper. You win." << endl;

		if (comp == 'P')
			cout << "The computer is Paper. You are Paper too. It is a draw." << endl;

		if (comp == 'S')
			cout << "The computer is Scissors. You are Paper. You lose." << endl;
		break;

	case 'S':
		if (choice == 'R')
			cout << "The computer is Rock. You are Scissors. You lose." << endl;

		if (choice == 'P')
			cout << "The computer is Paper. You are Scissors. You win." << endl;

		if (choice == 'S')
			cout << "The computer is Scissors. You are Scissors too. It is a draw." << endl;
		break;

	default:
		cout << "Invalid character, please enter Rock (R), Paper (P), or Scissors (S)" << endl;
	}

	cout << endl;
	system("PAUSE");
	return 0;
}
