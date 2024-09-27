import pygame
import random

# 初始化 pygame
pygame.init()

# 設定畫面大小
screen_width = 800
screen_height = 600
screen = pygame.display.set_mode((screen_width, screen_height))

# 設定顏色
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)
RED = (255, 0, 0)

# 角色設定
player_size = 50
player_pos = [screen_width // 2, screen_height - 2 * player_size]
player_speed = 10

# 障礙物列表
obstacles = []
obstacle_size = 50
obstacle_speed = 10
obstacle_frequency = 20  # 每幾幀產生一個障礙物

# 定義 Boss
boss_size = 100
boss_pos = [screen_width // 2, 0]
boss_speed = 5
boss_exists = False

# 設定遊戲時鐘
clock = pygame.time.Clock()

game_over = False
score = 0
frame_count = 0

# 遊戲主迴圈
while not game_over:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            game_over = True

    # 接收按鍵輸入
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT] and player_pos[0] > 0:
        player_pos[0] -= player_speed
    if keys[pygame.K_RIGHT] and player_pos[0] < screen_width - player_size:
        player_pos[0] += player_speed

    # 每 x 幀生成一個新障礙物，並隨著時間增加頻率
    if frame_count % max(1, obstacle_frequency) == 0:
        new_obstacle = [random.randint(0, screen_width - obstacle_size), 0]
        obstacles.append(new_obstacle)
    frame_count += 1

    # 更新障礙物位置
    for obstacle in obstacles:
        obstacle[1] += obstacle_speed
        if obstacle[1] > screen_height:
            obstacles.remove(obstacle)
            score += 1

    # 增加障礙物掉落速度以及生成頻率，每得分10分遞增一次
    if score % 10 == 0 and score != 0:
        obstacle_speed += 1
        obstacle_frequency -= 1  # 增加生成頻率
        score += 1  # 更新分數，避免重複遞增

    # 更新 Boss 位置和條件
    if score > 30:  # 當分數達到某一數值時出現 Boss
        boss_exists = True
        boss_pos[1] += boss_speed

    # 檢查是否與障礙物碰撞
    for obstacle in obstacles:
        if (player_pos[0] < obstacle[0] < player_pos[0] + player_size or
            obstacle[0] < player_pos[0] < obstacle[0] + obstacle_size):
            if (player_pos[1] < obstacle[1] < player_pos[1] + player_size or
                obstacle[1] < player_pos[1] < obstacle[1] + obstacle_size):
                game_over = True

    # 檢查是否與 Boss 碰撞
    if boss_exists:
        if (player_pos[0] < boss_pos[0] < player_pos[0] + player_size or
            boss_pos[0] < player_pos[0] < boss_pos[0] + boss_size):
            if (player_pos[1] < boss_pos[1] < player_pos[1] + player_size or
                boss_pos[1] < player_pos[1] < boss_pos[1] + boss_size):
                game_over = True

    # 重繪畫面
    screen.fill(BLACK)
    pygame.draw.rect(screen, RED, (player_pos[0], player_pos[1], player_size, player_size))
    for obstacle in obstacles:
        pygame.draw.rect(screen, WHITE, (obstacle[0], obstacle[1], obstacle_size, obstacle_size))

    if boss_exists:
        pygame.draw.rect(screen, RED, (boss_pos[0], boss_pos[1], boss_size, boss_size))

    pygame.display.flip()
    clock.tick(30)

pygame.quit()
