
#include <iostream>
#include <cstring>

using namespace std;

void printBook(struct Books *book);
void createnode(int value);

 struct Books
  {
      char title[50];
      char author[50];
      char subject[100];
      int book_id;
      } ;




int main()
{
    cout << "Hello world!" << endl;


 struct Books Book1;
 struct Books Book2;

strcpy(Book1.title , "Learn C++ Programming");
 strcpy(Book1.author, "Jonte' Fears");
 strcpy(Book1.subject, "C++ Programming");

 Book1.book_id =6495407;

 strcpy(Book2.title, "Rap Science");
 strcpy(Book2.author, "Jonte' Fears");
 strcpy(Book2.subject, "Music");
 Book2.book_id = 6495700;

 cout<<"Book 1 Title : "<<Book1.title<<endl;
cout<<"Book 1 Author : "<<Book1.author<<endl;
cout<<"Book 1 Subject : "<<Book1.subject<<endl;
cout<<"Book 1 Id : "<<Book1.book_id<<endl;

cout<<"Book 2 Title : "<<Book2.title<<endl;
cout<<"Book 2 Author : "<<Book2.author<<endl;
cout<<"Book 2 Subject : "<<Book2.subject<<endl;
cout<<"Book 2 Id : "<<Book2.book_id<<endl;

//*or//

printBook(&Book1);

printBook(&Book2);


//*or//

typedef struct
{ char titles[50];
char authors[50];
char subjects[100];
int book_id;
} Books;


Books BookOne, BookTwo;


typedef long int *pint32;
pint32 x, y, z;


//*linked list//

struct node{
int data;
node *next;

};

class list{
private:
    node *head, *tail;

public:
    list(){
    head=NULL;
    tail=NULL;
    }




void createnode(int value){
    node *temp=new node;
temp->data=value;
temp->next=NULL;
if (head=NULL){
    head=temp;
    tail=temp;
    }
else {tail->next=temp;
tail=temp;
}
};

void display()
{node *temp=new node;
temp=head;
while(temp!=NULL)
{cout<<temp->data<<"\t";
cout<<temp->next;
}
};

void insert(int value){
node *temp=new node;
temp->data=value;
temp->next=head;
head=temp;
}
void insert_position(int pos, int value){
node *pre=new node;
node *cur=new node;
node *temp=new node;
cur=head;
for(int i=1;i<pos;i++){
    pre=cur;
    cur=cur->next;
}
temp->data=value;
pre->next=temp;
temp->next=cur;
}

void delete_first()
{ node *temp=new node;
temp=head;
head=head->next;
    delete temp;
}

void delete_last()
{node *current=new node;
node *previous=new node;
    current=head;
    while(current->next!=NULL)
    {previous=current;
    current=current->next;
        }
        tail=previous;
        previous->next=NULL;
        delete current;
        }

void delete_position(int pos)
{node *current=new node;
node *previous=new node;
for (int i=1;i<pos;i++)
{previous=current;
current=current->next;
    previous->next=current->next;
    delete current;
}



}














};























return 0;
};



