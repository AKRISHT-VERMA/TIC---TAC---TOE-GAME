# 🎮 Tic Tac Toe  

A fun **Tic Tac Toe game** built with Python 🐍.  
Play in the **terminal** using **dial pad-style numbering (1–9)** for selecting box positions.  

---

## ✨ Features  
✅ Classic **3x3 Tic Tac Toe** board  
✅ Play with a friend in the terminal  
✅ Uses **dial pad layout** for moves  
✅ Detects **win** and **draw** conditions  
✅ Beginner-friendly, clean Python code  

---

## ⚙️ Installation  

Clone the repo:  
```bash
git clone https://github.com/AKRISHT-VERMA/TIC---TAC---TOE-GAME.git
cd tic-tac-toe
```
## CODE
```python


print("🎮 WELCOME TO THE TIC - TAC - TOE GAME 🎮")
print("📌 THIS GAME USES DIAL-PAD STYLE NUMBERING (1–9) FOR POSITIONS\n")

# Initial board setup
line1 = [1, 2, 3]
line2 = [4, 5, 6]
line3 = [7, 8, 9]


def display():
    print("\n🟦 THE CURRENT TIC - TAC - TOE BOARD 🟦")
    print(line1)
    print(line2)
    print(line3)

def check_winner():
    # horizontal check
    if line1[0] == line1[1] == line1[2]:
        return True
    elif line2[0] == line2[1] == line2[2]:
        return True
    elif line3[0] == line3[1] == line3[2]:
        return True
    
    # vertical check
    if line1[0] == line2[0] == line3[0]:
        return True
    elif line1[1] == line2[1] == line3[1]:
        return True
    elif line1[2] == line2[2] == line3[2]:
        return True
    
    # diagonal check
    if line1[0] == line2[1] == line3[2]:
        return True
    elif line1[2] == line2[1] == line3[0]:
        return True

    return False

def position():
    while True:
        try:
            choice = int(input("\n👉 Enter the position (1-9): "))
            if choice not in range(1, 10):
                print("⚠️ Invalid choice! Pick a number between 1 and 9.")
                continue
        except ValueError:
            print("⚠️ Please enter a valid number.")
            continue

        # Place symbol
        if choice in line1:
            symbol = input("❓ Enter your symbol ('X' or 'O'): ").upper()
            if symbol not in ["X", "O"]:
                print("⚠️ Invalid symbol! Choose 'X' or 'O'.")
                continue
            line1[line1.index(choice)] = symbol
            break
        elif choice in line2:
            symbol = input("❓ Enter your symbol ('X' or 'O'): ").upper()
            if symbol not in ["X", "O"]:
                print("⚠️ Invalid symbol! Choose 'X' or 'O'.")
                continue
            line2[line2.index(choice)] = symbol
            break
        elif choice in line3:
            symbol = input("❓ Enter your symbol ('X' or 'O'): ").upper()
            if symbol not in ["X", "O"]:
                print("⚠️ Invalid symbol! Choose 'X' or 'O'.")
                continue
            line3[line3.index(choice)] = symbol
            break
        else:
            print("🚫 That position is already taken!")

# Game loop
display()
for _ in range(9):  # max moves
    position()
    display()
    if check_winner():
        print("\n🎉 Congratulations! You won the game 🏆")
        break
else:
    print("\n🤝 It's a draw!")
```

## 🛠️ Technologies Used

 .Python 3.13.5 🐍

## 🚀 Future Improvements

  .🤖 Add AI opponent (minimax algorithm)

   .🔁 Option for replay without restarting

   .🎨 Improve UI/UX (colored board, better layout)

   .🖼️ Create a GUI version using Tkinter/PyGame

