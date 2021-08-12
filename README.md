# lab1-
this contains lab1 assignment population growth
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // TODO: Prompt for start size
    int start;
    do 
    {
         start = get_int("Start? ");
        
    }
    while (start < 9);
    
    // TODO: Prompt for end size
    int end;
    do
    {
        end = get_int("End? ");
    }
    while (end < start);
    // TODO: Calculate number of years until we reach threshold
    int years = 0;
    int netGain = (start/3) - (start/4);
    start = start + netGain;
    do 
    {
        start = start + netGain;
        years++;
    }
    while (start < end);
    // TODO: Print number of years
    printf("Years: %i", years);
}
