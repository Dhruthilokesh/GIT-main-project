#include<stdio.h>
#include<stdlib.h>
#define ss 3
int mstack[];
int ele;
int top= -1;
void push(int ele){
    if(top == ss-1){
        printf("stack is full");
        return ;
    }
    top++;
    mstack[top] = ele;
    printf("the element pushed is %d", mstack[top]);
}
  int pop (){
    if(top == -1){
        printf("the stack is empty");
    }
    int ele = mstack[top];
    top--;
    printf("the element popped is %d", mstack[top]);
  } 
  void size(){
    printf("the size of the stack is %d", top +1);
  }
  void display(){
    for (int i = 0 ; i<= top; i++){
        printf("%d", mstack[i]);
    }
  }
  void main (){
    int choice , ele;
    printf("the choices are 1for push and 2 for pop and 3 for size and 4 for display and 5 for exit");
    while(1){
        printf("Enter the choice");
        scanf("%d", &choice);
    switch(choice){
        case 1:
        printf("Enter the element to be pushed");
        scanf("%d", &ele);
        push(ele);
        break;
        case 2:
        pop();
        break;
        case 3:
        size();
        break;
        case 4 :
        display();
        break;
        case 5:
        exit(0);
        

    }
    }
  }