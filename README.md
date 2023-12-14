include <stdio.h>
#include <ctype.h>

int main()
{
	printf("GROUP MEMBERS ARE \n");
	printf("SAKWE JORIS-SWE\nCHE RENE-NWS\nTEMBE SANDRINE-DBMS\nAWO EKPO JEORG-NWS\n\n");
    char questions[][100] = {"1-what is e^0",
                              "2-solve for x where x-1=0",
                              "3-solve |x+2|>2",
                              "4-experess 10000 in standard form",
                              "5-what is the economic capital of cameroon",
                              "6-when did c language come into existence",
                              "7-Who is the father of c",
                              "8-what is 2^8",
                              "9-expeess 2 in binary",
                              "10-who came out with the law of gravitation"};


    char options[][100] = { "A. 0","B. 5","C. 1","D. NONE",
                            "A. 1","B. -2","C. 9","D. -1",
                            "A. 17","B. 0","C. 2","D. 3",
                            "A. 1.0*10^2","B. 10","C. 1.1^10","D .1.0*10^4",
                            "A. Yaounde","B. Douala","C. Bamenda","D. Buea",
                            "A.1969","B. 1972","C. 1975","D. 1999",
                            "A.Dennis Ritchie","B.Sakwe JOVI","C.Nikola Tesla","D.John Camet",
                            "A. 255","B. 299","C. 256","D. 8",
                            "A. 001","B. 111","C. 110","D. 00011",
							"A. Isaac Netwon", "B.TESLA", "C.CHRISTOPER COLOMBUS","D. SAKWE JOVI"};

    char answers[10] = {'C', 'A', 'B', 'D', 'B', 'A', 'A', 'C', 'D', 'A'};
    int numberofquestion = sizeof(questions)/sizeof(questions[0]);
    
    char choose;
    int score;

    printf("programming quiz\n\n");
    for(int i=0;i<numberofquestion;i++)
    {
        printf("%s\n",questions[i]);
         for (int j = (i * 4); j < (i * 4) + 4; j++)
        {
          printf("%s\n",options[j]);
        }
        
        printf("choose :");
        scanf("%c",&choose);
        scanf("%c");
        
        choose = toupper(choose);
        
        if(choose == answers[i])
        {
        	printf("correct \n");
        	score ++;
		}
        else{
        	printf("wrong\n");
        	
		}
    }
    printf("TOTAL SCORE %d/%d\n",score,numberofquestion);
    
    if(score <= 3)
    {
    	printf("you need to put more effort\n");
	}
	else if(score >=5)
	{
		printf("you can do it\n");
	}
	else if(score >=6)
	{
		printf("good job");
	}
	else if(score >= 9)
	{
		printf("excellent");
	}

   

    return 0;
}
