# Interaction Sequences

## Startup Sequence

```mermaid
sequenceDiagram
  Set_Board->>+Update_UI: Game board set
  Update_UI->>+Start_Game: UI set
  Start_Game->>+Poll_Input: Started game
  Update_UI->>+Update_UI: Update UI for each frame
  Poll_Input->>+Poll_Input: Get player inputs updates
  Poll_Input->>+Update_UI: There is user input
```

```mermaid
sequenceDiagram
  Frame_Update->>+Check_Collision: Current Frame
  Check_Collision->>+Update_Dir_Vel: Collision between ball,paddles,top/bottom wall
  Check_Collision->>+Update_Score_Count: Collision between ball and right/left wall
  Update_Dir_Vel->>+Update_UI: Updates
  Update_Score_Count->>+Update_UI: Updates
```

```mermaid
sequenceDiagram
  Update_Score_Count->>+Reset_Ball: Point scored
  Update_Score_Count->>+Check_Winner: Updated Score
```

## Movement Initiation

```mermaid
sequenceDiagram
Start_Game->>+Update_UI: Start ball rolling
```

```mermaid
sequenceDiagram
  Frame_Update->>+Check_Collision: Current Frame
  Check_Collision->>+Update_Dir_Vel: Collision between ball,paddles,top/bottom wall
  Update_Dir_Vel->>+Update_UI: Updated Direction and velocity of ball
```

```mermaid
sequenceDiagram
  Update_Score_Count->>+Reset_Ball: Point scored
```

## One score

```mermaid
sequenceDiagram
  Frame_Update->>+Check_Collision: Current Frame
  Check_Collision->>+Update_Score_Count: Collision between ball and right/left wall
  Update_Score_Count->>+Update_UI: Updated player score
```
