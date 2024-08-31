# Contents of config.py
level_map=[
"                                                                                                                                                                                    ",
"                                                                                                                                                                             12     ",
"                       XX       56                                          E                                                                                                34     ",
"        E                       87           c            XXXXXX         XXXXXX  XXX     C                                                                      XXXXXXX  XXXXXXXXXXX",
"XX P  xxxx     C                                                     XX                XXXXXXXXXX                  C                                   XXXXXXX                      ",
"XXXX          XX         XX                       Y   xxx        XX                                   C        XXXXXX                   C e                                         ",
"            XX                     e   C         XXX        S                       C                XX                              XXXXXXXXX    XXXX                              ",
"       X  XXXX    XX  XX         XXXXXXXX   XX   XXX     XXXXXXX               XX  XXXXXX                                          X             XXXXX                        C     ",
"       X  XXXX    XX  XXX     X             XX   XXXX    XXXXXXXXX           XXXX                             XXXXX  XX  X  XXXX                 XXXXXX      C               XXXXX  ",
"    XXXX  XXXXXX  XX  XXXX    X             XX   XXXXXX  XXXXXXXXX          XXXXX                    XXXXXX                 XXXXX                XXXXXX    XXXXXXXXXXX              ",
"XXXXXXXX  XXXXXX  XX  XXXXXXXXXXXXXXXXXX    XX   XXXXXX  XXXXXXXXXXX     XXXXXXXX                XXXXXXXXXXXX               XXXXXX               XXXXXX    XXXXXXXXXXXXXXX          ",
]

level_map2=[
"                                                                                                                                                                                    ",
"                                                                                                                                    M                                               ",
"                                                                                                                                    XX                                              ",
"            56                                            XXXXX   XXXXX    XXXX  XXXXXXX   XXXXXXX                        XXXXXXXX                                                  ",
"            87                                      XXX                                                     XXXXXXXX                                                                ",
"                                              XXX                                                XXXXXX                                                                             ",
"                                     XXXXXX                                                                                                                                         ",
" P                     XXXX     XX   XXX          XXXXXXXX                                                                                                                          ",
"XXXX            XXX    XXXXX    XX   XXX                     XXXX    XXX                                                                 12                                         ",
"XXXX   XXXXXX          XXXXX    XX   XXX  X                  XXXX    XXX  XX   XXXXXXX             XXXXXX   XX  X XXXX                   34                                        ",
"XXXX                   XXXXXX   XX   XXXXXX                  XXXX    XXX  XX   XXXXXXXXXXXXXXXXXX                       XXXXXX  XX  XXXXXXX                                         ",
]

tile_size=32
en=600
boy=len(level_map)*tile_size
ENEMY_SPEED = 1

# Contents of enemy.py
import pygame,random
from os import walk
from config import *

