### **Part 1\. Unit Testing the Game Mechanics**

#### **Description:**

Unit tests focus on ensuring isolated gameplay mechanics work as expected.

#### **Action:**

**A) Key Mechanics:**

* **Paddle Movement:** Test left and right movement.  
* **Ball Collision:** Check if the ball bounces off correctly from bricks, walls, and the paddle.  
* **Brick Destruction:** Confirm bricks disappear when hit by the ball.  
* **Power-Ups:** Verify power-ups activate correctly when collected.

**B) Test Examples:**

1. Paddle moves left and right within screen boundaries.  
2. Ball bounces correctly at all angles from the paddle, bricks, and walls.  
3. Power-ups like extra lives or ball speed change activate on collision.

---

### **Part 2\. Logic Testing the Game Rules and Calculations**

#### **Description:**

Logic tests verify calculations for scores, level progression, and power-up effects.

#### **Action:**

**A) Key Calculations:**

* **Score:** Points awarded correctly for breaking bricks.  
* **Level Progression:** Level increases after clearing all bricks.  
* **Ball Speed:** Increases in endless mode over time.

**B) Test Examples:**

1. Breaking a brick adds the correct points (e.g., 10 points per brick).  
2. Clearing all bricks progresses to the next level and resets the board.  
3. Ball speed increases gradually in endless mode and caps at a reasonable speed.

---

### **Part 3\. Boundary Testing: Edge Cases and Limits**

#### **Description:**

Boundary testing ensures the game handles extreme scenarios.

#### **Action:**

**A) Edge Cases:**

* **Score Limits:** Verify game behavior at max score (e.g., 99999).  
* **Paddle Boundary:** Prevent paddle movement beyond screen edges.  
* **Endless Mode:** Ensure ball speed caps and game remains functional at high speeds.

**B) Test Examples:**

1. At max score, ensure the score does not overflow or reset.  
2. Ball and paddle stop at screen boundaries without glitches.  
3. Ensure game handles extremely fast ball speeds in endless mode.

---

### **Part 4\. Integration Testing: System Interaction**

#### **Description:**

Integration tests verify interactions between game components.

#### **Action:**

**A) Component Interactions:**

* **Paddle and Ball Collision:** Confirm ball bounces correctly off the paddle.  
* **Menu and Game State:** Ensure pausing and resuming work without errors.  
* **Co-Op Mode:** Verify both players’ inputs and game state are synchronized.

**B) Test Examples:**

1. Ball’s trajectory changes based on where it hits the paddle.  
2. Resuming the game from pause restores the exact previous state.  
3. In co-op mode, ensure players’ scores are calculated separately.

---

### **Part 5\. Handling Bad Input and Run-Time Errors**

#### **Description:**

Ensure the game gracefully handles invalid inputs or runtime errors.

#### **Action:**

**A) Bad Input Handling:**

* Invalid Key Presses: Ignore unassigned keys without crashing.  
* Extreme Paddle Movement: Prevent paddle movement beyond the screen.

**B) Test Examples:**

1. Ignore simultaneous conflicting key presses without glitches.  
2. On save file corruption, notify the player and allow a new game start.

---

### **Part 6\. Presenting the Tests in a Table**

| Test Case | Test Data | Expected Outcome |
| ----- | ----- | ----- |
| Paddle Movement | Move paddle left and right | Paddle moves correctly, stops at screen boundaries. |
| Ball Collision | Ball hits paddle/bricks/walls | Ball bounces off surfaces at the expected angle. |
| Brick Destruction | Ball hits a brick | Brick disappears, score increases by 10 points. |
| Level Progression | Clear all bricks | Level increases, game board resets, ball speed increases. |
| Endless Mode Speed | Long survival time | Ball speed gradually increases but caps at a maximum value. |
| Invalid Key Press | Press unassigned keys | Game ignores invalid keys without crashing. |
| Co-op Scoring | Player 1 vs Player 2 | Both players’ scores are calculated separately without interference. |
| Pause and Resume | Pause and resume the game | Game pauses and resumes from the exact previous state. |
| Save/Load | Corrupted save file | Notify player, start new game without crashing. |

