#include<stdio.h>
#include<string.h>
#include<stdlib.h> 
int BMI(int num);                 /* DECLARATION: program allocator function according to the BMI of the customer*/
int diet_c();                     /* DECLARATION: high cardio function*/
int diet_ww();                    /* DECLARATION: weight gainer diet function*/
int diet_fr();                    /* DECLARATION: fat reduction diet function*/
int exxit();                      /* DECLARATION: program exiting function*/
int exper(char ask);              /* DECLARATION: customer sorter function*/
int disclaimer();                 /* DECLARATION: disclaimer function*/

int main(){

    disclaimer();
    char ask;                   
    char username[15];
    char pass[15];
    printf("-----WELCOME TO THE GYM MANAGEMENT PROGRAM-----\n");
    printf("LET'S LOG YOU INSIDE THE PROGRAM\n");
    printf("Enter your username:\n");          /*USERNAME OF THE GYM TRAINER*/
    scanf("%s",&username);
    printf("Enter your password:\n");          /*PASSWORD OF THE GYM TRAINER*/
    scanf("%s",&pass);
    if(strcmp(username,"admin")==0){
        if(strcmp(pass,"admin123")==0){       //username must be equal to admin and password must be equal to admin123//
        printf("\nWelcome!!!Login Success!\n");

        system("pause");   /*system command .. function = pauses the program and displayes "Press any KEY to continue"*/  
        system("cls");     /*system command .. function = closes the current screen and displayes the next code in fresh window*/ 

    printf("\n");
    printf("\t\t\t+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++\n");
    printf("\t\t\t+++++++++++++++++++++++WELCOME TO GYM MANAGEMENT PROGRAM+++++++++++++++++++\n");
    printf("\t\t\t+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++\n");

    printf("\nPLEASE ENTER THE FOLLOWING DETAILS.");
    printf("DOES THE CLIENT HAVE ANY EXPERIENCE OF A GYM ?\n");
    scanf("%s",&ask);
    exper(ask);                /*CUSTOMER SORTER FUNCTION *USED**/
    exxit();                /*EXIT FUNCTION *USED**/
    }
    }
    else{
    printf("wrong password\n"); 
    exxit();               /*EXIT FUNCTION *USED**/
    }
    return 0; 
}
    

 int exper(char ask){            /*CUSTOMER SORTER FUNCTION*//*TWO TYPE OF SORTINGS: EXPERIENCED AND NON-EXPERIENCED*/
    int bmi;
    double bmi1;
    double w,h;
    if(ask=='N'|| ask=='n'){
        printf("\nNEW REGISTRATION in NON_EXPERIENCED\n.");         
        printf("LET'S PROCEED TO BMI CALCULATION.\n");
        printf("\nENTER YOUR HEIGHT IN METRE:");
        scanf("%lf",&h);
        printf("\nENTER YOUR WEIGHT:");
        scanf("%lf",&w); 
        bmi1= w/(h*2);                    /* BODY MASS INDEX CALCULATING FORMULAS*/
        printf("YOUR BMI(BODY MASS INDEX) IS :%lf\t\n",bmi1);
        BMI(bmi1);
    }
    else if(ask=='y'||ask=='Y'){
        printf("NEW REGISTRATION IN EXPERIENCED .\n");
        printf("INPUT YOUR BMI !:");
        scanf("%d",&bmi);
        BMI(bmi);
    }
    else{  printf("PLZZ ENTER 'Y' for YES OR 'N' for NO. INVALID INPUT !!!!");  }
}
int fat_reduction()                   /*FAT REDUCTION FUNCTION*/
{
      int day;
      printf("\nenter day:");
      scanf("%d",&day);                 /* DAY STANDS FOR WEEKDAY*/
      switch (day){
      case 1: printf("\nMONDAY:LEG DAY\n");
      break;
      case 2: printf("\nTUESDAY:CHEST DAY\n");
      break;
      case 3: printf("\nWEDNESDAY:BACK DAY\n");
      break;
      case 4: printf("\nTHURSDAY:BICEP DAY\n");
      break;
      case 5: printf("\nFRIDAY:PRESSUPS\n");
      break;
      case 6: printf("\nSATURDAY:THIGH DAY\n");
      break;
      case 7: printf("\nSUNDAY:REST\n");
      break;
      default: printf("\nINVALID INPUT\n !!"); 
      break;      
      }
      system("pause");         /*system command .. function = pauses the program and displayes "Press any KEY to continue"*/
      system("cls");           /*system command .. function = closes the current screen and displayes the next code in fresh window*/
}

