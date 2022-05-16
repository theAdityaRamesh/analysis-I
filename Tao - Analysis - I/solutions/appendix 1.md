# Appendix 1 : Logic
****

### Ex A.1.1
$$\neg(\textit{either X is true or Y is true})$$
$$\neg(\textit{X is true } \oplus\textit{ Y is true})$$
$$(X \odot Y)$$

where $\oplus$ is the XOR operator and $\odot$ is XNOR operator.

### Ex A.1.2

$$\neg(\textit{X is true} \iff \textit{Y is true})$$
$$\neg(X \implies Y \wedge Y \implies X)$$
$$(\neg(X \implies Y) \vee \neg(Y \implies X) )$$
$$(\neg(\neg X \vee Y) \vee \neg(\neg Y \vee X))$$
$$((X \wedge \neg Y) \vee (Y \wedge \neg X))$$
$$(\textit{either X or Y but not both})$$

### Ex A.1.3

It is given that $\textit{whenever X is true Y is true}$, Hence if $\textit{Y is true X must be true}$. Similarly we conclude that $\textit{if Y is false X must be false}$. Hence $\textit{X \& Y are logically equivalent}$

### Ex A.1.4

In the question the conditional statement and its contrapositive is given. However the contrapositive is equivalent to the original conditional statement. Hence we cannot conclude anything about the converse. Hence we can't say if the statements are logically equivalent.

### Ex A.1.5

Given that $X \iff Y $ and $Y \iff Z$. 
- If X is false Y becomes false and if Y is false Z becomes false. Hence Z is false whenever X is false.
- If X is true Y becomes true and if Y is true Z becomes true. Hence Z is true whenever X is true.

Hence X and Z are logically equivalent.

### Ex A.1.6

Yes.

