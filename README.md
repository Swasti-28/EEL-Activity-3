# EEL-Activity-3
#include <stdio.h>
void main() {
int CustomerID,membership_plan,AddYoga,AddDiet,AddTrainer,CustomerType, PhoneNumber ;
char name[50] ;
int amount=0;
printf("WELCOME TO FITNESS GYM AND WELLNESS CENTER\n");

printf("Enter Phone Number:\n");
scanf("%d", & PhoneNumber);
printf("Enter Customer ID:\n");
scanf("%d",& CustomerID); 
printf("Enter Customer name:\n");
scanf("%s",& name);
printf("Enter Customer Type: 1= Individual/ 2= Corporate:\n");
scanf("%d", & CustomerType);
printf("Select Membership Plan:\n 1= Monthly\n 2= Quarterly \n 3= Annual\n");
scanf("%d", & membership_plan);

printf("Add Yoga classes? 1=Yes/ 0=No:\n");
scanf("%d", & AddYoga);
printf("Add Personal Trainer? 1=Yes/ 0=No\n");
scanf("%d", & AddTrainer);
printf("Add Diet Plan? 1=Yes/ 0=No\n");
scanf("%d", & AddDiet);

if (membership_plan==1) amount= amount+1000 ;
if (membership_plan==2) amount= amount+ 2700;
if (membership_plan==3) amount= amount+10000;

if(AddYoga==1 || AddTrainer==1 || AddDiet==1 )amount=amount+750;
if (CustomerType==2) {
    amount= amount*0.9;
}
printf("\n=========== FITNESS MEMBERSHIP BILL ===========\n");
printf("CustomerID       : %d\n", CustomerID);
printf("Customer Name    : %s\n", name);
printf("Customer Type    : %d\n", CustomerType);
printf("Membership Plan  : ");

if (membership_plan==1) printf("Monthly\n");
else if (membership_plan==2) printf("Quarterly\n");
else if (membership_plan==3) printf("Annual\n");
printf("Add-ons:\n");
if (AddYoga == 1) printf("Yoga Classes        : ₹750\n");
if (AddTrainer == 1) printf("Personal Trainer    : ₹750\n");
if (AddDiet == 1) printf("Diet Plan           : ₹750\n");
if (AddYoga == 0 && AddTrainer == 0 && AddDiet == 0) printf("  No Add-ons\n");
printf("--------------------------------------------\n");
printf("Total amount Payable: ₹ %d\n", amount);
printf("Keep Going, Stay Fit and Healthy!\n");
printf("==========================================\n");

} 
