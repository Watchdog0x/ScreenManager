# GetScreen

GetScreen is a Python class that retrieves information about display screens connected to a Windows system using the ctypes library. It provides methods to obtain the device name, coordinates, dimensions, and primary status of a specified screen.

## Persistence of Screen Identification
The GetScreen class uses the device name of the screen to consistently identify the same screen even after a system restart. This ensures that the screen with a specific device name will be recognized consistently across different system sessions.

Please note that the device name may change if the display configuration is modified (e.g., connecting or disconnecting displays).

## Prerequisites

- Python 3.x
- Windows operating system

## Usage

```python
screen = 1
get_screen = GetScreen(screen)
display_info = get_screen.display_name
print(display_info)

left, top, right, bottom = get_screen.left_top_right_bottom
print(f"Left: {left}, Top: {top}, Right: {right}, Bottom: {bottom}")

x, y, width, height = get_screen.x_y_width_height
print(f"X: {x}, Y: {y}, Width: {width}, Height: {height}")

is_primary = get_screen.is_primary_screen
print(f"Is Primary: {is_primary}")
```

## DOC
https://learn.microsoft.com/en-us/windows/win32/api/_gdi/
