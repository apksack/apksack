import shutil
import os

def download_game_file(source_path, destination_path):
    """
    Copy the game file from source_path to destination_path.
    
    Parameters:
        source_path (str): Path to the game file.
        destination_path (str): Path where the game file will be copied.
    """
    if os.path.exists(source_path):
        try:
            shutil.copyfile(source_path, destination_path)
            print("Game file downloaded successfully!")
        except Exception as e:
            print(f"Error: {e}")
    else:
        print("Error: Source file not found.")

# Example usage
source_file_path = "C:/offline_games/my_game.exe"
destination_file_path = "D:/downloads/my_game.exe"

download_game_file(source_file_path, destination_file_path)
