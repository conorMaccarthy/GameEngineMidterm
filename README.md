# GameEngineMidterm

Practical Midterm Submission - Conor MacCarthy
Student Number: 100876374

1 + 8 + 7 + 6 + 3 + 7 + 4 = 36
Even number, so project is Galaga.


THE SCENE:
Game is made using primitives. Orange cube for player, purple cubes for enemies, green capsule for bullets. There is a HUD showing score, which increases by 100 when an enemy is killed.
Player can move left and right, and use Space to shoot. Enemies die when shot. Enemies do not move.


SINGLETON:
The UIManager is a singleton. There is only ever one instance of it so I decided this would be the best use of a singleton. It has some code to ensure there is only ever one instance of it at a time. It is used by the bullets whenever an enemy is hit to increase the score on the UI.

OBSERVER:
The UIManager is also an observer, which observes the bullets. When a bullet hits an enemy, the UIManager is notified. There is a subfolder within the scripts that includes logic for subjects and observers called Observer.

STATE:
The enemies have 2 states: alive and dead. They start off alive. When a bullet hits them, they transition into the dead state. All logic for states can be found in the State subfolder in the scripts. Enemies currently do not respawn. I was going to have them respawn when all enemies were killed but I ran out of time.
