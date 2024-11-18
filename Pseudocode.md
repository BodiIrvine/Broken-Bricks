Name (Bodi, Malachi)

\# Initialize Game  
Initialize game grid (playfield)  
Initialize score \= 0  
Initialize level \= 1  
Initialize lives \= 3  
Initialize game speed \= normal  
Initialize power-ups (empty)  
Initialize game mode \= "single-player" or "co-op" or "endless"  
Initialize current world \= "world 1"  
Initialize ball speed \= normal  
Initialize paddle size \= default  
Initialize achievements (empty)

\# Start Game Loop  
While game is running:  
    Clear screen  
    Display current score, level, and lives  
    Display current world/level  
    Display achievements or unlocks  
    Spawn new ball at paddle position  
    Spawn new paddle at default position

    \# Start gameplay loop  
    While player is playing:  
        Move ball based on ball direction  
          
        If ball hits wall or boundary:  
            Reflect ball direction  
          
        If ball hits paddle:  
            Reflect ball off paddle  
            If ball hits a brick:  
                Destroy brick and update score  
                Increase ball speed or difficulty if needed  
                Check if level is completed  
          
        \# Handle user input for paddle control  
        If player presses "left":  
            Move paddle left  
          
        If player presses "right":  
            Move paddle right  
          
        If player presses "pause":  
            Pause game  
          
        \# Handle game modes  
        If game mode is "endless":  
            Increase ball speed after each level  
            If player loses all lives, end game  
          
        If game mode is "co-op":  
            If second player loses all lives, end game for that player  
          
        \# Handle power-ups  
        If ball collides with power-up:  
            Activate power-up (e.g., enlarge paddle, extra life, slow ball, etc.)  
            Remove power-up from the screen  
          
        \# Handle achievements/unlocks  
        If player achieves milestone (e.g., 100 points, level 5):  
            Unlock achievement or new feature (e.g., new ball skin, world)

    \# Check for game over condition  
    If lives \= 0 or grid is full:  
        End game  
        Display "Game Over"  
      
    \# Continue next frame  
    Update game screen with new state

\# Level Completion Logic  
If all bricks are destroyed in a level:  
    Increase level  
    Increase ball speed  
    Increase difficulty (more bricks, faster ball, smaller paddle)  
    Spawn new level with new world/level theme  
    If co-op mode, show score comparison between players

\# Power-up Logic  
For each active power-up:  
    Check if power-up is collected by the ball  
    If collected:  
        Trigger corresponding effect (e.g., slow down time, enlarge paddle, etc.)  
        Remove power-up from screen

\# Game Over and Restart  
If player finishes all levels or exits:  
    Display final score  
    Ask if player wants to restart or quit  
    If restart, reset game settings and start new game

