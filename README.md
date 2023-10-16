# vendingmachine

#include <stdio.h>

int ItemA(); // item A
int ItemB(); // item B
int ItemC(); // item C
int firstmenu(); 
int usermenu();
int adminmode();
int access();
int password = 1234; // admin password
int min = 5; // minimum quantity
float total_amount = 0.0f ;// total sale amount

int firstmenu()
 { 
    int modeselect;
    printf("press 1 to select adminmode \n") ;
    printf("press 2 to select consumermode \n") ;
    printf("press 0 to exit \n") ;
    scanf("%d", &modeselect);
    if (modeselect==1)
    {
        access();
    }
    else if (modeselect==2)
    {
        usermenu();
    }
    else 
    {
      printf("thank you \n");
    }

 }

int usermenu ()
{

    printf("Welcome to the Vending Machine \n");

    printf(" Press 1 for Item A \n"); 
    printf(" Press 2 for Item B \n"); 
    printf(" Press 3 for Item C \n");
    printf(" Press 4 to exit usermode \n");

    printf("Which item would you like? \n");

    char option;
    scanf("%d", &option);
    switch(option)
    {
        case 1:
        ItemA(); // calling function item a
        break;

        case 2:
        ItemB(); // calling function item b
        break;

        case 3:
        ItemC(); // calling function item c
        break;

        case 4:
        firstmenu();

        default:
        printf("input error \n");
    
    }
    
    return 0;
}
int ItemA()
    {
        int var1;
        printf ("This item is 0.25 dirham, would you like to purchase it? 1 for yes 0 for no \n");
        scanf("%d", &var1);
        if (var1==1)
        {
            printf("Please pay by price in only 1, 0.5, 0.25");
            scanf ;

        }
        else if (var1==0)
        {
           usermenu();
        }
        else
        {
            printf("Input error \n");
            usermenu();
        }
    }

int ItemB()
    {
        int var2;
        printf ("This item is 0.5 dirham, would you like to purchase it? 1 for yes 0 for no \n");
        scanf("%d", &var2);
        if (var2==1)
        {
            printf("Please pay by price in only 1, 0.5, 0.25");
            scanf ;

        }
        else if (var2==0)
        {
           usermenu();
        }
        else
        {
            printf("Input error \n");
            usermenu();
        }
    }

int ItemC()
    {
        int var3;
        printf ("This item is 1 dirham, would you like to purchase it? 1 for yes 0 for no \n");
        scanf("%d", &var3);
        if (var3==1)
        {
            printf("Please pay by price in only 1, 0.5, 0.25");
            scanf ;

        }
        else if (var3==0)
        {
           usermenu();
        }
        else
        {
            printf("Input error \n");
            usermenu();
        }        
    }

int access()
{
    int pass;
    printf("Welcome to admin mode \n");
    printf("Please enter the password \n");
    scanf("%d",&pass);
    if (pass==password)
    {
    printf("\nCorrect\n");
    adminmode();
    }
    else 
    {
    printf("\nIncorrect\n\n");
    firstmenu();
    }
}    
    
int adminmode()
{ 
    printf("Pick one of the following \n");
    printf("Press 1 for Replenish Items \n");
    printf("Press 2 for Change Item Prices \n");
    printf("Press 3 for display Item Prices \n");
    printf("Press 4 for Display Item Availability \n");
    printf("Press 5 for Exit Admin mode \n");

    char option2;
    scanf("%d", &option2);
    switch(option2)
     {
        case 1:

        break;

        case 2:

        break;

        case 3:

        break;

        case 4:

        break;

        case 5:
        firstmenu();
        break;

        default:
        printf("input error \n");
    

    }
}

int main()
{
    firstmenu();


}