class Enemy(pygame.sprite.Sprite):
  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
    #self.image.fill("red")
    self.image = pygame.image.load("platform_game/e1.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (26, 28))
    self.rect = pygame.Rect(pos, (size, size))
    
    self.facing = random.choice(["left", "right"])
    self.animation_loop = 1
    self.haraket_loop = 0
    self.max_travel = random.randint(7, 30)
    self.x_change = 0
    self.y_change = 0
    self.max_health = 400  # Maksimum sağlık
    self.enemy_health = self.max_health  # Başlangıçta maksimum sağlık

    self.animation_counter = 0 
  
  def haraket(self):
    if self.facing == "left":
      self.x_change -= ENEMY_SPEED
      self.haraket_loop -= 1
      if self.haraket_loop <= -self.max_travel:
        self.facing = "right"
      self.image = pygame.image.load("platform_game/e1.png").convert_alpha()
    

    if self.facing == "right":
      self.x_change += ENEMY_SPEED
      self.haraket_loop += 1
      if self.haraket_loop >= self.max_travel:
        self.facing = "left"
      self.image = pygame.image.load("platform_game/e2.png").convert_alpha()
   
  def update(self,x_shift):
    self.rect.x+=x_shift
    self.haraket()
    self.rect.x += self.x_change
    self.rect.y += self.y_change

    self.x_change = 0
    self.y_change = 0


class Enemybüyücü(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size))
        self.image = pygame.image.load("platform_game/eb1.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (26, 28))
        self.rect = pygame.Rect(pos, (size, size))

        self.facing = random.choice(["left", "right"])
        self.haraket_loop = 0
        self.max_travel = random.randint(7, 30)
        self.x_change = 0
        self.y_change = 0
      
        self.max_health = 500  # Maksimum sağlık
        self.enemy_health = self.max_health  # Başlangıçta maksimum sağlık

      
        self.images_left = [pygame.image.load("platform_game/eb1.png").convert_alpha(),
                            pygame.image.load("platform_game/eb2.png").convert_alpha()]
        
        self.animation_counter = 0
      
        self.enemy_bullets = pygame.sprite.Group()
        self.shoot_delay = 60  # Adjust the delay between shots as needed
        self.shoot_timer = 0
      
    def shoot(self, direction):
        bullet_size = 16  # Adjust the size as needed
        bullet_pos = (self.rect.left - bullet_size, self.rect.centery)

        # Set the direction attribute for reference
        self.direction = "left"
        bullet = EnemyBullet(bullet_pos, bullet_size)
        self.enemy_bullets.add(bullet)


        # Set the direction attribute for reference
        self.direction = direction

    def update_bullets(self):
        self.enemy_bullets.update()
  
    def haraket(self):
        if self.facing == "left":
            self.x_change -= 0.4
            self.haraket_loop -= 1
            if self.haraket_loop <= -self.max_travel:
                self.facing = "right"

        if self.facing == "right":
            self.x_change += 0.4
            self.haraket_loop += 1
            if self.haraket_loop >= self.max_travel:
                self.facing = "left"

    def animate(self):

        if self.facing == "left":
            frame = self.animation_counter // 10 % len(self.images_left)
            self.image = self.images_left[frame]

    def update(self, x_shift):
      self.rect.x += x_shift
      self.haraket()
      self.rect.x += self.x_change
      self.rect.y += self.y_change
      
      self.animate()  
      self.animation_counter += 1
      
      self.x_change = 0
      self.y_change = 0
      
      if self.shoot_timer <= 0:
        direction = random.choice(["left", "right"])
        self.shoot(direction)
        self.shoot_timer = self.shoot_delay
      else:
        self.shoot_timer -= 1

    # Update enemy bullets
      self.update_bullets()

class EnemyBullet(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        pygame.draw.circle(self.image, (255, 0, 0), (size // 2, size // 2), 5)
        self.rect = self.image.get_rect(center=pos)
        self.speed = 2  # Ayarladığınız hız
        self.max_distance = 300  # Mermilerin kat edebileceği maksimum mesafe
        self.distance_travelled = 0  # Mermi tarafından kat edilen toplam mesafe

    def update(self):
        self.rect.x -= self.speed
        self.distance_travelled += abs(self.speed) 
        if self.distance_travelled >= self.max_distance:
            self.kill()

class EnemySlime(pygame.sprite.Sprite):
  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
    #self.image.fill("red")
    self.image = pygame.image.load("platform_game/es1.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (37, 28))
    self.rect = pygame.Rect(pos, (size, size))
    
    self.facing = random.choice(["left", "right"])
    self.animation_loop = 1
    self.haraket_loop = 0
    self.max_travel = random.randint(7, 30)
    self.x_change = 0
    self.y_change = 0
    self.max_health = 600  # Maksimum sağlık
    self.enemy_health = self.max_health  # Başlangıçta maksimum sağlık

    self.animation_counter = 0 

    self.images_left = [pygame.image.load("platform_game/es1.png").convert_alpha(),
                            pygame.image.load("platform_game/es4.png").convert_alpha()]

    self.images_right = [pygame.image.load("platform_game/es2.png").convert_alpha(),
                            pygame.image.load("platform_game/es3.png").convert_alpha()]
        
  
  def haraket(self):
    if self.facing == "left":
      self.x_change -= ENEMY_SPEED
      self.haraket_loop -= 1
      if self.haraket_loop <= -self.max_travel:
        self.facing = "right"
      self.image = pygame.image.load("platform_game/es1.png").convert_alpha()
    

    if self.facing == "right":
      self.x_change += ENEMY_SPEED
      self.haraket_loop += 1
      if self.haraket_loop >= self.max_travel:
        self.facing = "left"
      self.image = pygame.image.load("platform_game/es2.png").convert_alpha()

  def animate(self):

        if self.facing == "left":
            frame = self.animation_counter // 10 % len(self.images_left)
            self.image = self.images_left[frame]

        if self.facing == "right":
            frame = self.animation_counter // 10 % len(self.images_right)
            self.image = self.images_right[frame]
  
  def update(self,x_shift):
    self.rect.x+=x_shift
    self.haraket()
    self.rect.x += self.x_change
    self.rect.y += self.y_change

    self.animate()  
    self.animation_counter += 1
    
    self.x_change = 0
    self.y_change = 0

class Enemycadı(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size))
        self.image.blit(pygame.image.load("platform_game/ec1.png").convert_alpha(), (0, 0))
        self.image = pygame.transform.scale(self.image, (36, 32))
        self.rect = pygame.Rect(pos, (size, size))

        self.facing = random.choice(["left", "right"])
        self.haraket_loop = 0
        self.max_travel = random.randint(7, 30)
        self.x_change = 0
        self.y_change = 0
      
        self.max_health = 300  # Maksimum sağlık
        self.enemy_health = self.max_health  # Başlangıçta maksimum sağlık

      
        self.images_left = [pygame.image.load("platform_game/ec2.png").convert_alpha(),
                            pygame.image.load("platform_game/ec3.png").convert_alpha()]

        self.images_right = [pygame.image.load("platform_game/ec1.png").convert_alpha(),
                            pygame.image.load("platform_game/ec4.png").convert_alpha()]
      
        self.animation_counter = 0
      
        self.enemy_bullets = pygame.sprite.Group()
        self.shoot_delay = 40  # Adjust the delay between shots as needed
        self.shoot_timer = 0
      
    def shoot(self, direction):
      bullet_size = 16  # Adjust the size as needed

    # Calculate the bullet position based on the character's direction
      if direction == "left":
        bullet_pos = (self.rect.left - bullet_size, self.rect.centery)
      else:  # direction == "right"
        bullet_pos = (self.rect.right, self.rect.centery)

    # Set the direction attribute for reference
      self.direction = direction
      bullet = EnemyBullet2(bullet_pos, bullet_size)
      self.enemy_bullets.add(bullet)


    def update_bullets(self):
        self.enemy_bullets.update()
  
    def haraket(self):
        if self.facing == "left":
            self.x_change -= 2
            self.haraket_loop -= 1
            if self.haraket_loop <= -self.max_travel:
                self.facing = "right"

        if self.facing == "right":
            self.x_change += 2
            self.haraket_loop += 1
            if self.haraket_loop >= self.max_travel:
                self.facing = "left"

    def animate(self):

        if self.facing == "left":
            frame = self.animation_counter // 10 % len(self.images_left)
            self.image = self.images_left[frame]
        if self.facing == "right":
            frame = self.animation_counter // 10 % len(self.images_right)
            self.image = self.images_right[frame]
          
    def update(self, x_shift):
      self.rect.x += x_shift
      self.haraket()
      self.rect.x += self.x_change
      self.rect.y += self.y_change
      
      self.animate()  
      self.animation_counter += 1
      
      self.x_change = 0
      self.y_change = 0
      
      if self.shoot_timer <= 0:
        direction = random.choice(["left", "right"])
        self.shoot(direction)
        self.shoot_timer = self.shoot_delay
      else:
        self.shoot_timer -= 1

    # Update enemy bullets
      self.update_bullets()

class EnemyBullet2(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        pygame.draw.circle(self.image, (100, 154, 90), (size // 2, size // 2), 5)
        self.rect = self.image.get_rect(center=pos)
        self.speed = 2  # Ayarladığınız hız
        self.max_distance = 300  # Mermilerin kat edebileceği maksimum mesafe
        self.distance_travelled = 0  # Mermi tarafından kat edilen toplam mesafe

    def update(self):
        self.rect.y += self.speed
        self.distance_travelled += abs(self.speed) 
        if self.distance_travelled >= self.max_distance:
            self.kill()

class EnemyYılan(pygame.sprite.Sprite):
  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
    #self.image.fill("red")
    self.image = pygame.image.load("platform_game/ey1.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (37, 28))
    self.rect = pygame.Rect(pos, (size, size))
    
    self.facing = random.choice(["left", "right"])
    self.animation_loop = 1
    self.haraket_loop = 0
    self.max_travel = random.randint(7, 30)
    self.x_change = 0
    self.y_change = 0
    self.max_health = 600  # Maksimum sağlık
    self.enemy_health = self.max_health  # Başlangıçta maksimum sağlık

    self.animation_counter = 0 

    self.images_left = [pygame.image.load("platform_game/ey1.png").convert_alpha(),
                            pygame.image.load("platform_game/ey2.png").convert_alpha()]

    self.images_right = [pygame.image.load("platform_game/ey3.png").convert_alpha(),
                            pygame.image.load("platform_game/ey4.png").convert_alpha()]
        
  
  def haraket(self):
    if self.facing == "left":
      self.x_change -= ENEMY_SPEED
      self.haraket_loop -= 1
      if self.haraket_loop <= -self.max_travel:
        self.facing = "right"
      self.image = pygame.image.load("platform_game/ey1.png").convert_alpha()
    

    if self.facing == "right":
      self.x_change += ENEMY_SPEED
      self.haraket_loop += 1
      if self.haraket_loop >= self.max_travel:
        self.facing = "left"
      self.image = pygame.image.load("platform_game/ey3.png").convert_alpha()

  def animate(self):

        if self.facing == "left":
            frame = self.animation_counter // 10 % len(self.images_left)
            self.image = self.images_left[frame]

        if self.facing == "right":
            frame = self.animation_counter // 10 % len(self.images_right)
            self.image = self.images_right[frame]
  
  def update(self,x_shift):
    self.rect.x+=x_shift
    self.haraket()
    self.rect.x += self.x_change
    self.rect.y += self.y_change

    self.animate()  
    self.animation_counter += 1
    
    self.x_change = 0
    self.y_change = 0



# Contents of level.py
from os import kill
import pygame,sys
from tiles import *
from config import tile_size,en,boy,level_map
from player import Player
from enemy import *

class Level(pygame.sprite.Sprite):
  def __init__(self,level_data,surface):
    self.display_surface=surface
    self.setup_level(level_data)
    self.world_shift=0
    self.player_died_flag = False
    self.mwin=0

  def startup_screen(self):
        font = pygame.font.Font(None, 36)
        startup_text = "You fainted and your eyes you opened "
        startup_text2 = "it in this place, you should get out of here..."
        text = font.render(startup_text, True, (255, 255, 255))
        text2 = font.render(startup_text2, True, (255, 255, 255))
        text_rect = text.get_rect(center=(300, 150))
        text_rect2 = text2.get_rect(center=(290, 190))
        for i in range(100):
            self.display_surface.fill((0, 0, 0))
            text_rect.y -= 2  # Move the text upward
            text_rect2.y -= 2
            self.display_surface.blit(text, text_rect)
            self.display_surface.blit(text2, text_rect2)
            pygame.display.flip()
            pygame.time.delay(10)  # Adjust the delay to control the scroll speed

        pygame.time.wait(1000)
        self.startup_complete = True
  
  def setup_level(self,layout):
    self.tiles=pygame.sprite.Group()
    self.player=pygame.sprite.GroupSingle()
    self.coin=pygame.sprite.Group()
    self.enemy=pygame.sprite.Group()
    self.enemyb=pygame.sprite.Group()
    self.enemyc=pygame.sprite.Group()
    self.bg=pygame.sprite.Group()
    self.kapı=pygame.sprite.Group()
    self.tablo=pygame.sprite.Group()
    self.enemyyılan=pygame.sprite.Group()
    self.map=pygame.sprite.Group()
    for row_index,row in enumerate(layout):
      for col_index,cell in enumerate(row):
        x=col_index*tile_size
        y=row_index*tile_size
        if cell=="x":
          tile=Tile((x,y),tile_size)
          self.tiles.add(tile)
        if cell=="X":
          tile2=Tile2((x,y),tile_size)
          self.tiles.add(tile2)
        if cell=="P":
          player_sprite=Player((x,y))
          self.player.add(player_sprite)
        if cell=="C":
          coin=Coin((x,y),tile_size)
          self.coin.add(coin)
        if cell=="E":
          enemy=Enemy((x,y),tile_size)
          self.enemy.add(enemy)
        if cell=="S":
          enemys=EnemySlime((x,y),tile_size)
          self.enemy.add(enemys)
        if cell=="e":
          enemyb=Enemybüyücü((x,y),tile_size)
          self.enemyb.add(enemyb)
        if cell=="c":
          enemyc=Enemycadı((x,y),tile_size)
          self.enemyc.add(enemyc)
        if cell=="Y":
          enemyy=EnemyYılan((x,y),tile_size)
          self.enemyyılan.add(enemyy)
        if cell==".":
          bg=Bg((x,y),tile_size)
          self.bg.add(bg)
        if cell=="1":
          k1=K1((x,y),tile_size)
          self.kapı.add(k1)
        if cell=="2":
          k1=K2((x,y),tile_size)
          self.kapı.add(k1)
        if cell=="3":
          k1=K3((x,y),tile_size)
          self.kapı.add(k1)
        if cell=="4":
          k1=K4((x,y),tile_size)
          self.kapı.add(k1) 
        if cell=="5":
          t1=T1((x,y),tile_size)
          self.tablo.add(t1)
        if cell=="6":
          t2=T2((x,y),tile_size)
          self.tablo.add(t2)
        if cell=="7":
          t3=T3((x,y),tile_size)
          self.tablo.add(t3)
        if cell=="8":
          t4=T4((x,y),tile_size)
          self.tablo.add(t4) 
        if cell=="M":
          map=Map((x,y),tile_size)
          self.map.add(map) 

  def scroolx(self):
    player=self.player.sprite
    player_x=player.rect.centerx
    direction_x=player.direction.x
    
    if player_x<en/4 and direction_x<0:
      self.world_shift=5
      player.speed=0
    elif player_x>en-(en/4) and direction_x>0:
      self.world_shift=-5
      player.speed=0
      
    else:
      self.world_shift=0
      player.speed=5
      
    if player.rect.y > 352:
        self.player_died()

  def collision(self):
    player=self.player.sprite
    player.rect.x+=player.direction.x*player.speed


    for sprite in self.tiles.sprites():
      if sprite.rect.colliderect(player.rect):
        if player.direction.x>0:
          player.rect.right=sprite.rect.left
        elif player.direction.x<0:
          player.rect.left=sprite.rect.right
    collected_coins = pygame.sprite.spritecollide(player, self.coin, True)
    if collected_coins:
      player.strength+=30

    win = pygame.sprite.spritecollide(player, self.kapı, False)
    if win and self.mwin==0:
      for kapı in win:
        self.win2()

    win2 = pygame.sprite.spritecollide(player, self.kapı, False)
    if win2 and self.mwin==1:
      for kapı in win2:
        self.win()
    
    hits = pygame.sprite.spritecollide(player, self.enemy, False)
    if hits and player.facing=="left":
      for enemy in hits:
        enemy.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemy.enemy_health <= 0:
                self.enemy.remove(enemy) 
                player.strength+=30
        player.animate_attackL()
      player.health -= 0.1

    hits2 = pygame.sprite.spritecollide(player, self.enemy, False)
    if hits2 and player.facing=="right":
      player.facing="right"
      for enemy in hits2:
        enemy.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemy.enemy_health <= 0:
                self.enemy.remove(enemy) 
                player.strength+=30
        player.animate_attackR()
      player.health -= 0.2

    hits3 = pygame.sprite.spritecollide(player, self.enemyb, False)
    if hits3 and player.facing=="left":
      for enemyb in hits3:
        enemyb.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyb.enemy_health <= 0:
                self.enemyb.remove(enemyb) 
                player.strength+=30
        player.animate_attackL()
      player.health -= 0.2

    hits4 = pygame.sprite.spritecollide(player, self.enemyb, False)
    if hits4 and player.facing=="right":
      player.facing="right"
      for enemyb in hits4:
        enemyb.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyb.enemy_health <= 0:
                self.enemyb.remove(enemyb) 
                player.strength+=30
        player.animate_attackR()
      
      player.health -= 0.2

    hits5 = pygame.sprite.spritecollide(player, self.enemyc, False)
    if hits5 and player.facing=="left":
      for enemyc in hits5:
        enemyc.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyc.enemy_health <= 0:
                self.enemyc.remove(enemyc) 
                player.strength+=30
        player.animate_attackL()
      player.health -= 0.2

    hits6 = pygame.sprite.spritecollide(player, self.enemyc, False)
    if hits6 and player.facing=="right":
      player.facing="right"
      for enemyc in hits6:
        enemyc.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyc.enemy_health <= 0:
                self.enemyc.remove(enemyc) 
                player.strength+=30
        player.animate_attackR()

    hits7 = pygame.sprite.spritecollide(player, self.enemyyılan, False)
    if hits7 and player.facing=="left":
      for enemyy in hits7:
        enemyy.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyy.enemy_health <= 0:
                self.enemyyılan.remove(enemyy) 
                player.strength+=30
        player.animate_attackL()
      player.health -= 0.3

    hits8 = pygame.sprite.spritecollide(player, self.enemyyılan, False)
    if hits8 and player.facing=="right":
      player.facing="right"
      for enemyy in hits8:
        enemyy.enemy_health -= 10  # Düşmanın sağlığını 10 azalt
        if enemyy.enemy_health <= 0:
                self.enemyyılan.remove(enemyy) 
                player.strength+=30
        player.animate_attackR()
      
      player.health -= 0.3
    for enemyb in self.enemyb:
      bullet_hits = pygame.sprite.spritecollide(player, enemyb.enemy_bullets, True)
      if bullet_hits:
        player.health -= 15 

    for enemyc in self.enemyc:
      bullet_hits = pygame.sprite.spritecollide(player, enemyc.enemy_bullets, True)
      if bullet_hits:
        player.health -= 15 
    
    for enemyb in self.enemyb:
        bullet_hits = pygame.sprite.groupcollide(enemyb.enemy_bullets, self.tiles, True, False)
        # Check for collisions between enemy bullets and tiles
        for bullet, tile_hit in bullet_hits.items():
            for tile in tile_hit:
                # Remove the bullet when it hits a tile
                enemyb.enemy_bullets.remove(bullet)

    for enemyc in self.enemyc:
        bullet_hits = pygame.sprite.groupcollide(enemyc.enemy_bullets, self.tiles, True, False)
        # Check for collisions between enemy bullets and tiles
        for bullet, tile_hit in bullet_hits.items():
            for tile in tile_hit:
                # Remove the bullet when it hits a tile
                enemyc.enemy_bullets.remove(bullet)

    for map in self.map:
      hits0 = pygame.sprite.spritecollide(player, self.map, True)
      if hits0:
        self.mwin=1
    
    if player.health<=0:
      self.player_died()
      self.reset()
      player.health=150

  
  def game_over_screen(self):
    font = pygame.font.Font(None, 74)
    font2 = pygame.font.Font(None, 25)
    self.display_surface.fill((20, 20, 20))
    text = font.render("YOU DIE", True, (255, 0, 0))
    text_rect = text.get_rect(center=(en / 2, boy / 2))
    text2 = font2.render("Press Enter to reboot", True, (255, 0, 0))
    text_rect2= text2.get_rect(center=(120, boy-20))
    self.display_surface.blit(text2, text_rect2)
    self.display_surface.blit(text, text_rect)
    pygame.display.flip()
    pygame.time.wait(2000)  # Display the game over screen for 2 seconds

  def win(self):
    font = pygame.font.Font(None, 30)
    font2 = pygame.font.Font(None, 40)
    self.display_surface.fill((20, 20, 20))
    text = font.render("You finally managed to escape this place...", True, (255, 0, 0))
    text_rect = text.get_rect(center=(en / 2, boy / 2))
    text3 = font2.render("END 1", True, (255, 0, 0))
    text_rect3 = text3.get_rect(center=(270, 50))
    self.display_surface.blit(text, text_rect)
    self.display_surface.blit(text3, text_rect3)
    pygame.display.flip()
    pygame.time.wait(2000) 

  def win2(self):
    font = pygame.font.Font(None, 30)
    font2 = pygame.font.Font(None, 40)
    self.display_surface.fill((20, 20, 20))
    text = font.render("You finally managed to escape this place", True, (255, 0, 0))
    text2 = font.render("but you didn't take the map, this could cause you to get lost....", True, (255, 0, 0))
    text_rect  = text.get_rect(center=(290, 140))
    text_rect2 = text.get_rect(center=(210, 190))
    text3 = font2.render("END 2", True, (255, 0, 0))
    text_rect3 = text3.get_rect(center=(270, 50))
    self.display_surface.blit(text, text_rect)
    self.display_surface.blit(text2, text_rect2)
    self.display_surface.blit(text3, text_rect3)
    pygame.display.flip()
    pygame.time.wait(2000) 
  
  def reset_game(self):
    self.setup_level(level_map)  # Reset the level
    self.player.sprite.rect.x = 0
    self.player.sprite.rect.y = 0
    self.world_shift = 0

  def player_died(self):
    self.game_over_screen()
    self.reset_game()
    self.player_died_flag = True 
    
  def collision_y(self):
    player=self.player.sprite
    player.apply_gravity()

    for sprite in self.tiles.sprites():
      if sprite.rect.colliderect(player.rect):
        if player.direction.y>0:
          player.is_jumping=False
          player.rect.bottom=sprite.rect.top
          player.direction.y=0
        elif player.direction.y<0:
          player.rect.top=sprite.rect.bottom
          player.direction.y=0
          
  def run(self):
    self.bg.update(self.world_shift)
    self.bg.draw(self.display_surface)

    self.tiles.update(self.world_shift)
    self.tiles.draw(self.display_surface)

    for coin in self.coin:
        coin.update(self.world_shift)
    self.coin.draw(self.display_surface)

    self.enemy.update(self.world_shift)
    self.enemy.draw(self.display_surface)

    self.enemyyılan.update(self.world_shift)
    self.enemyyılan.draw(self.display_surface)
    
    for enemyb in self.enemyb:
        enemyb.update(self.world_shift)  # Update enemybüyücü
        self.enemyb.draw(self.display_surface)  # Draw enemybüyücü

        # Update and draw enemy bullets
        enemyb.update_bullets()
        enemyb.enemy_bullets.draw(self.display_surface)

    for enemyc in self.enemyc:
        enemyc.update(self.world_shift)  # Update enemybüyücü
        self.enemyc.draw(self.display_surface)  # Draw enemybüyücü

        # Update and draw enemy bullets
        enemyc.update_bullets()
        enemyc.enemy_bullets.draw(self.display_surface)
    
    self.kapı.update(self.world_shift)
    self.kapı.draw(self.display_surface)

    self.tablo.update(self.world_shift)
    self.tablo.draw(self.display_surface)

    self.map.update(self.world_shift)
    self.map.draw(self.display_surface)
    
    self.player.update()
    self.collision()
    self.scroolx()
    self.collision_y()
    self.player.draw(self.display_surface)


# Contents of main.py
import pygame,sys
from config import *
from level import Level
from player import *

pygame.init()

ekran = pygame.display.set_mode((en, boy))
clock=pygame.time.Clock()
level=Level(level_map,ekran)
arkaplan_resmi = pygame.image.load("platform_game/bg.png") 

while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
        elif event.type == pygame.KEYDOWN:
            if event.key == pygame.K_RETURN and level.player_died_flag:
                level.player_died_flag = False
                level.reset_game()

    ekran.fill((10, 50, 10))
    ekran.blit(arkaplan_resmi, (0, 0))
    ekran.blit(arkaplan_resmi, (480, 0))
    level.run()
    pygame.draw.rect(ekran, (255, 255, 255), (27, 17, 156, 21))
    pygame.draw.rect(ekran, (255, 0, 0), (30, 20, 150, 15)) 
    pygame.draw.rect(ekran, (255, 255, 255), (27, 67, 156, 21))
    pygame.draw.rect(ekran, (255, 0, 0), (30, 70, 150, 15)) 
    level.player.sprite.draw_health_bar(ekran)
    pygame.draw.circle(ekran, (255, 255, 255), (25, 25), 20)
    pygame.draw.circle(ekran, (255, 255, 255), (25, 75), 20)
    font = pygame.font.Font(None, 28)
    health_text = font.render("HP", True, (0, 0, 0))
    ekran.blit(health_text, (12, 17))
    health_text2 = font.render("MP", True, (0, 0, 0))
    ekran.blit(health_text2, (12, 67)) 
    pygame.display.update()
    clock.tick(60)

# Contents of player.py
import pygame
from config import *
class Player(pygame.sprite.Sprite):
  def __init__(self,pos):
    super().__init__() 
    self.image = pygame.image.load("platform_game/1.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (32, 32)) 
    self.rect = self.image.get_rect(topleft=pos)
    
    self.images_left =[pygame.image.load("platform_game/12.png").convert_alpha(),
                       pygame.image.load("platform_game/1.png").convert_alpha(),
                       pygame.image.load("platform_game/2.png").convert_alpha(), 
                       pygame.image.load("platform_game/11.png").convert_alpha(),
                       pygame.image.load("platform_game/3.png").convert_alpha(),]
    
    self.images_right = [pygame.image.load("platform_game/9.png").convert_alpha(),
                         pygame.image.load("platform_game/4.png").convert_alpha(),
                         pygame.image.load("platform_game/5.png").convert_alpha(), 
                         pygame.image.load("platform_game/0.png").convert_alpha(),
                         pygame.image.load("platform_game/6.png").convert_alpha(),]

    self.images_up = [pygame.image.load("platform_game/7.png").convert_alpha(),
                     pygame.image.load("platform_game/8.png").convert_alpha(),]
    
    self.direction=pygame.math.Vector2(0,0)
    self.speed=8
    self.gravity=1
    self.jump_speed=-13
    self.is_jumping = False
    self.animation_counter = 0 
    self.facing="right"
    
    self.total_distance = 0
    
    self.health = 150
    self.max_health = 150  
    self.health_bar_width = 150
    self.health_bar_height = 15
    self.health_bar_color = (0, 255, 0)

    self.strength = 0
    self.max_strength = 150  
    self.strength_bar_width = 150
    self.strength_bar_height = 15
    self.strength_bar_color = (0, 0, 255)

    self.attack_animation_frames = [
      pygame.image.load("platform_game/9.png").convert_alpha(),
      pygame.image.load("platform_game/0.png").convert_alpha(),
      pygame.image.load("platform_game/4.png").convert_alpha(),
      pygame.image.load("platform_game/0.png").convert_alpha(),]
    self.attack_animation_frames2 = [
      pygame.image.load("platform_game/12.png").convert_alpha(),
      pygame.image.load("platform_game/11.png").convert_alpha(),
      pygame.image.load("platform_game/1.png").convert_alpha(),
      pygame.image.load("platform_game/11.png").convert_alpha(),]
    self.attack_animation_index = 0
    self.attack_animation_counter = 0

  def animate_attackR(self):
        if self.attack_animation_counter % 3 == 0:  # Animasyon hızını ayarlayabilirsiniz
            self.image = self.attack_animation_frames[self.attack_animation_index]
            self.attack_animation_index = (self.attack_animation_index + 1) % len(self.attack_animation_frames)
        self.attack_animation_counter += 1

  def animate_attackL(self):
        if self.attack_animation_counter % 3 == 0:  # Animasyon hızını ayarlayabilirsiniz
            self.image = self.attack_animation_frames2[self.attack_animation_index]
            self.attack_animation_index = (self.attack_animation_index + 1) % len(self.attack_animation_frames2)
        self.attack_animation_counter += 1
      
  def draw_health_bar(self, surface):
        health_bar_rect = pygame.Rect(30, 20, self.health_bar_width, self.health_bar_height)
        pygame.draw.rect(surface, (0, 255, 0), health_bar_rect)
    
        strength_bar_rect = pygame.Rect(30 , 70, self.strength_bar_width, self.strength_bar_height)
        pygame.draw.rect(surface, (0, 0, 255), strength_bar_rect)

  def update_health_bar(self):
        strength_percentage = max(0, self.health) / self.max_health
        self.health_bar_width = int(strength_percentage * 150)

  def update_strength_bar(self):
        strength_percentage = max(0, self.strength) / self.max_strength
        self.strength_bar_width = int(strength_percentage * 150)
  
  def get_input(self):
        keys = pygame.key.get_pressed()

        if keys[pygame.K_RIGHT]:
            self.direction.x = 0.4
            self.facing="right"
            
        elif keys[pygame.K_LEFT]:
            self.direction.x = -0.4
            self.facing="left"

        else:
            self.direction.x = 0
            self.animation_counter = 0

        if keys[pygame.K_SPACE] and not self.is_jumping:
          #  self.facing="up"
            self.jump()
          
        if keys[pygame.K_x] and self.strength>=150 and self.facing=="right":
            self.direction.x = 11
            self.facing="right"
            self.strength=0
          
        if keys[pygame.K_x] and self.strength>=150 and self.facing=="left":
            self.direction.x = -11
            self.facing="left"
            self.strength=0

  def animate(self):
        if self.facing == "right":self.image = self.images_right[self.animation_counter // 10 % len(self.images_right)]
        elif self.facing == "left":self.image = self.images_left[self.animation_counter // 10 % len(self.images_left)]
        elif self.facing == "up":self.image = self.images_up[self.animation_counter // 10 % len(self.images_up)]
    
        self.animation_counter += 1
  
  def apply_gravity(self):
    self.direction.y+=self.gravity
    self.rect.y+=self.direction.y
  
  def jump(self):
    self.direction.y=self.jump_speed
    self.is_jumping = True
    
  def update(self):
        self.get_input()
        self.animate()
        self.update_health_bar() 
        self.update_strength_bar() 

# Contents of tiles.py
import pygame
from os import walk

class Tile(pygame.sprite.Sprite):

  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
   # self.image.fill("grey")
    self.image = pygame.image.load("platform_game/game_wall.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (32, 32))
    self.rect = self.image.get_rect(topleft=pos)

  def update(self,x_shift):
    self.rect.x+=x_shift

class Tile2(pygame.sprite.Sprite):

  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
   # self.image.fill("grey")
    self.image = pygame.image.load("platform_game/game_wall2.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (32, 32))
    self.rect = self.image.get_rect(topleft=pos)

  def update(self,x_shift):
    self.rect.x+=x_shift

class Bg(pygame.sprite.Sprite):

  def __init__(self, pos, size):
    super().__init__()
    self.image=pygame.Surface((size,size))
    self.image = pygame.image.load("platform_game/game_bg.png").convert_alpha()
    self.image = pygame.transform.scale(self.image, (32, 32))
    self.rect = self.image.get_rect(topleft=pos)

  def update(self,x_shift):
    self.rect.x+=x_shift

class Coin(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/game_coin.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class K1(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/k1.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class K2(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/k2.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class K3(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/k3.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift


class K4(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/k4.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class T1(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/t1.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class T2(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/t2.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class T3(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/t3.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift


class T4(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/t4.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

class Map(pygame.sprite.Sprite):
    def __init__(self, pos, size):
        super().__init__()
        self.image = pygame.Surface((size, size), pygame.SRCALPHA)
        self.image = pygame.image.load("platform_game/map.png").convert_alpha()
        self.image = pygame.transform.scale(self.image, (32, 32))
        #self.rect = self.image.get_rect(topleft=pos)
        self.rect = pygame.Rect(pos, (size, size))
    def update(self,x_shift):
      self.rect.x+=x_shift

