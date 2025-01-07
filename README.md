
# Squid_Game_Red_Light_Green_Light_Program_Using_Python
Python application that implements the  "Red Light, Green Light" game based on the movie Squid Game. The program provides an interactive graphical interface using the Pygame library, which allows several users to complete against each other, and adds the condition of the light status to the competition

<img src="https://github.com/user-attachments/assets/adbfc857-f130-44cd-87cf-f770452a1034" alt="Image 1" width="400" height="300">

<img src="https://github.com/user-attachments/assets/82e37fe8-589a-4106-bafb-eb0ac8908861" alt="Image 2" width="400" height="300">

___
## Initialization

- `pip install pygame`
Pygame is a free and open-source cross-platform library for the developemtn of multimedia appplication like vedio games using python [[1]](https://www.geeksforgeeks.org/how-to-install-pygame-in-windows/)

- `random` Generate random floating numbers between 0 and 1.
- `time` module in python provides functions for handling time-related tasks. Includes,
      reading the current time,
      formatting time,
      sleeping for a specified number for seconds and so on.

- **Screen Dimenations:** The game window is set to 900x800 pixles.`(WIDTH, HEIGHT)`
- **colors:** White,Black,Red and Green are defined using RGB values.
- **Game window:** The pygame diaplay is initialized with caption `"SQUID GAME: RED LIGHT, GREEN LIGHT"`
- **Back Ground and light(doll) surface:** A background image id downloaded and enlarged to match the display, The light's(doll) condition is currently represented by two surfaces `green_img` and `red_img`.
  
![background](https://github.com/user-attachments/assets/88c0d4ff-9bca-4a39-be81-ddd0811f3569)

___
## Players And Doll

- **Players:** Totally eight players are created as rectangles (`pygame.rect`), each with unique horizontal positions and random speeds.Thier movements are controlled by player-specific speeds and game logic.
- **Dolls:** Represented as a static position at the top center of the screen, it determins whether players can move based on the light status

  ![image](https://github.com/user-attachments/assets/1190d2f7-d299-4b4e-b895-8c2352bbde4e)

  ___

  ## Game States

  - **Light** The doll alternates between "GREEN LIGHT" (players can move) and "RED LIGHT"(stop moving), the light's duration is 5 seconds for both states, managed using `time()`
  - **Players** Each players can either be : *alive and playing* = allowed to move based in the light, *Game Over* = If caught moving during "RED LIGHT", *Winner* = If they reach the doll's position.

___

## Game Logic 

- **Light state transition** The light switches between "RED LIGHT" and "GREEN LIGHT" in every 5 seconds, if "RED LIGHT" players caught moving are marked as `game_over`.
- **Player Movement** The K_UP refers to the *up arrow key* moves players forwards if the light is green in colour and they are not eliminated, Aplayer wins if they reach the doll's position.
- **Collision Detection** The program checks if any player reaches the doll's posotion to mark them as winners.

  ___

  ## Graphics, Display and Audio

  - **background:** Rendered on every frame
  - **Doll's Light:** Displays a green or red box based on the light code
  - **Players:** Displays black rectangles if still in the game
  - **Audio:** Background music ([red_light_green_light.mp3](c:\Users\rdeva\Downloads\red_light_green_light.mp3))

  - **Messages:** (`Game Over` or `you win`) on the screen.

  ___

  ## Termination

  - **Game Exit** Stops the loop if the user quits. `pygame.quit()` cleans up and closes the game

___

### Python Standard Library Commands
```python
import pygame
import random
import time
```
### Pygame Initialization
```python
pygame.init()
pygame.display.set_mode()
pygame.display.set_caption()
```
### Surface and Rectangle Commands
```python
pygame.Surface()
pygame.Rect()
surface.fill()
```
### Image and Music Loading
```python
pygame.image.load()
pygame.transform.scale()
pygame.mixer.music.load()
pygame.mixer.music.play()
```
### Keyboard and Event Handling
```python
pygame.key.get_pressed()
pygame.event.get()
pygame.QUIT
```
### Font and Text Rendering
```python
pygame.font.Font()
font.render()
```
### Clock and Timing
```python
pygame.time.Clock()
clock.tick()
```
### Display and Updates
```python
screen.blit()
pygame.display.update()
```
### Color Definitions
```python
Colors like (255, 255, 255) for WHITE, (255, 0, 0) for RED, etc.
```

___

## Summary of Features Used
- **Libraries** pygame, random, time.
- **Visuals** Surfaces, rectangles, images, and text.
-**Audio** Background music.
-**Events** Keyboard input and quitting.
  -**Logic** Timing, movement, collision detection, and dynamic updates.

___

## Conclusion 

This Python program perfectly recreates the "Red Light, Green Light" game inspired by Squid Game using Pygame. It includes interactive graphics, sound, and game features to create an engaging experience. Notable features include the random speed of the players, real-time movement control, light state switching, and status updates on who is winning or losing. The program shows effective use of Pygame for graphics, events, timing, and audio features.

This implementation teaches players to focus on timing and precision as the tension in the original game. It also is an excellent example of how to use Python and Pygame to make interactive, logic-based games.
  

  

