# College-Management-System
A console-based Student &amp; Faculty Management System developed in C with login authentication, student details, internal marks, semester results, SGPA/CGPA calculation, library, placements, and notifications.

#include <stdio.h>
#include<stdlib.h>
#include<string.h>
struct id
{
int no;
char name[20];
char dept[20];
char username[20];
char password[20];
};
struct rollno
{
char username[20];
char password[20];
char htno[20];
char name[20];
char branch[20];
int int_marks1;
int int_marks2;
float sgpa1;
float sgpa2;
float sgpa3;
float sgpa4;
float sgpa5;
float sgpa6;
float sgpa7;
float sgpa8;
};
struct year
{
char name[20];
int package;
};
int main()
{
int choice,internal;
char username[20],password[20];
char fac_username[20],fac_password[20];
float copy,total;
int id,i,hat,sch,sem;
struct id no[5]={
{7701,"faculty1","ece","faculty1@123","faculty1@123"},{7702,"faculty2","ece","faculty2@123","faculty2@123"},{7703,"faculty3","ece","faculty3@123","faculty3@123"},{7704,"faculty4","ece","faculty4@123","faculty4@123"},
{7705,"faculty5","ece","faculty5@123","faculty5@123"}};
struct rollno rool[5]={
{"25WJ1A7701","student@123","25WJ1A7701","student","ECE",37,38,8.05,8.8},
{"25WJ1A7702","student1@123","25WJ1A7702","student1","VLSI",25,30,8.05,8.90},
{"25WJ1A7703","student2@123","25WJ1A7703","student2","VLSI",26,35,3.45,6},
{"25WJ1A7704","student3@123","25WJ1A7704","student3","VLSI",30,35,6.6,4},
{"25WJ1A7705","student4@123","25WJ1A7705","student4","VLSI",35,40,5.7,6.67}
};
struct year place[5]=
{{"rishik",16},{"ravi",7},{"koushik",18},{"gitesh",6},{"Sujith",20}};
printf("-----------------------------------------\n");
printf("|     ---GURU NANAK INSTITUTION---       |\n");
printf("|           TECHNICAL CAMPUS             |\n");
printf("|                                        |\n");
printf("|                                        |\n");
printf("|                                        |\n");
printf("|      Enter 1 for faculty login         |\n");
printf("|      Enter 2 for student login         |\n");
printf("-----------------------------------------\n");
scanf("%d",&choice);
if(choice==1)
{
printf("USERNAME:\n");
printf("PASSWORD:\n");
scanf("%s\n%s",&fac_username,fac_password);
for(i=0;i<5;i++)
{
if(strcmp(fac_username,no[i].username)==0&&strcmp(fac_password,no[i].password)==0)
{
printf("---WELCOME---\n\nNAME:%s\n\nDEPARTMENT:%s\n\n",no[i].name,no[i].dept);
printf("--- FACULTY DASHBOARD ---\n1. STUDENT DETAILS\n2.INTERNAL MARKS\n3. NOTIFICATION \n4. LOGOUT\n");
printf("ENTER Your Choice:\n");
scanf("%d",&sch);}}
switch(sch)
{
case 1:
printf("---STUDENT DETAILS---\n");
for(i=0;i<5;i++)
{
printf("\nNAME:%s\nROLLNO:%s\nBRANCH:%s\n",rool[i].name,rool[i].htno,rool[i].branch);
}
case 2:
printf("Enter the internal details:1 or 2\n");
scanf("%d",&internal);
if(internal==1)
{
printf("---Internal marks 1---\n");
for(i=0;i<5;i++)
{
printf("\nNAME:%s\nBRANCH:%s\nMARKS:%d\n",rool[i].name,rool[i].branch,rool[i].int_marks1);
}}
else if(internal==2)
{
printf("---INTERNAL MARKS 2---\n");
for(i=0;i<5;i++)
{
printf("\nNAME:%s\nBRANCH:%s\nMARKS=%d\n",rool[i].name,rool[i].branch,rool[i].int_marks2);
}}
case 3:
printf("---NOTIFICATION---\n");
printf("Sardar Tavinder Singh Kohli Memorial \n--NATIONAL SPORTS MEET--\n PART OF GNITC SILVER JUBILEE CELEBRATIONS\n 3 - 5th September 2026");

case 4:
exit(0);
default:
printf("--WRONG CREDENTIALS!!\n");
}}
else if(choice==2)
{
printf("USERNAME:\n");
printf("PASSWORD:\n");
scanf("%s\n%s",&username,password);
for(i=0;i<5;i++)
{
if(strcmp(username,rool[i].username)==0&&strcmp(password,rool[i].password)==0)
{
printf("---WELCOME---\nRollno: %s\nNAME: %s\nBRANCH: %s\n",rool[i].htno,rool[i].name,rool[i].branch);
printf("\n\n---DASHBOARD---\n1.ACADEMICS:\n2.EXAMINATION CELL:\n3.LIBRARY:\n4.PLACEMENTS:\n5.NOTIFICATION:\n6.Exit\n");
printf("Enter your choice:\n");
scanf("%d",&sch);}}
switch(sch)
{
 case 1:
 printf("LIST OF HOLIDAYS\n");
 printf("");
 break;
 case 2:
 printf("EXAMINATION CELL\n");
 printf("Enter your SEM details\n In the format of 1-1 is '1'and 1-2 is '2'\n");
 scanf("%d",&sem);
 if(sem==1)
 {
 for(i=0;i<5;i++)
 {
 if(strcmp(username,rool[i].username)==0)
 {
 copy=rool[i].sgpa1;
 printf("ROLLNO:%s\nNAME:%s\nBRANCH:%s\n\n---SEM 1 RESULTS---\n\nSGPA:%2.f\n",rool[i].htno,rool[i].name,rool[i].branch,rool[i].sgpa1);
 if(copy>5.00)
 printf("PASSED\n");
 else
 printf("FAILED\n");}}}
 else if(sem==2)
 {
 for(i=0;i<5;i++)
 {
 if(strcmp(username,rool[i].username)==0)
 {
 copy=rool[i].sgpa2;
 printf("ROLLNO:%s\nNAME:%s\nBRANCH:%s\n\n---SEM 2 RESULTS---\n\nSGPA:%2.f\n",rool[i].htno,rool[i].name,rool[i].branch,rool[i].sgpa2);
 total=(rool[i].sgpa1+rool[i].sgpa2)/2;
 printf("CGPA:%2.f\n",total);
 if(total>5)
 printf("PASSED\n");
 else
 printf("FAILED\n");
 }}}
 else
 printf("RESULTS NOT AVAILABLE\n");
 break;
case 3:
printf("GNI INSTITUTIONS HAS A CENTRAL LIBRARY\n");
printf("ENRICH YOUR KNOWLEDGE WITH BOOKS\n");
break;
case 4:
printf("PLACEMENTS!!!!\n");
printf("LIST:\n");
printf("NAME\t\tPACKAGE\n");
for(i=0;i<5;i++)
{
printf("%s\t\t%dLPA\n\n",place[i].name,place[i].package);
}
break;
case 5:
printf("NOTIFICATION\n");
printf("Sardar Tavinder Singh Kohli Memorial \n--NATIONAL SPORTS MEET--\n PART OF GNITC SILVER JUBILEE CELEBRATIONS\n 3 - 5th September 2026");
break;
case 6:
exit(0);
default:
printf("WRONG CREDENTIALS!!!");
}
}
return 0;
}
