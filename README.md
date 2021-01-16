# c-random-number-gen
code that selects a random number without modules.


This is a c++ random number generator!
Below is the code used to make it. As
you can see, no random-number modules were used
to make this! It was entirely made without modules!



#include <iostream>
#include <Windows.h> #okay there is ONE module. But this module is for taking in Key Input..
using namespace std;

int main()
{
	int random = 0; # the core var..
	bool runningInTheBackground = true;      #VERY self explanatory..
	while (runningInTheBackground == true) { #loop that adds 1 to the random variable and then checks if it's below 20. If it is, it will start at 0 again..
		random += 1;
		if (random >= 20)
		{
			random = 0;
		}
		if (GetKeyState('A'))  # if A key pressed, stop the loop and output the random variable's current value (or, the random number)..
		{
			runningInTheBackground = false; 
			cout << random;
		}
	}
}
