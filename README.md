package gupi;
import java.util.Scanner;

public class project {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        String[] questions = {
            "1. What is the capital of Bangladesh? (A. Dhaka, B. Bogura, C. Rajshahi, D. Dinajpur)",
            "2. What is 8 + 2? (A. 3, B. 4, C. 10, D. 6)",
            "3. What is the traditional food of Tangail? (A. ChamCham, B. Burger, C. Pizza, D. Chiken Fry )",
            "4. What is 15-9? (A. 14, B. 6, C. 11, D. 13)",
            "5. Which is a prime number? (A. 9, B. 6, C. 3, D. 12)"
        };

        char[] correctAnswers = {'A', 'C', 'A', 'B', 'C'};
        double score = 0;

        
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            System.out.print("Your answer (A/B/C/D): ");
            char answer = scanner.next().toUpperCase().charAt(0);

            if (answer == correctAnswers[i]) {
                score ++;
            } else {
                score --;
            }
        }

        System.out.printf("Your final score: %.2f\n", score);
        scanner.close();
    }
}