int cardio()                    /*HIGH CARDIO FUNCTION*/
{
    int day;
      printf("\nenter day:");
      scanf("%d",&day);
      switch (day){
      case 1: printf("MONDAY:CYCLING, TREADMILL\n");
      break;
      case 2: printf("TUESDAY:CYCLING FAST,TREADMILL\n");
      break;
      case 3: printf("WEDNESDAY:TREADMILL,SKIPPING\n");
      break;
      case 4: printf("THURSDAY:TREADMILL,SKIPPING\n");
      break;
      case 5: printf("FRIDAY:CYCLING,TREADMILL,SKIPPING\n");
      break;
      case 6: printf("SATURDAY:CYCLING,TREADMILL,SKIPPING\n");
      break;
      case 7: printf("SUNDAY:REST\n");
      break;
      default: printf("INVALID INPUT\n !!"); 
      break;
      }
      system("pause");          /*system command .. function = pauses the program and displayes "Press any KEY to continue"*/
      system("cls");            /*system command .. function = closes the current screen and displayes the next code in fresh window*/
}

int weight_workout()
{
    int day;
      printf("\nenter day:");
      scanf("%d",&day);
      switch (day){            /*DAY STANDS FOR WEEKDAY*/
      case 1: printf("MONDAY:LEG DAY\n");
      break;
      case 2: printf("TUESDAY:CHEST DAY\n");
      break;
      case 3: printf("WEDNESDAY:REST\n");
      break;
      case 4: printf("THURSDAY:BICEP DAY\n");
      break;
      case 5: printf("FRIDAY:HIGH INTENSITY CARDIO\n");
      break;
      case 6: printf("SATURDAY: DAY\n");
      break;
      case 7: printf("SUNDAY:REST\n");
      break;
      default: printf("INVALID INPUT\n !!"); 
      break;
      }
      system("pause");      /*system command .. function = pauses the program and displayes "Press any to continue"*/
      system("cls");        /*system command .. function = closes the current screen and displayes the next code in fresh window*/
}
int diet_fr(){       /*DIET CHART FOR FAT REDUCTION FOR THE CUSTOMER*/
    printf("\nYOUR DIET ROUTINE FOR THE FAT REDUCTION EXERCISE WILL BE.\n");
    printf("\nBreakfast::\n\n");
    printf("\tMON\t\tTUE\t\tWED\t\tTHU\t\tFRI\t\tSAT\t\tSUN\n");
    
    printf("\tboiled_eggs\tpea_toast  \toats_muesli\tboiled_eggs\tfat-cutSHKE\t  cornflakes \tCheat\n\n");
    printf("\tmilk(toned)\t1-apple    \torange_juic\tmilk(toned)\t oats_milk \t1-pomegranate\tCheat\n\n");
    printf("\tdry_fruits \tfat-cutSHKE\tdry_fruits \t7-almonds  \tfat-cutSHKE\t   1-banana  \tCheat\n\n");
  
    
    printf("Lunch::\n\n");
    printf("\tdal_chapati\trice_khcdhi\trice_gr.dal\tdal_chapati\trice_khcdhi\t  1-bowl_oats \tomelette\n\n");
    printf("\tany_veget. \t1-beetroot \tbuttermilk \tany_veget. \t1-beetroot \t--------------\twhitebutter\n\n");
    printf("\tsome_salads\tsome_salads\tan_onion   \tsome_salads\tmix_veg_jui\t  some_salads \tany_ketchup\n\n");
    
    
    printf("Dinner::\n\n");
    printf("\trice_veget.\tbuttr_omltt\tcaffine_int\tboiled_eggs\tprotein.bar\tjapanse-salad\tCheat\n\n");
    printf("\tsome_salads\tstrawberr.s\tchapati_veg\tmilk(toned)\tchea_seeds \tfat-cutSHKE  \tCheat\n\n");
    printf("\twarm_milk  \talmnd_milk \tmash.potats\t7-almonds  \thon_lem.wat\t   1-banana  \tCheat\n\n");
    
}
    
