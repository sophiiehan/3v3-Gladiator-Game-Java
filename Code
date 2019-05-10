import java.util.Scanner;


class Main {
  public static void main(String[] args) {
    String P = "";
    String E = "";
    Scanner kb = new Scanner(System.in);
    Gladiator p1 = new Gladiator();
    Gladiator p2 = new Gladiator();
    Gladiator p3 = new Gladiator();
    Gladiator currentPlayer = new Gladiator();
    Gladiator e1 = new Gladiator();
    Gladiator e2 = new Gladiator();
    Gladiator e3 = new Gladiator();
    Gladiator currentEnemy = new Gladiator();
    while(true){
       Gladiator[] players= new Gladiator[] {p1,p2,p3};
       Gladiator[] enemies= new Gladiator[] {e1,e2,e3};
      //Printing enemy health and player health
      System.out.println("Player 1: " + p1.getHealth());
      System.out.println("Player 2: " + p2.getHealth());
      System.out.println("Player 3: " + p3.getHealth());
      System.out.println("Enemy 1: " + e1.getHealth());
      System.out.println("Enemy 2: " + e2.getHealth());
      System.out.println("Enemy 3: " + e3.getHealth());
      //Check if game over
      if (e1.getHealth() == "dead" && e3.getHealth() == "dead" && e2.getHealth() == "dead"){
        System.out.println("Game Over");
        break;
      }
      //User chooses a Player
      System.out.println("Choose a player to attack with: ");
      int a = kb.nextInt();
      if (a == 1){
        currentPlayer = p1;
        P = "1";
      }
      else if(a == 2){
        currentPlayer = p2;
        P = "2";
      }
      else if(a == 3){
        currentPlayer = p3;
        P = "3";
      }
      else{
        System.out.println("Not valid");
      }
      //User chooses an enemyy
       System.out.println("Choose an enemy to attack: ");
      int b = kb.nextInt();
      if (b == 1){
        currentEnemy = e1;
        E = "1";
      }
      else if(b == 2){
        currentEnemy = e2;
        E = "2";
      }
      else if(b == 3){
        currentEnemy = e3;
        E = "3";
      }
      else{
        System.out.println("Not valid");
      }

      //Actual attacking
      int Pdmg = currentPlayer.attack();
      int Edmg = currentEnemy.attack();
      currentEnemy.takeDmg(Pdmg);
      //Random enemy attacks random player
      currentPlayer = players[(int)(Math.random() *3)];
      currentEnemy = enemies[(int)(Math.random() *3)];
      //For the print statment
      String newE = "";
      String newP = "";
      if (currentEnemy == e1){
        newE = "1";
      }
      else if(currentEnemy ==e2){
        newE = "2";
      }
       else if(currentEnemy ==e3){
        newE = "3";
      }
      else{
        System.out.println("Not valid");
      }
      //******************************************
      currentPlayer = players[(int)(Math.random() *3)];
       if (currentPlayer == p1){
        newP = "1";
      }
      else if(currentPlayer ==p2){
        newP = "2";
      }
       else if(currentPlayer ==p3){
        newP = "3";
      }
      else{
        System.out.println("Not valid");
      }

      Edmg = currentEnemy.attack();
      currentPlayer.takeDmg(Edmg);
      System.out.println("Player " + P + " did " + Pdmg + " damage to Enemy " + E);
      System.out.println("Enemy " + newE + " did " + Edmg + " damage to Player " + newP);
    }
  }
}
