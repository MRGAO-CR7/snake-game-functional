[中文版](README_CN.md) | [English](README.md)

# 贪吃蛇游戏 - 函数式编程版本

## 📋 简介

这是使用**函数式编程风格**实现的贪吃蛇游戏。代码主要使用函数和全局变量，展示了函数式编程的特点。

## 🎯 编程风格特点

### 1. 使用全局变量
```python
# 游戏状态存储在全局变量中
snake = []
food_pos = None
direction = (1, 0)
score = 0
game_over = False
```

### 2. 函数式设计
- ✅ 每个函数完成一个特定任务
- ✅ 函数通过参数接收数据
- ✅ 函数通过返回值或修改全局变量输出结果

### 3. 函数示例
```python
def move_snake():
    """移动蛇"""
    global snake, direction, food_pos
    # ... 逻辑处理

def check_collision(head_x, head_y):
    """检查碰撞"""
    # ... 返回布尔值
```

## 📁 代码结构

```
snake_functional.py
├── 全局变量（游戏状态）
│   ├── 速度配置（INITIAL_GAME_SPEED, MIN_GAME_SPEED等）
│   └── 游戏状态（snake, food_pos, score, current_speed等）
├── 工具函数
│   ├── get_opposite_direction()
│   ├── is_valid_direction()
│   └── generate_food_position() - 随机生成苹果位置
├── 游戏逻辑函数
│   ├── init_game() - 初始化游戏（重置速度）
│   ├── move_snake() - 移动蛇（速度递增逻辑）
│   ├── check_collision()
│   └── change_direction()
├── 绘制函数
│   ├── draw_apple() - 绘制苹果emoji
│   ├── draw_snake_head() - 绘制蛇头（带眼睛）
│   ├── draw_snake_body() - 绘制蛇身
│   ├── draw_snake_tail() - 绘制蛇尾
│   ├── draw_grid()
│   └── draw_game()
├── GUI函数
│   ├── create_gui() - 创建界面（优化按钮样式）
│   ├── on_key_press()
│   └── game_loop() - 使用动态速度
└── main()
```

## 🔧 环境配置

### macOS
1. **安装 Python 3.11+**（如果尚未安装）：
   ```bash
   brew install python3
   ```

2. **安装 tkinter**（GUI 所需）：
   ```bash
   brew install python-tk
   ```

3. **验证安装**：
   ```bash
   python3 -c "import tkinter; print('tkinter 已就绪!')"
   ```

### Windows
1. **从 [python.org](https://www.python.org/downloads/) 安装 Python 3.11+**
   - ✅ 安装时勾选 "Add Python to PATH"
   - ✅ Windows 版本的 Python 默认包含 tkinter

2. **验证安装**：
   ```cmd
   python -c "import tkinter; print('tkinter 已就绪!')"
   ```

## 🎮 运行方式

```bash
python3 snake_functional.py
```

## ⚙️ 游戏控制

- **方向键** 或 **WASD**：控制蛇的移动
- **空格键**：暂停/继续
- **重新开始按钮**：开始新游戏

## 🎮 游戏特色

### 速度系统
- **初始速度**：600ms（很慢，适合新手）
- **速度递增**：每吃一个苹果🍎，速度增加（延迟减少5ms）
- **最快速度**：50ms（挑战极限）
- **重新开始**：速度重置为初始值

### 图形设计
- **苹果**：使用红色苹果emoji 🍎，清晰醒目
- **蛇头**：绿色圆形，带眼睛（根据移动方向显示）
- **蛇身**：绿色圆形，渐变效果
- **蛇尾**：较小的绿色圆形，区分明显
- **所有蛇的部分**：统一的绿色系配色

### 苹果生成
- **随机位置**：每次生成时使用`random.randint()`随机选择位置
- **智能避让**：确保苹果不会生成在蛇身上
- **即时刷新**：吃到苹果后立即生成新位置

### UI优化
- **按钮样式**：浅灰背景 + 深色文字，清晰易读
- **视觉反馈**：按钮有立体效果（raised relief）
- **界面美观**：统一的配色方案

## 💡 函数式编程的优缺点

### ✅ 优点
- 代码结构简单直观
- 函数职责清晰
- 适合小型项目

### ⚠️ 缺点
- 全局变量可能导致状态管理混乱
- 难以扩展和维护
- 函数之间耦合度高

## 📚 学习要点

1. **全局变量的使用**：理解何时使用全局变量
2. **函数设计**：如何设计职责单一的函数
3. **状态管理**：如何在函数式编程中管理状态
4. **GUI编程**：tkinter的基本使用

## 🔄 对比面向对象版本

查看 `../oop_version/` 了解面向对象编程的优势！
