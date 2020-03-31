# saicharan1125
#include<iostream>
using namespace std;
class LovelySweets
{
public:
int semaphore;
int n;
int left;
void Entershop(int left)
{
cout<<"\n\n			 no of people enter for shoping is= "<<left;
}
void ShopForWhile()
{
cout<<"\n\n			people are shoping";
cout<<"				need to wait";
cout<<"				need to wait";
cout<<"				need to wait";
cout<<"				need to wait";
}
void LeaveShop(int left)
{
cout<<"\n\n 			done with shoping";
cout<<"\n\n			people left the shop is= "<<left;
semaphore=0;
n=n-left;
}
};

int	main()
{

cout<<"											WELCOME TO";
cout<<"										**** LOVELY SWEETS ***";
LovelySweets obj;
while(true)
{

cout<<"\n\n 					enter the no of  people waiting outside";
cin>>obj.n;
while(obj.n>0)
{
obj.semaphore=0;
cout<<"\n\n 					people will enter one after one so be follow the shop rules \n Thank your coming ";

if(obj.semaphore==0)
{
cout<<"\n\n					shopkeeper checking any people are shoping inside";
cout<<"\n\n					no one is there please allow people inside";
cout<<"\n\n    according to shop rules two people can enter the shop they must be one left-hand person and one right-hand peson";
cout<<"\n\n					people waiting outside= "<<obj.n;
cout<<"\n\n					please enter no of people to be allow inside";
cin>>obj.left;

cout<<"\n\n              				sendind inside no of people are= "<<obj.left;

obj.Entershop(obj.left);
obj.ShopForWhile();
obj.LeaveShop(obj.left);
}
}
}
}
