import java.util.Scanner;

public class Main{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[] words = {"apple", "banana", "cherry", "date", "grape"};
        String wordToGuess = words[(int) (Math.random() * words.length)];
        char[] guessedWord = new char[wordToGuess.length()];
        boolean[] guessedLetters = new boolean[26];
        int attempts = 6;

        while (attempts > 0) {
            System.out.println("Word to guess: " + String.valueOf(guessedWord));
            System.out.println("Attempts left: " + attempts);
            System.out.print("Guess a letter: ");
            char guess = scanner.next().charAt(0);

            if (guessedLetters[guess - 'a']) {
                System.out.println("You already guessed that letter.");
                continue;
            }

            guessedLetters[guess - 'a'] = true;

            boolean found = false;
            for (int i = 0; i < wordToGuess.length(); i++) {
                if (wordToGuess.charAt(i) == guess) {
                    guessedWord[i] = guess;
                    found = true;
                }
            }

            if (!found) {
                attempts--;
                System.out.println("Incorrect guess.");
            }

            if (String.valueOf(guessedWord).equals(wordToGuess)) {
                System.out.println("Congratulations! You guessed the word: " + wordToGuess);
                break;
            }
        }

        if (attempts == 0) {
            System.out.println("You ran out of attempts. The word was: " + wordToGuess);
        }

        scanner.close();
        }
}
