# shopping-cart

#include<stdlib.h>
#include<stdio.h>
#include<string.h>

struct Product
{
     int id;
     char name[20];
     int price;
     int qty;
};
struct Bill
{
      int pid;
      char pname[20];
      int pprice;
};
char mygetch();
int getID();

void manageProduct();
void purchaseProduct();
void generateBill();
void addProduct();
void displayAllPorduct();
struct Product findProduct(int d);
void updateProduct(int id,int qty);

char fproduct[]={"product.dat"};
char fbill[]={"bill.dat"};
int total=0;

int main()
{
      FILE *fp;
      int ch;
      system("clear"); //clrscr();

      while(1)
      { 
           system("clear");
           printf("==========================================\n\n");
           printf("\t\t Welcome Product Management System\n\n");
           printf("===========================================\n\n");
           printf("1. Manage Product\n\n");
           printf("2. Purchase Product\n\n");
           printf("3. Generate Bill\n\n");
           printf("================================================\n\n");
           printf("\nPlease enter your Choice:");
           scanf("%d",&ch);
           switch(ch)
           {
                case 1: manageProduct();
                       break;
                case 2: purchaseProduct();
                       break;
                case 3: generateBill();
                       break;
                case 0: exit(0);
                       
           }
           mygetch();
       }
      return 0;
}
