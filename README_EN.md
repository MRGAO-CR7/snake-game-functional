# Snake Game - Functional Programming Version

## 📋 Introduction

This is a Snake game implemented using **functional programming style**. The code primarily uses functions and global variables, demonstrating the characteristics of functional programming.

## 🎯 Programming Style Features

### 1. Using Global Variables
```python
# Game state stored in global variables
snake = []
food_pos = None
direction = (1, 0)
score = 0
game_over = False
```

### 2. Functional Design
- ✅ Each function completes a specific task
- ✅ Functions receive data through parameters
- ✅ Functions output results through return values or modifying global variables

### 3. Function Examples
```python
def move_snake():
    """Move snake"""
    global snake, direction, food_pos
    # ... logic processing

def check_collision(head_x, head_y):
    """Check collision"""
    # ... returns boolean
```

## 📁 Code Structure

```
snake_functional.py
├── Global variables (game state)
│   ├── Speed configuration (INITIAL_GAME_SPEED, MIN_GAME_SPEED, etc.)
│   └── Game state (snake, food_pos, score, current_speed, etc.)
├── Utility functions
│   ├── get_opposite_direction()
│   ├── is_valid_direction()
│   └── generate_food_position() - Randomly generates apple position
├── Game logic functions
│   ├── init_game() - Initialize game (reset speed)
│   ├── move_snake() - Move snake (speed increase logic)
│   ├── check_collision()
│   └── change_direction()
├── Drawing functions
│   ├── draw_apple() - Draw apple emoji
│   ├── draw_snake_head() - Draw snake head (with eyes)
│   ├── draw_snake_body() - Draw snake body
│   ├── draw_snake_tail() - Draw snake tail
│   ├── draw_grid()
│   └── draw_game()
├── GUI functions
│   ├── create_gui() - Create interface (optimized button style)
│   ├── on_key_press()
│   └── game_loop() - Use dynamic speed
└── main()
```

## 🎮 How to Run

```bash
python3 snake_functional.py
```

## ⚙️ Game Controls

- **Arrow Keys** or **WASD**: Control snake movement
- **Spacebar**: Pause/Resume
- **Restart Button**: Start new game

## 🎮 Game Features

### Speed System
- **Initial Speed**: 600ms (very slow, suitable for beginners)
- **Speed Increase**: Each apple 🍎 eaten increases speed (decreases delay by 5ms)
- **Maximum Speed**: 50ms (ultimate challenge)
- **Restart**: Speed resets to initial value

### Graphics Design
- **Apple**: Red apple emoji 🍎, clear and eye-catching
- **Snake Head**: Green circle with eyes (shows direction)
- **Snake Body**: Green circles with gradient effect
- **Snake Tail**: Smaller green circle, clearly distinguishable
- **All Snake Parts**: Unified green color scheme

### Apple Generation
- **Random Position**: Uses `random.randint()` to randomly select position each time
- **Smart Avoidance**: Ensures apples don't spawn on snake body
- **Instant Refresh**: Generates new position immediately after eating

### UI Optimization
- **Button Style**: Light gray background + dark text, clear and readable
- **Visual Feedback**: Buttons have 3D effect (raised relief)
- **Beautiful Interface**: Unified color scheme

## 💡 Pros and Cons of Functional Programming

### ✅ Advantages
- Simple and intuitive code structure
- Clear function responsibilities
- Suitable for small projects

### ⚠️ Disadvantages
- Global variables may cause state management confusion
- Difficult to extend and maintain
- High coupling between functions

## 📚 Learning Points

1. **Global Variable Usage**: Understand when to use global variables
2. **Function Design**: How to design single-responsibility functions
3. **State Management**: How to manage state in functional programming
4. **GUI Programming**: Basic tkinter usage

## 🔄 Compare with OOP Version

Check out `../oop_version/` to learn about the advantages of object-oriented programming!
