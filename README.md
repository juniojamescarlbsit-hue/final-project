# final-project
Junio,James Carl S.
bsit 2-j
clude <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));               
    int secret = rand() % 100 + 1;  
    int guess = 0;
    int attempts = 0;

    cout << "=== Guess the Number Game ===\n";
    cout << "I have chosen a number between 1 and 100.\n";

    while (guess != secret) {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess > secret) {
            cout << "Too high! Try again.\n";
        } else if (guess < secret) {
            cout << "Too low! Try again.\n";
        } else {
            cout << "Correct! You guessed the number in " 
                 << attempts << " attempts.\n";
        }
    }

    return 0;
}
