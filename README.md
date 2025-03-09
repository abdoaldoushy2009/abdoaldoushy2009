## 💫 About Me

### 👋 Hey there, I'm Abdo!
🚀 Aspiring Developer | Cybersecurity Enthusiast | AI Learner

---

### 👨‍💻 About Me
- 🎓 **Student at Assiut Official Language School**
- 🔥 **Passionate about Cybersecurity, AI, and Software Development**
- 🏆 **Constantly improving my skills in Python, JavaScript, and Linux**
- 🎯 **Open to collaborating on innovative projects and contributing to open-source**

---

## 🚀 Skills & Technologies

### 🔹 Programming Languages:
![Python](https://img.shields.io/badge/python-%233776AB.svg?style=for-the-badge&logo=python&logoColor=yellow)
![JavaScript](https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)

### 🔹 Cybersecurity:
![Linux](https://img.shields.io/badge/Linux-%23FCC624.svg?style=for-the-badge&logo=linux&logoColor=black)
![Networking](https://img.shields.io/badge/Networking-%2300C7B7.svg?style=for-the-badge&logo=windowsterminal&logoColor=white)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-%231877F2.svg?style=for-the-badge&logo=kalilinux&logoColor=white)

### 🔹 Development Tools:
![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-%23181717.svg?style=for-the-badge&logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-%23007ACC.svg?style=for-the-badge&logo=visualstudiocode&logoColor=white)

### 🔹 AI & ML:
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-%23FF6F00.svg?style=for-the-badge&logo=tensorflow&logoColor=white)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-%2300A4EF.svg?style=for-the-badge&logo=pytorch&logoColor=white)

---

## 📊 GitHub Stats

![](https://github-readme-stats.vercel.app/api?username=abdoaldoushy2009&theme=radical&hide_border=false&include_all_commits=true&count_private=true)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=abdoaldoushy2009&theme=radical&hide_border=false&include_all_commits=true&count_private=true&layout=compact)
![](https://github-profile-trophy.vercel.app/?username=abdoaldoushy2009&theme=radical&no-frame=true&no-bg=false&margin-w=4)
![](https://github-contributor-stats.vercel.app/api?username=abdoaldoushy2009&limit=5&theme=default&combine_all_yearly_contributions=true)

---

## 📫 Connect With Me

<p align="center">
  <a href="https://facebook.com/abdoaldoushy" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-%231877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"/>
  </a>
  <a href="https://instagram.com/abdo_aldoushy" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram"/>
  </a>
  <a href="https://linkedin.com/in/abdoaldoushy" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://pinterest.com/abdoaldoushy" target="_blank">
    <img src="https://img.shields.io/badge/Pinterest-%23E60023?style=for-the-badge&logo=pinterest&logoColor=white" alt="Pinterest"/>
  </a>
  <a href="https://tiktok.com/@abdoaldoushy" target="_blank">
    <img src="https://img.shields.io/badge/TikTok-%23000000?style=for-the-badge&logo=tiktok&logoColor=white" alt="TikTok"/>
  </a>
  <a href="mailto:abdoaldoushy@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

---

## 💰 Support Me

[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/abdo_aldoushy)
[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/abdo_aldoushy)

---

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

---
import pygame
import random

# تهيئة pygame
pygame.init()

# إعدادات اللعبة
WIDTH, HEIGHT = 600, 400
BLOCK_SIZE = 20
WHITE, GREEN, RED, BLACK = (255, 255, 255), (0, 255, 0), (255, 0, 0), (0, 0, 0)

# شاشة العرض
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Snake Game")

# الثعبان والطعام
snake = [(100, 100), (90, 100), (80, 100)]
snake_dir = (BLOCK_SIZE, 0)
food = (random.randint(0, WIDTH // BLOCK_SIZE - 1) * BLOCK_SIZE, 
        random.randint(0, HEIGHT // BLOCK_SIZE - 1) * BLOCK_SIZE)

clock = pygame.time.Clock()

# الحلقة الرئيسية للعبة
running = True
while running:
    screen.fill(BLACK)
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        elif event.type == pygame.KEYDOWN:
            if event.key == pygame.K_UP and snake_dir != (0, BLOCK_SIZE):
                snake_dir = (0, -BLOCK_SIZE)
            elif event.key == pygame.K_DOWN and snake_dir != (0, -BLOCK_SIZE):
                snake_dir = (0, BLOCK_SIZE)
            elif event.key == pygame.K_LEFT and snake_dir != (BLOCK_SIZE, 0):
                snake_dir = (-BLOCK_SIZE, 0)
            elif event.key == pygame.K_RIGHT and snake_dir != (-BLOCK_SIZE, 0):
                snake_dir = (BLOCK_SIZE, 0)

    # تحريك الثعبان
    new_head = (snake[0][0] + snake_dir[0], snake[0][1] + snake_dir[1])
    if new_head in snake or not (0 <= new_head[0] < WIDTH and 0 <= new_head[1] < HEIGHT):
        running = False  # نهاية اللعبة
    else:
        snake.insert(0, new_head)
        if new_head == food:
            food = (random.randint(0, WIDTH // BLOCK_SIZE - 1) * BLOCK_SIZE, 
                    random.randint(0, HEIGHT // BLOCK_SIZE - 1) * BLOCK_SIZE)
        else:
            snake.pop()

    # رسم الثعبان والطعام
    for block in snake:
        pygame.draw.rect(screen, GREEN, (*block, BLOCK_SIZE, BLOCK_SIZE))
    pygame.draw.rect(screen, RED, (*food, BLOCK_SIZE, BLOCK_SIZE))

    pygame.display.flip()
    clock.tick(10)

pygame.quit()


[![](https://visitcount.itsvg.in/api?id=abdoaldoushy2009&icon=0&color=0)](https://visitcount.itsvg.in)
