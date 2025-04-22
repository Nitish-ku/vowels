# vowels
A c program that counts the number of vowels
// counts the number of vowels
#include <stdio.h>
#include <string.h>

int main(void)
{
    // array for string upto 49 character + \0
    char word[50];

    // getting user's input
    printf("Word: ");

    // reads a word with no spaces
    scanf("%s", word);

    // getting the length of the word entered by the user
    size_t word_length = strlen(word);

    // printing the length of the word entered by the user
    printf("Length of the word: %i\n", word_length);

    // counting vowels
    int number_of_vowels = 0;
    for (int i = 0; i < word_length; i++)
    {
        if (word[i] == 'a' || word[i] == 'e' || word[i] == 'i' || word[i] == 'o' ||
            word[i] == 'u' || word[i] == 'A' || word[i] == 'E' || word[i] == 'I' ||
            word[i] == 'O' || word[i] == 'U')
        {
            number_of_vowels++;
        }
    }

    printf("The word \"%s\" has %d vowel(s)", word, number_of_vowels);

    return 0;
}
