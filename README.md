# 🐱 or 🥐 Power BI Game Challenge

![Game Screenshot](./assets/game-screenshot.png) *(replace with your actual screenshot)*

## 🎮 About the Project
An interactive "Cat or Croissant" game built in Power BI, inspired by Workout Wednesday's May DAX challenge. This project demonstrates creative use of DAX, bookmarks, and custom visuals in Power BI for gamification.

## ✨ Enhanced Features
✅ **Dynamic Game Mechanics**  
- Randomized image order on each refresh  
- Smart game state detection (Win/Lose/In Progress)  
- One-click reset functionality  

✅ **Immersive Visual Design**  
- Custom-designed UI buttons  
- Conditional formatting for game states  
- Responsive layout for all devices  

✅ **Advanced DAX Implementation**  
- Game logic implemented through measures  
- Dynamic scoring system  
- Session tracking  

## 🛠️ Technical Implementation

### 📊 Power BI Components Used
- **DAX Measures** for game logic
- **Bookmarks** for game reset
- **Custom Visuals** for image selection
- **Conditional Formatting** for visual feedback
- **M Query** for data preprocessing

### 🎨 Design Elements
- Custom button graphics (created in [Tool Name])
- Themed color palette
- Animated transitions

## 📋 How to Play
1. Click "Start Game" to begin
2. Select all cat images 🐱
3. Avoid selecting any croissants 🥐
4. Win by selecting all cats with no croissants
5. Use "Reset" to start a new game

## 🚀 Getting Started
1. Clone this repository
2. Open `CatOrCroissant.pbix` in Power BI Desktop
3. Refresh the dataset connection
4. Enter "Play Mode" (View > Page View > Actual Size)

## 📈 Advanced Features to Implement
Here are some enhancements you could add:

1. **Scoring System**  
   ```dax
   Score = 
   VAR CatsSelected = COUNTROWS(FILTER('Table', [IsCat] = TRUE && [IsSelected] = TRUE))
   RETURN CatsSelected * 100
