import java.util.*;

interface Player {
    String getName();
    void setName(String newName);
}
class UserNAME implements Player {
    private String name;
    public String getName() {
        return name;
    }
    public void setName(String newName) {
        this.name = newName;
    }
}
interface GameMode {
    void play();
    void performAction(String action);
}
class StoryMode implements GameMode {
    private Scanner sc;
    public StoryMode(Scanner sc) {
        this.sc = sc;
    }
    public void play() {
        System.out.println("\nYou woke up alone deep within the forest of the inhabited island.");
        System.out.println("\nChoice 1: Venture Deeper into the Forest");
        System.out.println("Choice 2: Follow the Sounds of Wildlife");
        System.out.println("Choice 3: Climb a Tree to Survey the Area");
        System.out.print("\nEnter your choice: ");
        int storyChoice = sc.nextInt();
        switch (storyChoice) {
            case 1:
                System.out.println("\nAs you venture deeper into the unfamiliar terrain, the dense foliage and looming shadows make it clear that danger lurks in every corner.");
                System.out.println("A fork in the path forces a decision. ");
                System.out.println("\nChoice 1: Take the Left Path");
                System.out.println("Choice 2: Take the Right Path");
                System.out.println("Choice 3: Climb a Small Hill for a Better View");
                System.out.print("\nEnter your choice: ");
                int choice1 = sc.nextInt();
                handleChoice1Endings(choice1);
                break;
            case 2:
                System.out.println("\nAs you follow the sounds of wildlife, they guide you to a clearing with a hidden pond.");
                System.out.println("However, the serene setting holds unexpected surprises.");
                System.out.println("\nChoice 1: Spot a Hidden Campsite");
                System.out.println("Choice 2: Encounter a Friendly Forest Dweller");
                System.out.println("Choice 3: Hear Distant Chanting");
                System.out.print("\nEnter your choice: ");
                int choice2 = sc.nextInt();
                handleChoice2Endings(choice2);
                break;
            case 3:
                System.out.println("\nAscending a sturdy palm tree, you gain a vantage point, revealing three distinct features in different directions.");
                System.out.println("\nChoice 1: Spot a Distant Village");
                System.out.println("Choice 2: Observe a Mysterious Structure");
                System.out.println("Choice 3: Identify a Clearing with a Helipad");
                System.out.print("\nEnter your choice: ");
                int choice3 = sc.nextInt();
                handleChoice3Endings(choice3);
                break;
        }
    }
    private void handleChoice1Endings(int choice) {
        switch (choice) {
            case 1:
                System.out.println("--------------------------------------------");
                System.out.println("\nDrawn by the faint sound of waves, you follow the left path, hoping it leads to a beach or some form of refuge.");
                System.out.println("\nEnding: Following the sound, you discover a desolate beach where remnants of the deadly game are scattered. \nThe haunting realization sets in that you're not alone, and other participants might be watching your every move.");
                performAction("You got stabbed at the foot by a forgotten piece of technology that is buried in the sand.");
                break;
            case 2:
                System.out.println("--------------------------------------------");
                System.out.println("\nOpting for the right path, you follow a trail marked by unsettling symbols. The hope is that it leads to answers or a way off the island.");
                System.out.println("\nEnding: The trail takes you to a mysterious clearing where remnants of the deadly game's challenges are evident. \nIt becomes apparent that escape won't be easy, and every step must be taken with caution.");
                performAction("You discovered a hidden compartment in the clearing, containing a cache of supplies and a cryptic note.");
                break;
            case 3:
                System.out.println("--------------------------------------------");
                System.out.println("\nSpotting a small hill nearby, you choose to climb it for a better view, hoping to gain insights into the island's mysteries.");
                System.out.println("\nEnding: From the elevated position, you see an abandoned campsite where your friends might have been. \nThe realization of their potential fate intensifies the urgency to navigate the island's dangers.");
                performAction("a blood-stained journal was found revealing snippets of writings about struggles, hinting at encounters with mysterious entities and the importance of a specific landmark on the island.");
                break;
        }
    }
    private void handleChoice2Endings(int choice) {
        switch (choice) {
            case 1:
                System.out.println("--------------------------------------------");
                System.out.println("\nBeside the pond, you discover a hidden campsite with signs of recent human activity. The remnants suggest your friends might have been here.");
                System.out.println("\nEnding: Investigating the campsite, you find clues left by your friends, indicating they faced challenges and left in a hurry. \nThe island's dangers become more apparent as you continue your search.");
                performAction("you caught a glimpse of a shadowy figure behind a tree.");
                break;
            case 2:
                System.out.println("--------------------------------------------");
                System.out.println("\nA mysterious figure, dressed in cryptic attire, approaches you. Claiming to be an island dweller with insights into the deadly game, they offer guidance but also warn of lurking dangers.");
                System.out.println("\nEnding: The island dweller guides you along a seemingly safe path, but as night falls, their demeanor changes. \nTrust becomes a dangerous game as the island's true threats are revealed.");
                performAction("you noticed that the island dweller's behavior becomes increasingly erratic.");
                break;
            case 3:
                System.out.println("--------------------------------------------");
                System.out.println("\nApproaching the pond, you hear rhythmic chanting from the heart of the island. The sounds hint at some form of organized human activity.");
                System.out.println("\nEnding: Investigating the chanting, you discover a group of participants gathering for the next deadly challenge. \nThe island's rules become clearer, and you must decide whether to confront the danger or evade it.");
                performAction("you found a hidden parchment detailing the island's rules and the consequences of non-compliance.");
                break;
        }
    }
    private void handleChoice3Endings(int choice) {
        switch (choice) {
            case 1:
                System.out.println("--------------------------------------------");
                System.out.println("\nIn the northwest, you spot a cluster of makeshift shelters. Smoke rises into the sky, indicating human activity.");
                System.out.println("\nEnding: Following the trail, you reach the village, where other participants reveal the game's ominous nature. \nThe village becomes a hub for alliances and betrayals in the deadly game.");
                performAction("you approached other participants with the intention of ???.");
                break;
            case 2:
                System.out.println("--------------------------------------------");
                System.out.println("\nTo the northeast, you notice an ancient structure covered in vines. Investigating could lead to discovering hidden secrets or encountering other players.");
                System.out.println("\nEnding: Investigating the ancient structure, you unwittingly trigger an ancient mechanism that unveils a clue about the deadly game's origins. \nKnowledge becomes a double-edged sword as you uncover the island's dark history.");
                performAction("within the hidden cave you saw drawings that narrate a tale of a cursed island.");
                break;
            case 3:
                System.out.println("--------------------------------------------");
                System.out.println("\nIn the south, you identify a large clearing with a helipad marked on the ground. It seems like a man-made construction in the heart of the island.");
                System.out.println("\nEnding: As you explore the clearing, you discover it was a potential extraction point. \nThe realization that escape is possible intensifies the stakes of the deadly game.");
                performAction("far away from where you stand, you saw a hidden building that looks modern and out of place.");
                break;
        }
    }
    public void performAction(String action) {
        System.out.println("\nPerforming action: " + action);
    }
}
class SurvivalMode implements GameMode {
    private String un;
    public SurvivalMode(String un) {
        this.un = un;
    }
    static int Punch = 10;
    static int Slash = 15;
    static int Throw = 20;
    static int CH = 250;
    static int MA = 500;
    static int Deb = 1000;
    static int Mix = 1500;
    static int lastChoice = -1;
    static int playerPoints = 100;
    static int playerAttackCount = 0;
    static Random random = new Random();
    static boolean isOutOfBounds(int num) {
        return num < 1 || num > 3;
    }
    static void decrementCH(int choice) {
        CH -= getAttackValue(choice);
    }
    static void decrementMA(int choice) {
        MA -= getAttackValue(choice);
    }
    static void decrementDeb(int choice) {
        Deb -= getAttackValue(choice);
    }
    static void decrementMix(int choice) {
        Mix -= getAttackValue(choice);
    }
    static int getAttackValue(int choice) {
        switch (choice) {
            case 1:
                return Punch;
            case 2:
                return Slash;
            case 3:
                return Throw;
            default:
                return 0;
        }
    }
    private String getAttackType(int choice) {
        switch (choice) {
            case 1:
                return "Punch";
            case 2:
                return "Slash";
            case 3:
                return "Throw";
            default:
                return "Unknown";
        }
    }
    @Override
    public void play() {
        try (Scanner scanner = new Scanner(System.in)) {
            while (CH > 0) {
                System.out.println("\n\nPunch: " + Punch + ", Slash: " + Slash + ", Throw: " + Throw + "\nEnemy: " + CH);
                int userChoice = 0;
                while (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                    System.out.print("Choose a number (1-3): ");
                    userChoice = scanner.nextInt();
                    if (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                        System.out.println("Out of bounds or same choice as last time! Choose again.");
                    }
                }
                lastChoice = userChoice;
                decrementCH(userChoice);
                playerAttackCount++;
                if (playerAttackCount % 5 == 0) {
                    int enemyAttackPoints = random.nextInt(5) + 5;
                    performAction("The Enemy attacks you with " + enemyAttackPoints + " hit points!");
                    System.out.println("\nPlayer points after enemy attack: " + (playerPoints -= enemyAttackPoints));
                    if (playerPoints <= 0) {
                        System.out.println("Game over. You DIED");
                        return;
                    }
                } else {
                    performAction("You have attacked with " + getAttackType(userChoice) + " injuring the Enemy with " + getAttackValue(userChoice) + " attack points.");
                }
            }
            System.out.println("\nYou have defeated the Crazed Humans. You may continue to the next stage!\n");
            playerPoints += 25;
            while (MA > 0) {
                System.out.println("\n\nPunch: " + Punch + ", Slash: " + Slash + ", Throw: " + Throw + "\nEnemy: " + MA);
                int userChoice = 0;
                while (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                    System.out.print("Choose a number (1-3): ");
                    userChoice = scanner.nextInt();
                    if (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                        System.out.println("Out of bounds or same choice as last time! Choose again.");
                    }
                }
                lastChoice = userChoice;
                decrementMA(userChoice);
                playerAttackCount++;
                if (playerAttackCount % 5 == 0) {
                    int enemyAttackPoints = random.nextInt(10) + 5;
                    performAction("The Enemy attacks you with " + enemyAttackPoints + " hit points!");
                    System.out.println("\nPlayer points after enemy attack: " + (playerPoints -= enemyAttackPoints));
                    if (playerPoints <= 0) {
                        System.out.println("Game over. You DIED");
                        return;
                    }
                } else {
                    performAction("You have attacked with " + getAttackType(userChoice) + " injuring the Enemy with " + getAttackValue(userChoice) + " attack points.");
                }
            }
            playerPoints += 50;
            System.out.println("\nYou have defeated the Mutated Animals. You may continue to the next stage!\n");
            while (Deb > 0) {
                System.out.println("\n\nPunch: " + Punch + ", Slash: " + Slash + ", Throw: " + Throw + "\nEnemy: " + Deb);
                int userChoice = 0;
                while (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                    System.out.print("Choose a number (1-3): ");
                    userChoice = scanner.nextInt();
                    if (isOutOfBounds(userChoice) || userChoice == lastChoice) {
                        System.out.println("Out of bounds or same choice as last time! Choose again.");
                    }
                }
                lastChoice = userChoice;
                decrementDeb(userChoice);
                playerAttackCount++;
                if (playerAttackCount % 5 == 0) {
                    int enemyAttackPoints = random.nextInt(15) + 5;
                    performAction("The Enemy attacks you with " + enemyAttackPoints + " hit points!");
                    System.out.println("\nPlayer points after enemy attack: " + (playerPoints -= enemyAttackPoints));
                    if (playerPoints <= 0) {
                        System.out.println("Game over. You DIED");
                        return;
                    }
                } else {
                    performAction("You have attacked with " + getAttackType(userChoice) + " injuring the Enemy with " + getAttackValue(userChoice) + " attack points.");
                }
            }
            System.out.println("\nCongratulations! You have survived all challenges in Survival Mode.\n");
        }
    }
    public void performAction(String action) {
        System.out.println("\nPerforming action: " + action);
    }
}
class GameManager {
    void startGame() {
        System.out.println("\n\nYou started this game...");
    }
    void endGame() {
        System.out.println("\n--------------------------------------------");
        System.out.println("\nTo be continued in Beta Version. Thank you for playing!");
    }
}
public class Game {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        UserNAME u = new UserNAME();
        System.out.println("Press 'S' to Start & 'Q' to Quit.");
        System.out.print("\nChoose your Destiny: ");
        String choice2 = sc.next();
        if (choice2.equalsIgnoreCase("s")) {
            GameManager gameManager = new GameManager();
            gameManager.startGame();
            System.out.println("\n\nThere's no going back...\n\n\n");
            String requiredKey1 = "y";
            String choice1;
            do {
                System.out.print("Let's play? You can't say no. (y/y): ");
                choice1 = sc.next();
            } while (!choice1.trim().equalsIgnoreCase(requiredKey1));
            System.out.print("\nUserName: ");
            String un = sc.next();
            u.setName(un);
            String requiredKey = "p";
            String choice;
            do {
                System.out.print("\nPress P to Play, " + u.getName() + ": ");
                choice = sc.next();
            } while (!choice.trim().equalsIgnoreCase(requiredKey));
            System.out.println("\nChoose your Game Mode:  ");
            System.out.println("1.) Story \n2.) Survival");
            int gameModeChoice;
            do {
                try {
                    System.out.print("Enter your choice: ");
                    gameModeChoice = sc.nextInt();
                } catch (InputMismatchException e) {
                    System.out.println("Invalid input. Please enter a valid option.");
                    sc.next(); 
                    gameModeChoice = 0; 
                }
            } while (gameModeChoice < 1 || gameModeChoice > 2);
            GameMode gameMode;
            if (gameModeChoice == 1) {
                gameMode = new StoryMode(sc);
                gameMode.play();
            } else {
                gameMode = new SurvivalMode(un);
                gameMode.play();
            }
            gameManager.endGame();
        }
        sc.close();
    }
}
