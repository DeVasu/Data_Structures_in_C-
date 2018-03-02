#include<iostream>
#include<cstdlib>

using namespace std;


struct node{
             int data;
             node *next;

             };
void printlist(node* a)
{
  while(a!=NULL)
  {
        cout<<a->data<<endl;
        a=a->next;
  }
  cout<<"this is the whole list\n";
}
void insertn(int dat, struct node **a)
{
    node* newp=(node*)malloc(sizeof(node));
    newp->data=dat;
    newp->next=*a;
    *a=newp;
}

void insertb(node *a,int data)
{
    node* newp=new node;
    newp->data=data;
    newp->next=NULL;
    if(a==NULL) a=newp;

    else{
        node *dum=new node;
        dum=a;
        while(dum->next!=NULL)
        {
            dum=dum->next;
        }
        dum->next=newp;
    }

}

void insertaf(node *a,int data)
{
    if(a==NULL) {cout<<"it can't be null";return;}
    node *n=new node;
    n->data=data;
    n->next=a->next;
    a->next=n;
}

void deleten(node **head,int key)
{
    node *temp=*head,*prev;
    if(temp!=NULL && temp->data==key)
    {
        *head=temp->next;
        free(temp);
        return;
    }
    while(temp!=NULL && temp->data!=key)
    {
        prev=temp;
        temp=temp->next;
    }
    if(temp==NULL) return;
    prev->next=temp->next;
    free(temp);
}


int main()
{
    struct node *head=NULL;
    struct node *second=NULL;
    struct node *third=NULL;
    
    head=(struct node*)malloc(sizeof(struct node));
    second=(struct node*)malloc(sizeof(struct node));
    third=(struct node*)malloc(sizeof(struct node));
    
    head->data=1;
    head->next=second;
    second->data=2;
    second->next=third;
    third->data=3;
    third->next=NULL;

    insertb(head,500);
    printlist(head);

    printlist(head);
    insertn(5,&head);
    printlist(head);
    insertn(6,&head);
    printlist(head);

    insertb(head,10);
    insertb(head,40);
    printlist(head);

    insertaf(third,487);
    printlist(head);

    deleten(&head,10);
    printlist(head);
    return 0;
}
