[[Index]]

## DSA in C
Date: 23-07-24
Teacher: Debabrat sir
Topic: #stacks

---
**Function of stacks**
1. `push()` this function allows user to update the stack in the top most address
2. `pop()` this function allows user to make the element in that address, which is the top most to be inaccessible by changing the top most address to the next one just below it, also we generally use pop to display the removed element or content
3. `peek()` this function just read the top most element, kind of peeking on the top most element
4. `display()` this prints the whole stack top to bottom


#### `push()`

```c
void push(){
    int x;
    printf("Enter data: ");
    scanf("%d",&x);

    if (ifFull_empty(stack[N]) == 1){  //here ifFull_empty() is a function created for checking when stackoverflow and stackunderflow is encountered
        printf("Stackoverflow");    // should use display() here before exit so that atleast the remaining stack which was entered can be accessed
        exit(0);
    }else{
        address++;
        stack[address]=x;
    }


}
```

#### `pop()`

```c
int pop(){

    if(ifFull_empty(stack[N])==2){
        printf("Stackunderflow");
        exit(0);
    }else{
        return stack[address];
        address--;
    }
}
```
Explanation:
	It is imp to check whether the stack is empty before proceeding.
	Now one that is sorted out the next thing is simply returning or printing the upper most element, given we had already pushed something before.
	Then the address is decremented to the next lower value so that the original one is no ore accessible.
	*We can simply do `adress++` that will make it accessible again right?*
	well yes, but reading a stack is only done from top to bottom not the other way around also if privacy & security is the main concern than we can also replace the original value with some garbage value.
	
	