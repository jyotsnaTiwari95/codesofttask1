# codesofttask1
This program is based on the number guessing system , in this program a random number is choosed between 1 to 100 .
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    // Initialize random seed
    srand(time(0));

    // Generate a random number between 1 and 100
    int randomNumber = rand() % 100 + 1;
    int userGuess;
    bool guessedCorrectly = false;

    cout << "Guess the number (between 1 and 100): ";

    // Loop until the user guesses the correct number
    while (!guessedCorrectly) {
        cin >> userGuess;

        if (userGuess > randomNumber) {
            cout << "Too high. Try again: ";
        } else if (userGuess < randomNumber) {
            cout << "Too low. Try again: ";
        } else {
            cout << "Congratulations! You guessed the correct number." << endl;
            guessedCorrectly = true;
        }
    }

    return 0;
}

