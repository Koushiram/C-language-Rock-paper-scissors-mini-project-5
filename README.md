#include <stdio.h>

#include <stdlib.h>

#include <time.h>

int
main() {

  int playerChoice, computerChoice;

  // Seed the random number generator
  srand(time(0));

  // Get player's choice
  printf("Enter your choice (0 for Rock, 1 for Paper, 2 for Scissors): ");

  scanf("%d", & playerChoice);

  // Generate computer's choice
  computerChoice = rand() % 3;

  // Determine the winner
  if (playerChoice == computerChoice) {

   printf("It's a tie!\n");

  } else if ((playerChoice == 0 && computerChoice == 2) ||
    (playerChoice == 1 && computerChoice == 0) ||
    (playerChoice == 2 && computerChoice == 1)) {

  printf("You win!\n");

  } else {
    printf("Computer wins!\n");

  }

  return 0;

}
