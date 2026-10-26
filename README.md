# COSC-7
I'm sorry its late I was having technical issues with my computer
def display_file_head():
    # Prompt the user for the name of the file
    filename = input("Enter the filename: ")

    try:
        # Open the file in read mode
        with open(filename, 'r') as file:
            # Read and print up to the first 5 lines
            for i in range(5):
                line = file.readline()
                
                # If readline() returns an empty string, the end of the file is reached
                if not line:
                    break
                
                # Print the line (strip trailing newline to avoid double spacing)
                print(line, end='')
                
    except FileNotFoundError:
        print(f"Error: The file '{filename}' could not be found.")
    except Exception as e:
        print(f"An error occurred: {e}")

# Run the program
if __name__ == "__main__":
    display_file_head()
