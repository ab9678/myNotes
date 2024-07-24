[[Index]] [[Stack in python]] 
## DSA
Date: 24-07-24
Teacher: Debabrat sir
Topic: #stacks 

---
### Here the target is to learn how to convert infix to prefix and postfix.

Lets define each of them first :--
	**Infix** : These are normal numbers where `<operand><opeartor><operand>`, A+B,etc.
		Here *BODMAS* rule is followed to determine operator precedence.
		precedence order:
			Brackets
			exponents
			division = multiplication [R to L] , whichever comes first gets the higher priority.
			addition = subtraction [L TO R]
	**prefix** : Here operator is placed before operand. `<operator><operand><operand>`
		eg :- A+B => + AB.
	**postfix** : Here operator is placed after operand. `<operand><operand><operator>`
		eg :- A+B => AB+
### How to CONVERT from normal/infix to postfix or prefix
##### Covert infix ---> postfix :--

*Algorithm :*
1. print operands as they arise
2. The first operator should be pushed to the stack
3. As new operators come into play, precedence rule is used. The new operator is compared to the top most operator of the stack. If the new_operator has lower precedence then the old_operator, the old/higher operator is popped out and printed at the end of the then printed operands. and the new operator sits at the top, **now, the comparison has to be done again and again until this operator is not the highest precedence operator**.
4. Remember : Low in High out *( LIHO )*
5. If `(` is encountered , it is directly pushed to the stack, and the operators are not compared with parenthesis 
6. when `)` is encountered, the operators in the stack, till the `(` are all popped out and these two `()` are deleted.
7. At the end of the expression, whatever is left pop out and print the new expression.

` ( A + B/C * ( D + C ) - F )` is when converted becomes `ABC/DC+*+F-`