int diet_c(){       /*DIET CHART FOR HIGH CARDIO FOR THE CUSTOMER*/
    printf("\nYOUR DIET ROUTINE FOR THE CARDIO EXERCISE WILL BE.\n");
    printf("\nBreakfast::\n\n");
    printf("\tMON\t\tTUE\t\tWED\t\tTHU\t\tFRI\t\tSAT\t\tSUN\n");
    
    printf("\tboiled_eggs\tpea_toast  \toats_muesli\tboiled_eggs\tfat-cutSHKE\t  cornflakes \tCheat\n\n");
    printf("\tmilk(toned)\t1-apple    \torange_juic\tmilk(toned)\t oats_milk \t1-pomegranate\tCheat\n\n");
    printf("\tdry_fruits \tfat-cutSHKE\tdry_fruits \t7-almonds  \tfat-cutSHKE\t   1-banana  \tCheat\n\n");
  
    
    printf("Lunch::\n\n");
    printf("\tdal_chapati\trice_khcdhi\trice_gr.dal\tdal_chapati\trice_khcdhi\t  1-bowl_oats \tomelette\n\n");
    printf("\tany_veget. \t1-beetroot \tbuttermilk \tany_veget. \t1-beetroot \t--------------\twhitebutter\n\n");
    printf("\tsome_salads\tsome_salads\tan_onion   \tsome_salads\tmix_veg_jui\t  some_salads \tany_ketchup\n\n");
    
    
    printf("Dinner::\n\n");
    printf("\tboiled_eggs\tpea_toast  \toats_muesli\tboiled_eggs\tfat-cutSHKE\t  cornflakes \tCheat\n\n");
    printf("\tmilk(toned)\t1-apple    \torange_juic\tmilk(toned)\t oats_milk \t1-pomegranate\tCheat\n\n");
    printf("\tdry_fruits \tfat-cutSHKE\tdry_fruits \t7-almonds  \tfat-cutSHKE\t   1-banana  \tCheat\n\n");
    

    
}
int diet_ww(){       /*DIET CHART FOR WEIGHT WORKOUT(GAINER) FOR THE CUSTOMER*/
    printf("\nYOUR DIET ROUTINE FOR THE WEIGHT GAINER EXERCISE WILL BE.\n");
    printf("\nBreakfast::\n\n");
    printf("\tMON\t\tTUE\t\tWED\t\tTHU\t\tFRI\t\tSAT\t\tSUN\n");
    
    printf("\tboiled_eggs\tpea_toast  \toats_muesli\tboiled_eggs\tfat-cutSHKE\t  cornflakes \tCheat\n\n");
    printf("\tmilk(toned)\t1-apple    \torange_juic\tmilk(toned)\t oats_milk \t1-pomegranate\tCheat\n\n");
    printf("\tdry_fruits \tfat-cutSHKE\tdry_fruits \t7-almonds  \tfat-cutSHKE\t   1-banana  \tCheat\n\n");
  
    
    printf("Lunch::\n\n");
    printf("\tdal_chapati\trice_khcdhi\trice_gr.dal\tdal_chapati\trice_khcdhi\t  1-bowl_oats \tomelette\n\n");
    printf("\tany_veget. \t1-beetroot \tbuttermilk \tany_veget. \t1-beetroot \t--------------\twhitebutter\n\n");
    printf("\tsome_salads\tsome_salads\tan_onion   \tsome_salads\tmix_veg_jui\t  some_salads \tany_ketchup\n\n");
    
    
    printf("Dinner::\n\n");
    printf("\tboiled_eggs\tpea_toast  \toats_muesli\tboiled_eggs\tfat-cutSHKE\t  cornflakes \tCheat\n\n");
    printf("\tmilk(toned)\t1-apple    \torange_juic\tmilk(toned)\t oats_milk \t1-pomegranate\tCheat\n\n");
    printf("\tdry_fruits \tfat-cutSHKE\tdry_fruits \t7-almonds  \tfat-cutSHKE\t   1-banana  \tCheat\n\n");
    

}


