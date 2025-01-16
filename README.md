# ROCK-PAPER-SCISSOR
#include<stdio.h>
#include<conio.h>
#include<time.h>
#include<stdlib.h>
void main(){
int num,i,n,user=0,comp=0;
clrscr();
srand(time(NULL));
printf("ROCK-PAPER-SCISSOR\n\n");
printf("ENTER:\n1 FOR ROCK\n2 FOR PAPER\n3 FOR SCISSOR");
for(i=0;i<3;i++){
printf("\nENTER 1,2 OR 3:");
scanf("%d",&n);
if(n==1)      printf("YOUR INPUT-ROCK\n");
else if(n==2) printf("YOUR INPUT-PAPER\n");
else if(n==3) printf("YOUR INPUT-SCISSOR\n");
num=rand()%3;
if(num==1)      printf("COMPUTER-ROCK\n");
else if(num==2) printf("COMPUTER-PAPER\n");
else if(num==3) printf("COMPUTER-SCISSOR\n");

if(n==1 && num==3){
user++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==3 && num==1){
comp++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==1 && num==1){
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==2 && num==1){
user++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==1 && num==2){
comp++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}

else if(n==2 && num==2){
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==3 && num==3){
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==3 && num==2){
user++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
else if(n==2 && num==3){
comp++;
printf("YOUR SCORE=%d\n",user);
printf("COMPUTER SCORE=%d\n",comp);
}
}
printf("\n\n     FINAL SCORE\n");
printf("%-10s  %-10s\n", "YOUR SCORE", "COMPUTER SCORE");
printf("-----------------------------\n");
printf("%5d %15d\n",user,comp);

if(user>comp)
printf("      YOU WON");
else if(comp>user)
printf("      COMPUTER WON");
else
printf("       DRAW");
getch();
}
