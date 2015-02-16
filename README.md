#include"stdafx.h"
#include<stdlib.h>
#include<stdio.h>
#include<conio.h>
#include<iostream>
#include<string>
using namespace std;


int	_tmain(int argc, _TCHAR* argv[])
{
	char cLetter = '0';
	char pass[11];
	int iCount = 0;
	cout << "Introduce a Password" << endl;
	while (cLetter != 13){
		cLetter = _getch();
		if (cLetter > 32 && iCount < 10){
			pass[iCount] = cLetter;
			cout << "*";
			iCount++;
		}
		else
			if (cLetter == 8 && iCount > 0){
				putchar(8);
				putchar(' ');
				putchar(8);
				iCount--;
			}

	}
	pass[iCount] = '\0';
	if (strcmp(pass, "CTN0452-9") == 0)
	
	cout << "\nBienvenido!";
	else
		cout << "\nLargo Intruzo!";
		

	_getch();
	return 0;
}
