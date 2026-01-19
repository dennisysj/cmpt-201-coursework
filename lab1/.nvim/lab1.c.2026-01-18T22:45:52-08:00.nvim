#define _POSIX_C_SOURCE 200809L
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {

  printf("Please Enter Some Text:> ");

  char *buff = NULL;
  size_t size = 0;

  if (getline(&buff, &size, stdin) != -1L) {
    // tokenizer
    char *input_str = buff;
    char *delim = " \t\n\r";
    char *token = NULL;
    char *saveptr = NULL;

    while ((token = strtok_r(input_str, delim, &saveptr)) != NULL) {
      printf("Token: '%s'\n", token);
      input_str = NULL;
    }
    // else {
    // printf("Getline failure.\n");
    //}
    free(buff);
  }

  return 0;
}
