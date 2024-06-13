#Alphabet rangoli

def print_rangoli(size):
    # your code goes here

    import string
    # Get the lowercase alphabet
    alpha = string.ascii_lowercase

    # Calculate the width of the rangoli
    width = 4 * size - 3

    # Initialize a list to store each line of the rangoli
    lines = []

    for i in range(size):
        # Get the part of the alphabet we need for the current line
        s = '-'.join(alpha[size-1:i:-1] + alpha[i:size])
        # Center the line with dashes
        lines.append(s.center(width, '-'))

    # Join the upper half and the mirrored lower half
    print('\n'.join(lines[:0:-1] + lines))


if __name__ == '__main__':
    n = int(input())
    print_rangoli(n)
