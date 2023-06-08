# OOP examples and inspiration and notes
- When compiling the code for the entire game,  
- before starting the game loop, have pygame initialize, along with any other methods, or functions that will take place within the game loop
- the game loop will resemble a condensed verion of recalling the already defined functions, 
- the game loop will check for collisions, re-blit-ing of each sprite for every movement of change of direction
## Movement example
```python
def update(self):
    pressed_keys = pygame.key.get_pressed()
   #if pressed_keys[K_UP]:
        #self.rect.move_ip(0, -5)
   #if pressed_keys[K_DOWN]:
        #self.rect.move_ip(0,5)
     
    if self.rect.left > 0:
          if pressed_keys[K_LEFT]:
              self.rect.move_ip(-5, 0)
    if self.rect.left > 0:       
          if pressed_keys[K_RIGHT]:
              self.rect.move_ip(5, 0)
```
## 'Blit'ing of the image
```python
def draw(self, surface):
    surface.blit(self.image, self.rect)
```
## Collision termination
```python
#To be run if collision occurs between Player and Enemy
if pygame.sprite.spritecollideany(P1, enemies):
      DISPLAYSURF.fill(RED)
      pygame.display.update()
      for entity in all_sprites:
            entity.kill() 
      time.sleep(2)
      pygame.quit()
      sys.exit()
      
# kill() function is also suitable - look into it
for entity in all_sprites:
    DISPLAYSURF.blit(entity.image, entity.rect)
    entity.move()
```
## Enemy Falling code
```python

```
## Movement of player
```python

```
## Full example with scrolling background for a vertical game
https://coderslegacy.com/python/pygame-scrolling-background/
https://coderslegacy.com/python/python-pygame-tutorial/
