/*
Qn:- Write a code 
(xFactorial + yFactorial = 10factorial)

and retuns the value of x and y in an array.
Use int[] solve10() as a sigsignature.








*/


public class Main {
  public static void main(String[] args) {
    int[] solution = solve10();

    if (solution != null) {
      System.out.println("x = " + solution[0]);
      System.out.println("y = " + solution[1]);
    } else {
      System.out.println("No solution found.");
    }
  }
  
  public static int[] solve10() {
    int[] solve10 = new int[2];
    int tenFactorial = 0;
    int x = 0;
    int y = 0;

    for (int i = 0; i <= 10; i++) {
      tenFactorial = tenFactorial * i;

      for (x = 1; x < 10; x++) {
        if (tenFactorial * x >= tenFactorial) {
          break;
        }

        for (y = 1; y < 10; y++) {
          if (tenFactorial * x + tenFactorial * y == tenFactorial) {
            solve10[0] = x;
            solve10[1] = y;
            return solve10;
          }
        }
      }
    }

    return null;
  }
}
