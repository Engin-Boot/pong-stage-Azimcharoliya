# Update Direction and Velocity

## Feature

This module will be responsible for updating the direction and velocity of ball.

## Acceptance Criteria

### Scenario: Updates when there is collision between ball and top/bottom wall

  Given the user is playing game on active device

  When there is a collision between ball and top/bottom wall

  Then compute and return the updated direction and velocity of ball.

### Scenario: Updates when there is collision between ball and paddles

  Given the user is playing game on active device

  When there is a collision between ball and paddles

  Then compute and return the updated direction and velocity of ball
  according to selected paddle level.
