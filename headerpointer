#include"ctype.h"

int get_string_length(const char input[]) {
    int length = 0;
    while (input[length] != '\0') {
        length++;
    }
    return length;
}


void copy_string(char destination[], const char source[]) {
    int index = 0;
    while (source[index] != '\0') {
        destination[index] = source[index];
        index++;
    }
    destination[index] = '\0';
}

int compare_strings(const char str1[], const char str2[]) {
    int index = 0;
    while (str1[index] != '\0' && str2[index] != '\0') {
        if (str1[index] != str2[index]) {
            return str1[index] - str2[index];
        }
        index++;
    }
    return str1[index] - str2[index];
}

void to_uppercase(char input_string[]) {
    int index = 0;
    while (input_string[index] != '\0') {
        input_string[index] = toupper((unsigned char)input_string[index]);
        index++;
    }
}

void to_lowercase(char input_string[]) {
    int index = 0;
    while (input_string[index] != '\0') {
        input_string[index] = tolower((unsigned char)input_string[index]);
        index++;
    }
}

int count_vowels(const char input_string[]) {
    int vowel_count = 0;
    int index = 0;
    while (input_string[index] != '\0') {
        char character = tolower((unsigned char)input_string[index]);
        if (character == 'a' || character == 'e' || character == 'i' ||
            character == 'o' || character == 'u') {
            vowel_count++;
        }
        index++;
    }
    return vowel_count;
}

void reverse_string(char input_string[]) {
    int length = get_string_length(input_string);
    for (int left = 0, right = length - 1; left < right; left++, right--) {
        char temp = input_string[left];
        input_string[left] = input_string[right];
        input_string[right] = temp;
    }
}

void sort_strings(char array[][100], int count) {
    char temp[100];
    for (int i = 0; i < count - 1; i++) {
        for (int j = i + 1; j < count; j++) {
            if (compare_strings(array[i], array[j]) > 0) {
                copy_string(temp, array[i]);
                copy_string(array[i], array[j]);
                copy_string(array[j], temp);
            }
        }
    }
}

void reverse_words(char input_string[]) {
    char words[100][100];
    int word_count = 0;
    int char_index = 0;
    int word_index = 0;

    for (int i = 0; input_string[i] != '\0'; i++) {
        if (input_string[i] != ' ') {
            words[word_count][char_index++] = input_string[i];
        } else {
            words[word_count][char_index] = '\0';
            word_count++;
            char_index = 0;
        }
    }
    words[word_count][char_index] = '\0'; 
    word_count++;

   
    int str_index = 0;
    for (int i = word_count - 1; i >= 0; i--) {
        int j = 0;
        while (words[i][j] != '\0') {
            input_string[str_index++] = words[i][j++];
        }
        if (i > 0) {
            input_string[str_index++] = ' ';
        }
    }
    input_string[str_index] = '\0';
}
