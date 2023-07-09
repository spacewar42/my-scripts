import os
import re

folder_path = os.path.dirname(os.path.abspath(__file__))

for filename in os.listdir(folder_path):
    if os.path.isfile(os.path.join(folder_path, filename)):
        file_name, file_extension = os.path.splitext(filename)
        match = re.search(r'\D(\d{2})\D', file_name)
        if match:
            target_number = match.group(1)
            new_filename = target_number + file_extension
            os.rename(os.path.join(folder_path, filename), os.path.join(folder_path, new_filename))
            print(f"Renamed {filename} to {new_filename}")

print("Renaming completed.")
input("Press Enter to exit.")