int BMI(int num)      /*DIET AND GYM_TYPE ALLOCATOR FUNCTION*/
{
    if(num>=30)
    {
        printf("\nYou need a fat reduction workout.");
        fat_reduction();
        diet_fr();
    }
    
    else if(num>=25 && num<30)
    {
        printf("\nFocus on cardio.");
        cardio();
        diet_c();
       
    }
    else if(num>=20 && num<25){        /* BMI FROM 20 TO 25 IS REGARDED AS PERFECT.*//*THE CUSTOMER NEEDS NO SPECIAL DIET OR TRAINING*/
        printf("you are in perfect shape.\n");
        printf("A special workout schedule for you.\n\n");
        printf("MONDAY:BICEPS\n\n");
        printf("TUESDAY:BACK\n\n");
        printf("WEDNESDAY:CHEST\n\n");
        printf("THURSDAY:TRICEPS\n\n");
        printf("FRIDAY:THIGHS\n\n");
        printf("SATURDAY:INTENSE CARDIO\n\n");
        printf("SUNDAY:REST\n\n");
        
    }
    else if(num<=20)
    {
       printf("\nThere will be WEIGHT GAINER TRAINING FOR YOU.");
        weight_workout();
        diet_ww();
        
    }
} 

int exxit(){     /*PROGRAM EXITING FUNCTION*/
    int op;
    printf("enter 0 to exit the program:");
    scanf("%d",&op);
    if(op==0){
        system("exit");     /*system command .. function = EXITS THE PROGRAM STRAIGHT AWAY*/
    }
    else{ 
    printf("enter only 0 to exit otherwise the program will undergo forceful stoppage:");  
    scanf("%d",&op);
    if(op==0){
        system("exit");     /*system command .. function = EXITS THE PROGRAM STRAIGHT AWAY*/
    }
    else{
        printf("EXECUTING FORCEFUL EXIT.");
        system("pause");   /*system command .. function = pauses the program and displayes "Press any KEY to continue"*/
        system("exit");    /*system command .. function = EXITS THE PROGRAM STRAIGHT AWAY*/
    }
    }
}
int disclaimer(){
    printf("\t\tD\tI\tS\tC\tL\tA\tI\tM\tE\tR\n");
    printf("\t\tUNLESS STATED OTHERWISE, THIS PROGRAM IS A PROPERTY OF THE GROUP MENTIONED BELOW.\n");
    printf("\t\tALL SOURCE CODE, TEXTS, COMMENTS AND THE FUNCTIONALITY OF THE CODE IS LICENSED TO US.\n");
    printf("\t\tPROTECTED BY COPYRIGHT AND TRADEMARK LAWS AND VARIOUS OTHER INTELLECTUAL PROPERTY RIGHTS.\n");
    printf("\t\tANY ACT OF REDUNDANCY OR DUPLICACY MAY LEAD TO SEVERE ACTION.\n");
    printf("\t\t\t..........!!!!!ALERT!!!!..........!!!!ALERT!!!!.........\n");
    printf("\n\t\t\t\tC\tR\tE\tD\tI\tT\tS\t\t\t\t\n");
    printf("\t\t\t\t\t\t...HARSH PANDEY...\n\t\t\t\t\t\t...PRATHAM BHARGAVA...\n\t\t\t\t\t\t...KRITI SINGH...\n\t\t\t\t\t\t...ANURAG PANDEY...\t\t\t\n");
    system("pause");   /*system command .. function = pauses the program and displayes "Press any KEY to continue"*/
    system("cls");     /*system command .. function = closes the current screen and displayes the next code in fresh window*/

}
