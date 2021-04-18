# kommand
class GameSprite(sprite.Sprite):
        def __init__(self, player_image, player_x, y, player_speed):
            super().__init__()
            self.image = transform.scale(image.load(Shrek.png), (65,65))
            self.speed = player_speed
            self.rect = self.image.get_rect()
            self.rect.x = player_x
            self.rect.y = y

class Player(GameSprite):
    def update(self):
        keys_pressed = key.get_pressed()
        if keys_pressed [K_LEFT]:# and self.rect.x > 5:
            self.rect.x -= self.speed
        if keys_pressed [K_RIGHT]:# and self.rect.x > 5:
            self.rect.x += self.speed
        if keys_pressed [K_UP]:# and self.rect.у > 5:
            self.rect.y -= self.speed
        if keys_pressed [K_DOWN]:# and self.rect.y> 5:
            self.rect.у -= self.speed

class Enemy(GameSprite):
    def update(self):
        if self.rect.x <= 47:
            self.direction = "right"
        if self.rect.x >= 600:
            self.direction = "left"
        if self.direction=="right":
            self.rect.x +=  self.speed
        else:
            self.rect.x -= self.speed
enemy = Enemy ('doctor.jpg',80,100,2)
