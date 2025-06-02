# Rock-paper-scissors
Play the infamous "Rock, paper, scissors" game by yourself with a computer!!
#include<iostream>
#include<cstdlib>
 
using namespace std;
 
void inputMenu(int &user)
{
cout<<"Menu: \n1. Rock. \n2. Paper. \n3. Scissors."<<endl<<endl;
cout<<"Rules: \n1. Paper wraps rock. \n2. Rock smashes scissors. \n3. Scissor cuts paper."<<endl<<endl;
cout<<"Enter your choice:";
cin>>user;
 
}
 
void gamePlay(int &computer)
{
computer=rand()%3+1;
 
}
 
void winner(int &computer, int &user)
{
if(computer==1 && user==2)
{
cout<<"Computer picked Rock. \nYou picked Paper. \nPaper wraps Rock. \nYOU WON smile"<<endl;
}
if(computer==1 && user==3)
{
cout<<"Computer picked Rock. \nYou picked Scissors. \nRock smashes Scissors. \nYOU LOST sad"<<endl;
}
if(computer==2 && user==3)
{
cout<<"Computer picked Paper. \nYou picked Scissors. \nScissor cuts Paper. \nYOU WON smile"<<endl;
}
if(computer==2 && user==1)
{
cout<<"Computer picked Paper. \nYou picked Rock. \nPaper wraps Rock. \nYOU LOST sad"<<endl;
}
if(computer==3 && user==1)
{
cout<<"Computer picked Scissors. \nYou picked Rock. \nRock smashes Scissors. \nYOU WON smile"<<endl;
}
if(computer==3 && user==2)
{
cout<<"Computer picked Scissors. \nYou picked Paper. \nPaper cuts Scissors. \nYOU LOST sad"<<endl;
}
if(computer == user)
{
cout<<"DRAW."<<endl;
}
 
}
 
int main()
{
system ("color fc");
cout<<"\t\t\t ROCK PAPERS SCISSORS"<<endl<<endl;
int computer;
int user;

char again;
do
{
    inputMenu(user); 
    gamePlay(computer);
    winner(computer, user);
 
    cout<<endl<<"Do you want to continue playing? (Y/N) : ";
    cin>>again;
    cout<<endl;
 
}while(again=='y' || again=='Y');
 
return 0;
}
