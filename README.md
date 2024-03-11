# Task-2-Java
import java.util.Scanner; 

  

public class GradeCalculator { 

     

    public static String calculateGrade(double marks) { 

        if (marks >= 90) { 

            return "A+"; 

        } else if (marks >= 80) { 

            return "A"; 

        } else if (marks >= 70) { 

            return "B"; 

        } else if (marks >= 60) { 

            return "C"; 

        } else if (marks >= 50) { 

            return "D"; 

        } else { 

            return "Fail"; 

        } 

    } 

     

    public static void main(String[] args) { 

        Scanner scanner = new Scanner(System.in); 

         

        System.out.print("Enter the number of subjects: "); 

        int numSubjects = scanner.nextInt(); 

         

        double totalMarks = 0; 

        for (int i = 1; i <= numSubjects; i++) { 

            System.out.print("Enter marks obtained in subject " + i + ": "); 

            double subjectMarks = scanner.nextDouble(); 

            totalMarks += subjectMarks; 

        } 

         

        double averagePercentage = totalMarks / numSubjects; 

        String grade = calculateGrade(averagePercentage); 

         

        System.out.println("\nResults:"); 

        System.out.println("Total Marks: " + totalMarks); 

        System.out.printf("Average Percentage: %.2f%%\n", averagePercentage); 

        System.out.println("Grade: " + grade); 

         

        scanner.close(); 

    } 

} 
