# Folder Creation Script

This script is designed to create a main folder and multiple subfolders within it. The main functionality is to ensure the main folder exists and then create 10 subfolders with specified naming conventions.

## Usage

To use this script, ensure you have Python installed on your machine. Copy the script into a Python file (e.g., `create_folders.py`) and execute it.

## Code Explanation

The script performs the following steps:

1. **Import necessary module**:
    - `os` module is used to interact with the operating system, specifically for file and directory operations.

2. **Define the main folder path**:
    - The variable `main_folder` holds the path of the main folder where subfolders will be created.

3. **Check and create the main folder**:
    - The script checks if the main folder exists using `os.path.exists()`. If it does not exist, it creates the folder using `os.mkdir()`.

4. **Create subfolders**:
    - A `for` loop iterates over a range of numbers (10 to 25).
    - For each iteration, a subfolder name is created with the format `subfolder: X` where `X` is the current number in the loop.
    - The full path of the subfolder is constructed using `os.path.join()`.
    - Each subfolder is created using `os.mkdir()`.

5. **Completion message**:
    - After creating all the subfolders, a success message is printed.

### Script

```python
import os

# Name of the main folder
main_folder = "C:\\Users\\mrahe\\Desktop\\main folder"

# Create the main folder if it doesn't exist
if not os.path.exists(main_folder):
    os.mkdir(main_folder)

# Create 10 subfolders
for i in range(10, 26):
    subfolder_name = f'subfolder: {i}'
    subfolder_path = os.path.join(main_folder, subfolder_name)
    
    # Create the subfolder
    os.mkdir(subfolder_path)

print("subfolders created successfully.")
```

## Execution

1. Save the script to a Python file, e.g., `create_folders.py`.
2. Open a command prompt or terminal.
3. Navigate to the directory where the script is saved.
4. Run the script using the command:
    ```sh
    python create_folders.py
    ```

Upon execution, the script will create a main folder at `C:\\Users\\mrahe\\Desktop\\main folder` if it does not already exist. Inside this main folder, it will create 16 subfolders named `subfolder: 10` to `subfolder: 25`.

## Requirements

- Python 3.x
- Permission to create directories in the specified path

## Troubleshooting

- Ensure that the specified path in `main_folder` is correct and accessible.
- If the script fails due to permission issues, try running the script with elevated permissions.

## License

This script is released under the Apache.
```

Feel free to copy and paste this into your README file. Adjust the content as needed to fit your specific requirements.
