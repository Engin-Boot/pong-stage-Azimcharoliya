# Collision Update

## Feature

This module will be responsible for determining collison between ball,paddles
and four sides of wall. This module will return the collision type.

## Acceptance Criteria

### Scenario: Checking whether there is any collision in the given game frame

  Given the user is playing game on active device

  When there is a input frame update from poll input module

  Then compute and return there is any collision or not in the given frame

### Scenario: There is collision between ball and paddles/walls in the frame

  Given the user is playing game on active device

  When there is a input frame update from poll input module

  Then compute and return the collision type that has occured
 (collision between ball and paddles or collision between ball
 and top/bottom wall or collision between ball and left/right wall).
