#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <time.h>

//FUNCTION USED TO INPUT THE NUMBER OF FACES OF DICE AND THE NUMBER OF THROWS
int user_input(int e, char f[])             //DECLARING FUNCTION WITH PARAMETERS
{
    printf("\nENTER NUMBER OF %s: ", f);    //PROMPTING THE USER TO INPUT A NUMBER
    scanf("%d", &e);                        //STORING THE NUMBER IN VARIABLE
    return e;                               //RETURNING THE VALUE OF THE VARIABLE TO THE MAIN
}

//FUNCTION TO CHECK IF THE INPUT ENTERED IS WITHIN THE RANGE OF VALUES ACCEPTED
int input_checker(int g, char h[])                  //DECLARING FUNCTION WITH PARAMETERS
{
    printf("\nInvalid number of %s entered", h);    //DISPLAYING AN ERROR MESSAGE
    printf("\nRe-enter number of %s: ", h);         //PROMPTING THE USER TO RE-ENTER THE NUMBER
    scanf("%d", &g);                                //STORING THE NUMBER IN VARIABLE
    return g;                                       //RETURNING THE VALUE OF THE VARIABLE TO THE MAIN
}

//FUNCTION TO GENERATE RANDOM NUMBERS
int random_generator(int d)                 //DECLARING FUNCTION WITH PARAMETERS
{
    int random_number;                      //DECLARING LOCAL VARIABLE
    random_number = ((rand() % d) + 1);     //GENERATING THE RANDOM NUMBER
    printf("%d\n", random_number);          //DISPLAYING THE RANDOM NUMBER THAT HAS BEEN GENERATED
    return random_number;                   //RETURNING THE VALUE OF THE VARIABLE TO THE MAIN
}

//FUNCTION TO CALCULATE THE PERCENTAGE OF OCCURRENCE
int percentage_calculator(int a, int b, int c)                  //DECLARING FUNCTION WITH PARAMETERS
{
    float percentage;                                           //DECLARING LOCAL VARIABLE
    percentage = (((float)c / b) * 100);                        //CALCULATING THE PERCENTAGE FOR THE OCCURRENCE OF A CERTAIN NUMBER
    printf("\nOccurrences of %d : %.2f%%", a, percentage);      //DISPLAYING THE PERCENTAGE
}



int main()
{
       //ASCII ART OF DICE ROLLING PROGRAM
 printf("***STARTING***\n");
printf("***DICE ROLLING PROGRAM***\n");

printf(".........\n");
printf(":~, *   * ~,\n");
printf(": ~, *   * ~.\n");
printf(":  ~........~\n");
printf(": *:         :      ~'~,\n");
printf(":  :         :    ~' *  ~,\n");
printf("~* :    *    : ,~' *    * ~,\n");
 printf(" ~,:         :.~,*    *  ,~ :\n");
  printf("  ~:.........::  ~, *  ,~   :\n");
              printf("              : *  ~,,~  *  :\n");
              printf("              :* * * :  *   :\n");
              printf("               ~, *  : *  ,~\n");
                 printf("                 ~,  :  ,~\n");
                   printf("                   ~,:,~\n\n");


    //DECLARING VARIABLES
    int num_of_faces, num_of_throws;
    int i, x, y;
    int random_number;


    //INPUTTING VALUE FOR THE NUMBER OF FACES OF THE ROLLING DICE
    //CALLING THE FUNCTION user_input TO ENABLE INPUT OF VALUE
    num_of_faces = user_input(num_of_faces, "FACES OF DICE");

    //CHECKING IF THE INPUT OF THE NUMBER OF FACES IS WITHIN THE REQUIRED RANGE
    //CALLING FUNCTION input_checker TO CHECK FOR THE INPUT CRITERIA
    while(num_of_faces <= 1 || num_of_faces >= 25)
    {
        num_of_faces = input_checker(num_of_faces, "faces");
    }

    //INPUTTING VALUE FOR THE NUMBER OF THROWS OF THE ROLLING DICE
    //CALLING THE FUNCTION user_input TO ENABLE INPUT OF VALUE
    num_of_throws = user_input(num_of_throws, "THROWS");

    //CHECKING IF THE INPUT OF THE NUMBER OF THROWS IS WITHIN THE REQUIRED RANGE
    //CALLING FUNCTION input_checker TO CHECK FOR THE INPUT CRITERIA
    while(num_of_throws <= 1 || num_of_throws >= 500)
    {
        num_of_throws = input_checker(num_of_throws, "throws");
    }

    //WRITING A PRINT FUNCTION TO CHANGE LINE TO ENSURE BETTER PRESENTATION OF DATA DURING PROCESSING
    printf("\n");

    //INPUTTING NUMBER OF FACES IN A NEW VARIABLE FOR USE IN LOOP
    //INPUTTING NUMBER OF THROWS IN A NEW VARIABLE FOR USE IN LOOP
    x = num_of_faces;
    y = num_of_throws;

    //DECLARING ARRAY COUNT TO STORE THE VALUE OF EACH FACE OF THE DICE
    int count[x];

    //ASSIGNING EACH POSITION OF THE ARRAY A VALUE OF 0 TO ENSURE GOOD INCREMENTATION
    for (x = 1; x < (num_of_faces + 1); ++x)
    {
        count[x-1] = 0;
    }

    //FUNCTION TO PREVENT THE RANDOMLY GENERATED NUMBER TO BE STORED FOR FUTURE USE
    //NUMBER GENERATED WILL BE GIVEN AN ADDRESS AND THIS ADDRESS WILL BE ERASED AFTER DISPLAY TO ENABLE A NEW NUMBER TO BE ASSIGNED THIS ADDRESS
    srand(time(0));

    //GENERATING A RANDOM NUMBER FOR EACH THROW BY USING A FOR LOOP
    for (i = 0; i < num_of_throws; ++i)
    {
        random_number = random_generator(num_of_faces);         //CALLING FUNCTION random_generator TO GENERATE A RANDOM NUMBER

        for (x = 1; x < (num_of_faces + 1); ++x)
        {
            if (x == random_number)     //CHECKING IF RANDOM NUMBER IS THE SAME AS THE VALUE OF x
            {
                count[x-1] += 1;        //INCREMENTING THE COUNT AT A CERTAIN POSITION IF THE VALUE GENERATED IS THE SAME AS x
            }
        }
    }

    //WRITING A PRINT FUNCTION TO CHANGE LINE TO ENSURE BETTER PRESENTATION OF DATA DURING PROCESSING
    printf("\n");

    //DISPLAYING THE FACE NUMBER THAT HAS BEEN GENERATED AND THE NUMBER OF TIMES IT HAS BEEN GENERATED
    for (x = 1; x < (num_of_faces + 1); ++x)
    {
        printf("Number %d has been generated %d times\n", x, count[x-1]);
    }

    //CALCULATING THE PERCENTAGE OF OCCURRENCE OF EACH FACE NUMBER
    for (x = 1; x < (num_of_faces + 1); ++x)
    {
         percentage_calculator(x, y, count[x-1]);       //CALLING FUNCTION percentage_calculator TO CALCULATE THE PERCENTAGE
    }

    //WRITING A PRINT FUNCTION TO CHANGE LINE TO ENSURE BETTER PRESENTATION OF DATA DURING PROCESSING
    printf("\n");

    return 0;
}
