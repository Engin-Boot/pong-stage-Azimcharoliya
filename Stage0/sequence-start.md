# Interaction Sequences

## Startup Sequence

### Module interaction to start the game

```mermaid
sequenceDiagram
  Set_Board->>+Update_UI: Game board set
  Update_UI->>+Start_Game: Board UI set
  Start_Game->>+Update_UI: Initial ball movement
  Update_UI->>+Poll_Input: Game Started
  Update_UI->>+Update_UI: Update UI for each frame
  Poll_Input->>+Poll_Input: Get player inputs updates
  Poll_Input->>+Update_UI: There is user input
```

## Movement Initiation

### Module interaction to move the ball

```mermaid
sequenceDiagram
Start_Game->>+Update_UI: Start ball rolling
```

```mermaid
sequenceDiagram
  Frame_Looper->>+Get_Current_Frame: Calls every 100ms
  Get_Current_Frame->>+Check_Collision: Current Frame
  Check_Collision->>+Update_Dir_Vel: Collision between ball,paddles,top/bottom wall
  Update_Dir_Vel->>+Update_UI: Updated Direction and velocity of ball
```

```mermaid
sequenceDiagram
  Update_Score_Count->>+Reset_Ball: Point scored
  Reset_Ball->>+Update_UI: Updated position of the ball
```

## One score

### Module interaction to record the scores of player

```mermaid
sequenceDiagram

  Frame_Looper->>+Get_Current_Frame: Calls every 100ms
  Get_Current_Frame->>+Check_Collision: Current Frame
  Check_Collision->>+Update_Score_Count: Collision between ball and right/left wall
  Update_Score_Count->>+Update_UI: Updated player score
```

```mermaid
sequenceDiagram
  Update_Score_Count->>+Check_Winner: Updated player score
```
