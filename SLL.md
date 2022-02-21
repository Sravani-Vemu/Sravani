#include<stdio.h>
struct node{
	int data;
	struct node *next;
};
struct node *head;
void insert_at_beginning(int num){
	struct node *newnode;
	newnode = (struct node*)malloc(1*sizeof(struct node));
	newnode->data = num;
	newnode->next = head;
	head = newnode;	
}
void display(){
	struct node *ptr;
	while(ptr!=NULL){
		printf("%d-> ",ptr->data);
		ptr = ptr->next;
	}
	
}

int main(){
	int num;
	while(1){
	
		scanf("%d",&num);
		if(num==-1){
			break;
		}
		insert_at_beginning(num);
		display();
		printf("\n");
	}
}
