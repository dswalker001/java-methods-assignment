# Java Methods Assignment

This repository contains solutions to a Java programming assignment focusing on:
- Method decomposition
- Method calls
- Method overloading

---

## Question 1: executeGradeReport Method

### Description
The `executeGradeReport(double score)` method is a high-level method that manages the program flow by calling helper methods. It does not perform any calculations directly.

### Java Implementation

```java
public class GradeReport {

    public static void executeGradeReport(double score) {
        if (!validateScore(score)) {
            System.out.println("Invalid Score");
            return;
        }

        char grade = calculateLetterGrade(score);
        displayPerformanceMessage(grade);
    }

    public static boolean validateScore(double score) {
        return score >= 0 && score <= 100;
    }

    public static char calculateLetterGrade(double score) {
        if (score >= 80) {
            return 'A';
        } else if (score >= 70) {
            return 'B';
        } else if (score >= 60) {
            return 'C';
        } else if (score >= 50) {
            return 'D';
        } else {
           .out.println("Excellent performance!");
                break;
            case 'B':
                System.out.println("Very good performance.");
                break;
            case 'C':
                System.out.println("Good performance.");
                break;
            case 'D':
                System.out.println("Pass, but needs improvement.");
                break;
            default:
                🔹 STEP 3: Fix the Explanation Text

Make sure this text is **OUTSIDE the Java code block**:

```md
### Explanation
The `executeGradeReport` method coordinates lower-level helper methods by:
1. Validating the score
2. Calculating the letter grade
3. Displaying a performance message

This demonstrates how a high-level method manages program logic without performing calculations itself.
---

## Question 2: calculateClassAverage (Method Overloading)

### Description
This question demonstrates method overloading by defining multiple methods with the same name but different parameters.

### Java Implementation

```java
public class ClassAverage {

    // Version 1: Two scores
    public static double calculateClassAverage(double score1, double score2) {
        return (score1 + score2) / 2;
    }

    // Version 2: Three scores
    public static double calculateClassAverage(double score1, double score2, double score3) {
        return (score1 + score2 + score3) / 3;
    }

    // Version 3: Array of scores
    public static double calculateClassAverage(double[] scores) {
        double total = 0;

        for (double score : scores) {
            total += score;
        }

        return total / scores.length;
    }
}
