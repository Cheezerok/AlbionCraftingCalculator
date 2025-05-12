# Albion Online Crafting Calculator

This application helps Albion Online players calculate crafting profits, track market prices, and make informed decisions about crafting and trading.

## Main Features

### 1. Database Management
- Store information about items, resources, prices, cities, and crafting recipes
- Track price history across different cities
- Filter and analyze price data

### 2. Profit Calculation
- Calculate crafting profits considering resource costs, taxes, and return rates
- Calculate refining profits for resources
- Compare prices across different cities to find the best places to buy and sell
- Analyze profit margins for different quality levels

### 3. OCR Processing
- Extract market data from screenshots using OCR (Optical Character Recognition)
- Automatically detect item names, prices, and quality levels from market UI
- Support for different item qualities (Normal, Good, Outstanding, Excellent, Masterpiece)
- Process multiple screenshots to gather more data
- **NEW**: Capture screenshots directly from clipboard
- **NEW**: Use hotkeys to capture and process screenshots (Alt+1, Alt+2, Alt+3)

## Installation

### Option 1: Run from executable (Windows only)
1. Download the executable from the release page
2. Run `AlbionCraftingCalculator.exe`
3. Make sure to install Tesseract OCR:
   - Download and install from https://github.com/UB-Mannheim/tesseract/wiki

### Option 2: Run from source code
1. Clone the repository:
```
git clone https://github.com/yourusername/albion-crafting-calculator.git
cd albion-crafting-calculator
```

2. Install dependencies:
```
pip install -r requirements.txt
```

3. Install Tesseract OCR:
   - Windows: Download and install from https://github.com/UB-Mannheim/tesseract/wiki
   - Linux: `sudo apt-get install tesseract-ocr`
   - Mac: `brew install tesseract`

4. Run the application:
```
python main.py
```

### Option 3: Build your own executable
1. Install the required dependencies
```
pip install -r requirements.txt
```

2. Run the build script:
```
python build_exe.py
```

3. The executable will be created in the `dist` folder

## Usage

1. Start the application:
   - If using executable: Run `AlbionCraftingCalculator.exe`
   - If using source code: Run `python main.py`

2. Use the tabs to navigate between different functionalities:
   - Database: Manage items, resources, and recipes
   - Profit Calculator: Calculate crafting and refining profits
   - OCR: Extract market data from screenshots

### Clipboard Integration and Hotkeys

The application supports capturing screenshots directly from the clipboard:

1. Take a screenshot in Albion Online (using Windows screenshot tool, Print Screen, or any other method)
2. The application will automatically detect the screenshot in the clipboard
3. Use the dropdown to select which screenshot position to use (top or bottom)
4. Click "Capture from Clipboard" to use the current clipboard content

**Hotkeys:**
- `Alt+1`: Capture and set as top screenshot
- `Alt+2`: Capture and set as bottom screenshot
- `Alt+3`: Process both screenshots

### Taking Screenshots for OCR

For best OCR results:
1. Set your game resolution to at least 1920x1080
2. Make sure the market UI is clearly visible with no overlapping elements
3. Take screenshots that show the item name, quality, and price clearly
4. Use the top screenshot for the upper part of the market UI and bottom screenshot for the lower part

## OCR Features

The OCR system includes:
- Item quality detection based on item frame color
- Precise price extraction from the price field
- Item name recognition from market listings
- Support for multiple languages (primarily English)
- Time data extraction to track listing age

## Data Structure

The application uses a SQLite database with the following tables:
- items: Stores information about crafted items
- resources: Stores information about resources
- cities: List of cities in Albion
- prices: Price data with support for different qualities
- crafting_recipes: Crafting recipe information
- recipe_resources: Resources required for each recipe

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Albion Online is a trademark of Sandbox Interactive GmbH
- This tool is not affiliated with or endorsed by Sandbox Interactive
- Thanks to the Albion Online community for providing feedback and suggestions 