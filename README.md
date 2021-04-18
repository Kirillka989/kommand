# kommand
class GameSprite(sprite.Sprite):
        def __init__(self, player_image, player_x, y, player_speed):
            super().__init__()
            self.image = transform.scale(image.load(Shrek.png), (65,65))
            self.speed = player_speed
            self.rect = self.image.get_rect()
            self.rect.x = player_x
            self.rect.y = y
