# QR Code Generator

A simple and user-friendly desktop application that generates QR codes from URLs using Python's Tkinter GUI framework.  
This project is available on hackr.io  
[QR Code Generator](https://hackr.io/blog/how-to-create-a-python-qr-code-generator?source=k8mepg2dMy)

## Overview

This application provides an intuitive graphical interface for creating QR codes from any URL. Users can input a URL, generate a QR code, and view it directly within the application. The generated QR code is also saved as a PNG file for external use.

## Features

- **Simple GUI**: Clean and modern interface built with Tkinter
- **URL Input**: Easy-to-use text entry field for URLs
- **QR Code Generation**: High-quality QR codes with error correction
- **Live Preview**: Generated QR codes are displayed immediately in the app
- **File Export**: Automatically saves QR codes as `qrcode.png`
- **Error Handling**: Validates input and provides user feedback
- **Responsive Design**: Well-organized layout with proper spacing and styling

## Requirements

- Python 3.11 or higher
- Required packages (automatically installed):
  - `qrcode` - QR code generation library
  - `pillow` - Image processing and display

## Installation & Setup

1. **Clone or download** this project to your local machine
2. **Install dependencies** - The required packages are automatically managed through the `pyproject.toml` file
3. **Run the application**:
   ```bash
   python main.py
   ```
## Alternative Installation   

These are the required libraries for this project   

I've used the following Python libraries:  

qrcode for generating QR codes.  
tkinter for creating the GUI.  
Pillow (PIL) for displaying the generated QR code.  

You can easily install them with this command:  

```pip install qrcode pillow```

## Usage

1. **Launch the application** by running `python main.py`
2. **Enter a URL** in the text input field (e.g., `https://www.example.com`)
3. **Click "Generate QR Code"** button
4. **View the result**:
   - The QR code will appear in the application window
   - A success message will confirm generation
   - The QR code is automatically saved as `qrcode.png` in the project directory

## Technical Details

### QR Code Configuration
- **Version**: 1 (21x21 modules)
- **Error Correction**: High level (ERROR_CORRECT_H)
- **Box Size**: 5 pixels per module
- **Border**: 2 modules wide
- **Colors**: Black foreground on white background

### GUI Components
- **Main Window**: 400x500 pixels with light blue background
- **URL Entry**: Helvetica font, 40 characters wide
- **Generate Button**: Styled with blue theme and hover effects
- **QR Display**: Centered image display area
- **Status Label**: Shows generation success/error messages

### File Structure
```
project/
├── main.py          # Main application file
├── qrcode.png       # Generated QR code (created after first use)
├── pyproject.toml   # Project dependencies
└── README.md        # This documentation
```

## Error Handling

The application includes built-in error handling:
- **Empty URL validation**: Prevents generation with blank input
- **Error dialog boxes**: Clear error messages for user guidance
- **Image processing errors**: Graceful handling of PIL/image operations

## Customization

You can easily modify the application by adjusting these parameters in `main.py`:

- **Window size**: Change `root.geometry("400x500")`
- **QR code size**: Modify `box_size` parameter
- **Colors**: Update `fill_color` and `back_color`
- **Error correction**: Change `error_correction` level
- **Styling**: Modify the `ttk.Style()` configurations

## Dependencies Explained

- **qrcode**: Core library for generating QR codes with various customization options
- **Pillow (PIL)**: Required for image processing, display, and saving QR codes as PNG files
- **tkinter**: Built-in Python GUI framework (no additional installation needed)

## License

This project is open source and available for educational and personal use.

## Troubleshooting

**Common Issues:**
- **Import errors**: Ensure all dependencies are installed via `uv` or `pip`
- **Display issues**: Verify that your system supports Tkinter GUI applications
- **File permissions**: Check write permissions in the project directory for saving QR codes

**Running the Application:**
- Use the "Run" button in your IDE, or
- Execute `python main.py` in the terminal
