# lotterygame
import java.util.Random;
import java.util.Scanner;


public class NewClass1 {
 
public static void main (String[] args) throws InterruptedException{
Scanner input = new Scanner(System.in);
Random random = new Random();

int aTries = 0;
int bTries = 0;
int cTries = 0;
int dTries = 0;
int eTries = 0;
int fTries = 0;
int chcTries = 0;
int ndTries = 0;
int choiceTries = 0;
int stTries = 0;
int nd;
int st;
int choice;
int a, b, c, d, e, f;
String chc;
System.out.println("Welcome to Lottery Game.");
Thread.sleep(1000);
System.out.println("Which game mode do you prefer?");
Thread.sleep(1000);
System.out.println("Press 1 for easy two.");
Thread.sleep(500);
System.out.println("Press 2 for 6 double digit.");
Thread.sleep(500);
do {System.out.print("(1/2): ");
choice = input.nextInt();
if (choice == 1)
{System.out.println("\nPlease take note that your choices only ranges from 1 to 30.");
Thread.sleep(500);
do {do {System.out.print("Please enter your 1st bet: ");
st = input.nextInt();
if (st < 1 || st > 30)
{System.out.println("Invalid input, please try again.");
} 
stTries++;
if (stTries >= 5) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (st < 1 || st > 30);

do{System.out.print("Please enter your 2nd bet: ");
nd = input.nextInt();
if (nd < 1 || nd > 30)
{System.out.println("Invalid input, please try again.");
} 
ndTries++;
if (ndTries >= 5) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (nd < 1 || nd > 30);

System.out.print("\nYour bets are: ");
Thread.sleep(500);
System.out.print(st+", ");
Thread.sleep(500);
System.out.println(nd+".");
do {System.out.print("Is this Correct? (Yes|No): ");
chc = input.next();
chc = chc.toLowerCase();
if (chc.equals("yes"))
{int x = random.nextInt(30) + 1;
int y = random.nextInt(30) + 1;
System.out.println("\nThe winning numbers are: ");
Thread.sleep(500);
System.out.print(x+", ");
Thread.sleep(500);
System.out.println(y+".");
Thread.sleep(500);
if (st != x && nd != y)
{System.out.println("Sorry, better luck next time!");
} else if(st == x && nd  != y)
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed the first number correct!");
System.out.println("You have won half of the prize!");
} else if(nd == y &&  st != x)
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed the second number correct!");
System.out.println("You have won half of the prize!");
} else 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed the numbers correct!");
}
} else if (chc.equals("no")) 
{System.out.println("\nPlease enter your bets again.");
Thread.sleep(500);
} else if (!chc.equals("yes") || !chc.equals("no"))
{System.out.println("Input invalid.");
}

chcTries++;
if (chcTries >= 5) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);
}
} while(!chc.equals("yes") && !chc.equals("no"));
} while(chc.equals("no"));
}else if (choice == 2) 
{System.out.println("\nPlease take note that your choices only ranges from 1 to 60");
Thread.sleep(500);
do {do {System.out.print("Please enter your 1st bet: ");
a = input.nextInt();
if (a < 1 || a > 60)
{System.out.println("Invalid input, please try again.");
} 
aTries++;
if (aTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (a < 1 || a > 60);
do{System.out.print("Please enter your 2nd bet: ");
b = input.nextInt();
if (b < 1 || b > 60)
{System.out.println("Invalid input, please try again.");
} 
bTries++;
if (bTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (b < 1 || b > 60);
do{System.out.print("Please enter your 3rd bet: ");
c = input.nextInt();
if (c < 1 || c > 60)
{System.out.println("Invalid input, please try again.");
} 
cTries++;
if (cTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (c < 1 || c > 60);
do{System.out.print("Please enter your 4th bet: ");
d = input.nextInt();
if (d < 1 || d > 60)
{System.out.println("Invalid input, please try again.");
} 
dTries++;
if (dTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (d < 1 || d > 60);
do{System.out.print("Please enter your 5th bet: ");
e = input.nextInt();
if (e < 1 || e > 60)
{System.out.println("Invalid input, please try again.");
} 
eTries++;
if (eTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (e < 1 || e > 60);
do{System.out.print("Please enter your 6th bet: ");
f = input.nextInt();
if (f < 1 || f > 60)
{System.out.println("Invalid input, please try again.");
} 
fTries++;
if (fTries >= 10) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while (f < 1 || f > 60);
System.out.print("\nYour bets are: ");
Thread.sleep(500);
System.out.print(a+", ");
Thread.sleep(500);
System.out.print(b+", ");
Thread.sleep(500);
System.out.print(c+", ");
Thread.sleep(500);
System.out.print(d+", ");
Thread.sleep(500);
System.out.print(e+", ");
Thread.sleep(500);
System.out.println(f+".");
Thread.sleep(500);
do {System.out.print("Is this Correct? (Yes|No): ");
chc = input.next();
chc = chc.toLowerCase();
if (chc.equals("yes"))
{int x = random.nextInt(60) + 1;
int y = random.nextInt(60) + 1;
int z = random.nextInt(60) + 1;
int v = random.nextInt(60) + 1;
int w = random.nextInt(60) + 1;
int u = random.nextInt(60) + 1;
System.out.println("\nThe winning numbers are: ");
Thread.sleep(1000);
System.out.print(x+", ");
Thread.sleep(500);
System.out.print(y+", ");
Thread.sleep(500);
System.out.print(z+", ");
Thread.sleep(500);
System.out.print(v+", ");
Thread.sleep(500);
System.out.print(w+", ");
Thread.sleep(500);
System.out.println (u+".");
Thread.sleep(500);
if (a == x && b == y && c == z && d == v && e == w && f == u) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed all numbers correct!");
System.out.println("You have won the jackpot prize!");
} else if (a == x && b == y && c == z && d == v && e == w) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed the first five numbers correct!");
System.out.println("You have won a large prize!");
} else if (b == y && c == z && d == v && e == w && f == u) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed the last five numbers correct!");
System.out.println("You have won a large prize!");
} else if ((a == x && b == y && c == z && d == v) || (b == y && c == z && d == v && e == w) || (c == z && d == v && e == w && f == u)) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed four numbers correct!");
System.out.println("You have won a medium prize!");
} else if ((a == x && b == y && c == z) || (b == y && c == z && d == v) || (c == z && d == v && e == w) || (d == v && e == w && f == u)) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed three numbers correct!");
System.out.println("You have won a small prize!");
} else if (a == x || b == y || c == z || d == v || e == w || f == u) 
{System.out.println("Congratulations!");
Thread.sleep(500);
System.out.println("You have guessed at least one number correct!");
System.out.println("You have won a consolation prize!");
} else 
{System.out.println("Sorry, better luck next time!");
}
} else if (chc.equals("no")) 
{System.out.println("\nPlease enter your bets again.");
Thread.sleep(500);
} else if (!chc.equals("yes") || !chc.equals("no"))
{System.out.println("Input invalid.");}

chcTries++;
if (chcTries >= 5) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
} while(!chc.equals("yes") && !chc.equals("no"));
} while(chc.equals("no"));
} else 
{System.out.println("Invalid input, please try again.");}
choiceTries++;
if (choiceTries >= 5) 
{System.out.println("\nUser attempts too many. \n\nProgram ended.");
System.exit(0);}
}while (choice != 1 && choice != 2);



}
}
    






   
