1 File read and write 
# Open and read the original file
with open("input.txt", "r") as infile:
    content = infile.read()

# Modify the content (e.g., convert to uppercase)
modified_content = content.upper()

# Write the modified content to a new file
with open("output.txt", "w") as outfile:
    outfile.write(modified_content)

print("File has been modified and saved as 'output.txt'.")

error handling lab
filename = input("Enter the filename to read: ")

try:
    with open(filename, "r") as file:
        content = file.read()
        print("\nFile content:\n")
        print(content)
except FileNotFoundError:
    print("Error: The file does not exist. Please check the filename and try again.")
except PermissionError:
    print("Error: You don't have permission to read this file.")
except Exception as e:
        print(f"An unexpected error occurred: {e}")
    ![1000091748](https://github.com/user-attachments/assets/28641299-ee72-4732-a52b-905b03d36ed5)
