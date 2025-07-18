# InternProject

    import java.util.Scanner;
    import java.util.Random;

    public class GuessTheNumber {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            Random random = new Random();
            boolean playAgain = true;
            int totalScore = 0;
            int round = 0;

            System.out.println("Welcome to the Number Guessing Game!");
            System.out.println("I'm thinking of a number between 1 and 100. Can you guess it?");

            while (playAgain) {
                int numberToGuess = random.nextInt(100) + 1;
                int attempts = 0;
                int maxAttempts = 10;
                boolean hasGuessed = false;

                while (attempts < maxAttempts) {
                    System.out.print("\nEnter your guess (" + (maxAttempts - attempts) + " attempts left): ");
                    int userGuess = scanner.nextInt();
                    attempts++;

                    if (userGuess == numberToGuess) {
                        System.out.println("Awesome! You guessed the correct number in " + attempts + " attempts.");
                        hasGuessed = true;
                        break;
                    } else if (userGuess < numberToGuess) {
                        System.out.println("Too low! Try a slightly higher number.");
                    } else {
                        System.out.println("Too high! Try a slightly lower number.");
                    }
                }

                if (!hasGuessed) {
                    System.out.println("Sorry! You've used all your attempts. The number was: " + numberToGuess);
                }

                round++;
                totalScore += hasGuessed ? (maxAttempts - attempts + 1) * 10 : 0;

                System.out.print("\nDo you want to play another round? (yes/no): ");
                scanner.nextLine(); // clear the buffer
                String response = scanner.nextLine().trim().toLowerCase();

                if (!response.equals("yes")) {
                    playAgain = false;
                }
            }

            System.out.println("\nGame Over!");
            System.out.println("Total Rounds Played: " + round);
            System.out.println("Your Final Score: " + totalScore + " points");
            System.out.println("Thanks for playing!");

            scanner.close();
        }
    }

