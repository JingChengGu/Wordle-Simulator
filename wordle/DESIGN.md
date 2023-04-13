
####DESIGN  

#####Purpose of the program

The program is an implementation of our own wordle game. There will be a target word for the player to guess and the
program will respond to the player to indicate if the characters in the word is correct or not. The letters x, y, and g
will appear as indications. X means that the character is not in the word, y means that the character is in the word but
in the wrong position, and g means that the character is in the word and in the right position. All words will be 5
characters long pulled from an external text file. 

#####Description and pseudocode

The score guess function is made to compare the secret word with the word guessed by the player. Then a result word
would be stored to indicate if the characters in the guessed words match with the secret word or not. This will be
displayed in a 5 character fashion made up with the characters x, y, and g.

score guess function(secret, guess, result)
    if(strcmp(secret, guess))
        for(i - 5)
          for(j - 5)
            if secret[i] = guess[i]
                result[i] = 'g'
            else if scret[i] = guess[j]
                result[i] = 'y'
            else
                result[i] = 'x'
    return result

The valid guess function returns true if the guess is one of the strings in the vocabulary array and false otherwise.
Search through the array to determine how many strings are in the string array and store that value.

valid guess function(guess, vocabulary, number words)
    for(i in vocabulary)
        if(strcmp(vocabulary[i], guess)
            true
        else
            false
    number words = sizeof(vocabulary)/sizeof(vocabulary[0])

The load vocabulary function returns an array of strings where each string contains a words from the given text file.
The number words pointer would be the number of elements in the array. There will be allocation of memory and it must
increase as the array grow bigger. The program uses fopen fget and fclose to access the text file.

load vocabulary function(file name, number words)
    pointer of pointer out = NULL
    buff[7]
    File* f = fopen(file name, r)
    out = calloc(1, sizeof(char))
    outpos = 0
    while(fgets(buff, 7, f) is not NULL)
        if(sizeof(out[outpos]) < sizeof(buff))
            char outnew = relloc(out, 100*sizeof(char))
            out[outpos] = strndup(buff, 5)
        else
            out[outpos] = strndup(buff, 5)
        outpos +=1
    return out;

The free vocabulary function frees the strings in the vocabulary and the pointer vocabulary through looping through the
vocabulary array.

free vocabulary function(vocabulary, number words)
    for i in vocabulary
        free vocabulary[i]
    free *vocabulary


