# File-Handling-and-Exception-Handling-Assignment
File Read & Write Challenge 🖋️: Create a program that reads a file and writes a modified version to a new file.Error Handling Lab 🧪: Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.

def modify_file(input_file, output_file):
    try:
        # Open the input file for reading
        with open(input_file, 'r') as infile:
            content = infile.read()

        # Modify the content (e.g., convert to uppercase)
        modified_content = content.upper()

        # Open the output file for writing
        with open(output_file, 'w') as outfile:
            outfile.write(modified_content)

        print(f"Modified content written to '{output_file}' successfully.")

    except FileNotFoundError:
        print(f"Error: The file '{input_file}' was not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

# Example usage
input_file = 'input.txt'  # Replace with your input file path
output_file = 'output.txt'  # Replace with your desired output file path
modify_file(input_file, output_file)


