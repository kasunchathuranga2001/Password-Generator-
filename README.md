# Password-Generator-
Introduction:
The provided C code generates a random password of a user-specified length. The password consists of a combination of digits, lowercase letters, uppercase letters, and symbols. The code uses the standard C library functions for generating random numbers and handling strings.

Functionality:

The program prompts the user to input the desired length of the password.
If the user enters an invalid length (i.e., less than or equal to zero), an error message is displayed, and the program terminates.
The code then dynamically allocates memory to store the password, considering the length provided by the user.
Four character types are available for generating the password: digits, lowercase letters, uppercase letters, and symbols.
A random character type is selected for each position in the password, and a random character from the corresponding character set is chosen for that position.
Finally, the generated password is printed on the screen.
Code Review:

The code overall is well-structured and easy to read.
The use of malloc to allocate memory for the password is appropriate.
The logic for generating the random password based on the user's input length and character types is sound.
The check for an invalid password length (less than or equal to zero) is correctly handled.
The use of srand to seed the random number generator is essential for generating different passwords in each run.
The time(NULL) * getpid() combination provides a reasonably good seed value for the random number generator.
The code uses printf and scanf to interact with the user effectively.
Possible Improvements:

To improve the randomness of the generated password, the seeding of the random number generator can be further enhanced. The current method uses the process ID and the current time, but it may not be entirely unpredictable. Consider using a more sophisticated approach to seed the random number generator, like reading from /dev/urandom.
It's good practice to free the allocated memory (password) using free at the end of the program, even though the operating system will automatically reclaim the memory when the program exits.
Conclusion:
The provided C code successfully generates random passwords based on user input. The code demonstrates the use of dynamic memory allocation, random number generation, and basic string manipulation in C. With minor improvements for better seeding and memory management, this code can be a useful utility for generating secure passwords.

Recommendation:
Overall, the code fulfills the assignment requirements. I recommend further testing the code with various input lengths and validating the generated passwords' randomness. Additionally, consider implementing the improvements suggested in the "Possible Improvements" section to enhance the code's overall quality.
