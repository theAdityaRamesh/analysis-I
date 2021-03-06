<head>
       ...
       <script type="text/x-mathjax-config"> MathJax.Hub.Config({ TeX: { equationNumbers: { autoNumber: "all" } } }); </script>
       <script type="text/x-mathjax-config">
         MathJax.Hub.Config({
           tex2jax: {
             inlineMath: [ ['$','$'], ["\\(","\\)"] ],
             processEscapes: true
           }
         });
       </script>
       <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
</head>

# Chapter 2 : Natural Numbers
***
### Ex 2.2.1 :

- To prove that : $(a+b)+c = a + (b+c)$.
- To do so we will induct on $a$ keeping $b$ & $c$ fixed.
- **Base Case** : $a=0$.
  - (0+b)+c = 0+(b+c)
  - by definition of addition $0 + m := m$ hence,
  - $b +c = b+c$ so the base case is true
- **Inductive Step** : let $(a+b)+c = a + (b+c)$ be true then we will show the same for $a++$.
  - $((a\text{++})+b)+c = (a\text{++})+(b+c)$
  - By definition of addition $(n\text{++})+m = (n+m)\text{++}$ hence,
  - $((a+b)+c)\text{++} = (a+(b+c))\text{++}$.
  - By axiom 2.4 we conclude that $(a+b)+c = a+(b+c)$.
  - Since this is already true due to the inductive hypothesis the induction is closed.


***

### Ex 2.2.2 :

- To prove $P(a) : \forall a (a \gt 0)(\exists b \in \mathbb{N} : b\text{++ } = a ) \wedge(c\in \mathbb{N} : c\text{++ } = a \implies b = c)$
- We need to demonstrate the existence and uniqueness of $b$ for the conjunction to be true.
- Using Axiom 2.5 we can prove this property for all natural numbers using induction.
  - **Existence** : we will induct on $a$ to prove existence. 
    - **Base Case** : $a = 0$ is vacuously true as $a$ is given to be a positive number in the question statement.
    - **Inductive Step** : $a \in \mathbb{N}-\{0\}$, let $P(a)$ be true, then we need to show $P(a\text{++})$ is true as well. 
    - Let there be some $c \in \mathbb{N}$ so that $c\text{++ } = a\text{++}$.
    - Using Axiom 2.4 and $P(a)$ we can conclude $c = a = b\text{++}$.
    - Hence for $c = b\text{++}$ we get $(b\text{++})\text{++} = a\text{++}$.
    - Hence the induction is closed and the existence is demonstrated.
  - **Uniqueness** : Let there be another $c \in \mathbb{N} : c\text{++} = a$.
  - By axiom of substitution and axiom 2.4 we can say $c\text{++} = b\text{++}$ which means $b=c$.
  - Hence uniqueness is also demonstrated.
- Hence the conjunction is true.
  
***
### Ex 2.2.3

- **Proof (a) :** To prove $\textit{Order is reflexive} : a \geq a$.
  -  ie : $\forall a \in \mathbb{N} \text{ } a \geq a$.
  -  $a \geq a$ means $a = a + m$ for some $m \in \mathbb{N}$.
  -  Since $a = a$ if we choose $m = 0$ then $\forall (a \in \mathbb{N}) a \geq a $.

- **Proof (b) :** To prove $\textit{Order is transitive } a \geq b \wedge b \geq c \implies a \geq c$.
  - $a \geq b$ means $a = b + m$.
  - $b \geq c$ means $b = c + n$. for some $m,n \in \mathbb{N}$.
  - Using axiom of substitution we can say $a = c + n + m$
  -  **Lemma :** $P(n) : \textit{Sum of 2 natural numbers is also a natural number.}$
     -  Proof : let $n,m \in \mathbb{N}$. and let $n+m \in \mathbb{N}$.
        -  **Base case** $n = 0$ we know by definition of addition $0+m = m$ and since $m \in \mathbb{N}$ the base case is true.
        -  **Inductive Step** Let $n+m \in \mathbb{N}$ the for $n\text{++}$, by definition of addition $n\text{++ } + m = (n+m)\text{++}$. By axiom 2.2 and $P(n)$ we conclude that $(n+m)\text{++} \in \mathbb{N}$. Hence the induction is closed.
  -  Using the lemma we can say $(n+m) \in \mathbb{N}$ so $a \geq c$ by definition.
  -  Hence proved.
-  **Proof (c) :** To prove $\textit{Order is antisymmetric } a\geq b \wedge b \geq a \implies a = b$.
   -  $a \geq b$ means $a = b + n$
   -  $b \geq a$ means $b = a + m$ for some $m,n \in \mathbb{N}$.
   -  Using axiom of substitution $a = a + m + n$
   -  Using cancellation $m + n = 0$.
   -  Using corollary 2.2.9 $m = 0 \wedge n = 0$.
   -  Hence $a = b$
- **Proof (d) :** To prove $\textit{Addition preserves order } a\geq b \iff a+c\geq b+c$
  - To prove this biconditional we need to show that $(a+c \geq b+c \implies a \geq b) \wedge (a \geq b \implies a + c \geq b + c)$
  - $a+c \geq b+c$ means $a + c = b + c + m$ for some $m \in \mathbb{N}$.
  - Using cancellation law $a = b + m$ which means $a \geq b$.
  - Hence proved that $(a+c \geq b+c \implies a \geq b)$.
  - $a \geq b$ means that $a = b + n$ for some $n\in \mathbb{N}$.
  - **Lemma :** If $a = b$ then $a + c = b + c$.
    - Proof by inducting on $a$.
      - **Base Case** $a=0$ : since $a=b \wedge a=0$  , $c+0=c+0$ 
      - by definition of addition and axiom of substitution we can get $c = c$. Hence base case is true.
      - **Inductive Step** : assume $a+c = b +c$ then for $a\text{++}$ we can say $(a\text{++})+c = (b\text{++})+c$, by definition of addition we get $(a+c)\text{++} = (b+c)\text{++}$ and by axiom 2.4 we get $a+c = b+c$ which is true because of the induction hypothesis. 
      - Hence the induction is closed.
  - By using the lemma we can say since $a = b +n$ $a+c = b + n + c$ for some $c \in \mathbb{N}$ which means $a+c \geq b+c$.
  - Hence the conjunction is true. Hence Proved.
- **Proof (e) :** To prove that $a \lt b \iff a\text{++ } \leq b$
  - To prove this biconditional we will prove the conjunction $( a\lt b \implies a\text{++} \leq b)\wedge(a\text{++ } \leq b \implies a \lt b)$.
  - $a \lt b$ means that $a \leq b \wedge a \neq b$. $a \leq b$ means that $b = a + m$ for some $m \in \mathbb{N}$. Using lemma 2.2.10 we know $\exists n : n\text{++ } = m$.
  - Using axiom of substitution we can say $b = a + n\text{++}$. Further using definition of addition we can say $b = (a+n)\text{++}$. Which is nothing but $b = a\text{++ } + n$. Which means $a\text{++} \leq b$.
  - Hence we have shown $a \lt b \implies a\text{++} \leq b$.
  - Now $a\text{++} \leq b$ means $a\text{++ } + m = b$ for some $m \in \mathbb{N}$. Which can be written as $(a+m)\text{++} = b$, which is $a + m\text{++ } = b$.
  - This means that $a\leq b$. Now to prove that $a \neq b$. 
  - If $a=b$ then it means that $m\text{++} = 0$, this is however a contradiction since by axiom 2.3 we know that $0$ is not the sucessor of any natural number. Hence it is proved.
  - Hence the conjunction is true.
- **Proof (f) :** To prove that $a\lt b \iff b = a + d$ where $d \in \mathbb{N}-\{0\}$.
  - To prove this biconditional we will prove the conjunction $(a\lt b \implies b = a + d)\wedge(b = a + d \implies a\lt b)$
  - $a\lt b$ means that $a\leq b \wedge a \neq b$. If $a \leq b$ it means $a + m = b$ for some $m \in \mathbb{N}$, hence if we choose $m := 0$ then $a+0=b$ which by definition of addition will mean $a=b$ this is however not possible since $a\neq b$. So $m \in \mathbb{N}-\{0\}$. Hence proved that $b = a +d$ where $d$ is positive.
  - If $b = a + d$ for positive $d$ then we can say it means $a\leq b$ as $d \in \mathbb{N} -\{0\}$ but $a \neq b$ since $d \neq 0$ hence this means $a\leq b \wedge a \neq b$ which is nothing but $a\lt b$.
  
***

### Ex 2.2.4 :

- **Proof St 1 :** $\forall b \in \mathbb{N} \implies b \geq 0$.
  - $b\geq 0$ means that $b = 0 + m$ for some natural number $m \in \mathbb{N}$.
  - By definition of addition we know that $0+m=m$ hence, $b=m$.
  - If we choose $m := b$ then the statement is true $\forall b \in \mathbb{N}$.
- **Proof St 2 :** $a\gt b \implies a\text{++} \gt b$.
  - $a\gt b$ means $a\geq b \wedge a \neq b$. since $a\geq b$ we can say $a =b + m $ for some $m \in \mathbb{N}$. Using lemma from Ex 2.2.3 proof(d) we can write this as $a+1=b+1+m$. 
  - Using definition of increment operator we can write this as $a\text{++} = b + m\text{++}$. Which means $a\text{++} \geq b$  as by axiom 2.2 $m\text{++} \in \mathbb{N}$. Now if $a\text{++} = b$ then $m\text{++} = 0$. 
  - This is not possible by axiom 2.3. Hence proved.
- **Proof St 3 :** $a=b \implies a\text{++} \gt b$.
  - Using lemma from Ex 2.2.3 proof(d) we can write $a + 1 = b+1$. Which is nothing but $a\text{++}=b+1$. Since $1\in \mathbb{N}$ this means that $a\text{++}\geq b$. 
  - If $a\text{++} = b$ then it means that $1=0$, this is not possible hence $a\text{++} \neq b$. 

***

### Ex 2.2.5

- Let $Q(n) := \forall m_0\leq m \lt n , P(m)$
- for $n=0,Q(0) :=  \forall m_0\leq m \lt 0 , P(m)$ is vacuously true since $m < 0 \wedge m \geq m_0$ can't be true.
- Let $Q(n)$ be true then,  $P(n\text{++})$ is true because of the property of $P(m)$. Hence $P(m\text{++})\wedge Q(n)$ gives $Q(n\text{++})$. Hence the induction is closed.
- Using axiom 2.5 we can say $Q(n)$ holds $\forall n\geq m_0 \in \mathbb{N}$, hence $P(m)$ is true $\forall n \geq m_0$.
***

### Ex 2.2.6

- **Proof** 
  - To prove that $P(n) \implies (Q(n) := \forall m\leq n, P(m))$.
  - Inducting on $n$;  first for $n=0$ we get, $P(0) \implies Q(0)$. Here $Q(0) := \forall m\leq 0, P(0)$. $m\leq0$ means $m+a=0$ for some $a \in \mathbb{N}$. Using corollary 2.2.9 we get $m=0\wedge a=0$. Hence This statement is equivalent to $P(0) \implies P(0)$, which is a tautology.
  - For the next step assume that $P(n) \implies Q(n)$ is true and $P(n\text{++})$ will be assumed to be true since we have to prove $P(\text{n++})\implies Q(\text{n++})$.
  - $P(\text{n++})\implies P(\text{n})$ and $P(n) \implies Q(n)$ so $P(n\text{++}) \implies Q(n)$. [Syllogism].
  - Now $(P(\text{n++})\implies Q(n) )\wedge P(\text{n++})$ will give $P(\text{n++})\implies Q(\text{n++})$
***

### Ex 2.3.1 :

- **Proof** 
  - To prove that $\forall m,n \in \mathbb{N}, n\times m = m \times n$. 
  - We shall induct on $n$ keeping $m$ fixed. Before that however we need to prove that $m\times 0 = 0$ since the definition only allows for $0\times m = 0$.
  - **Lemma :** $m\times 0 = 0$
    - We will induct on $m$ to prove the lemma
    - **Base Case** $m = 0$, $0\times 0 = 0$ by definition 2.3.1 of multiplication. Hence the base case is true.
    - **Inductive Step** Suppose that $m\times 0 = 0$ then we will prove the same for $m\text{++}$. $m\text{++ }\times 0$ by definition 2.3.1 is equal to $(m\times0) + 0$. Since by the inductive hypothesis $m\times0= 0$ we can simplify this to $0+0 = 0$. Hence the induction is closed.
  - **Base Case** $n=0$.
    - $0\times m = 0$
    - $m\times 0 = 0$  using definition 2.3.1 and the above stated lemma.
  - **Inductive Step** Suppose that inductively $n\times m = m \times n$ is true. We shall now prove the same for $n\text{++ }$. $n\text{++ } \times m = m \times n\text{++}$. 
    - $n\text{++ } \times m = (n\times m) + m$.
    - $m \times n\text{++ } = m \times (n+1)$
    - Note :  The distributive law of multiplication uses commutativity in its proof however that is to avoid doing the induction twice for $a(b+c)$ and $(b+c)a$. Hence i think it would not be a case of circular reasoning to use distributive property in proving commutativity.
    - Using distributive property we can say $m\times(n+1) = m\times n + m$.
    - Using the induction hypothesis this is nothing but $n\times m + m$.
    - Hence $LHS = RHS$ and the induction is closed.

***

### Ex 2.3.2 :
- To prove that $\forall n,m \in \mathbb{N}, n\times m = 0 \iff n = 0 \vee m = 0$
- To prove that $\forall n,m \in \mathbb{N}-\{0\} \implies n\times m \in \mathbb{N}-\{0\}$
  - We will induct on $n$ to prove the 2nd statement first. The **base case** is vacuously true since $n=0$ means that $n$ is not positive which is false.
  - Suppose that $n\times m$ is positive then we shall show the same for $n\text{++ }$. $n\text{++}\times m = (n\times m)+m$, we know that sum of two positive numbers is positive. (proposition 2.2.8). Hence the induction is closed.
- To prove the biconditional $\forall n,m \in \mathbb{N}, n\times m = 0 \iff n = 0 \vee m = 0$ we will prove the conjunction $\forall n, m \in \mathbb{N}$ $(n\times m = 0 \implies n = 0 \vee m =0 ) \wedge( n = 0 \vee m = 0 \implies n\times m = 0)$
- If the $n = 0 \vee m = 0$ is true then $(n = 0 \wedge m \neq 0) \vee (n \neq 0 \wedge m = 0) \vee (n = 0 \wedge m =0)$.
- Case 1 : for $(n = 0 \wedge m \neq 0)$ $0 \times m = 0$ by definition.
- Case 2 : for $(n \neq 0 \wedge m = 0)$ $n \times 0 = 0$ using the lemma in proof of EX 2.3.1.
- Case 3 : for $(n = 0 \wedge m = 0)$ $0\times0 = 0$ by definition 
- Hence $( n = 0 \vee m = 0 \implies n\times m = 0)$ is true.
- The contrapositive of $n\times m = 0 \implies n = 0 \vee m =0$ is that $n \neq 0 \wedge m \neq 0 \implies n \times m \neq 0$. Which is nothing but the product of 2 positive numbers is always positive.
- Hence the conjunction is true.

***

### Ex 2.3.3 :

- To prove that $\forall a,b,c \in \mathbb{N},\text{ } (a\times b)\times c = a \times ( b \times c)$. To do so we will fix $b,c$ and induct on $a$.
- **Base Case** $a = 0$ will yield $(0\times b)\times c = 0 \times (b\times c).$ Here by definition $(0\times b)\times c = 0$. Similarly before we show that $0\times(b\times c) = 0$ we need to show that product of 2 natural numbers is another natural number.
  - **Lemma** $\forall n,m\in \mathbb{N}, \text{ }n\times m \in \mathbb{N}$. 
    - **Base Case** Fix $n=0$, then $0\times m = 0$ and since $ 0 \in \mathbb{N}$ the base case is true.
    - **Inductive Step** Suppose that $n\times m \in \mathbb{N}$, Then we will show the same for $n\text{++. }$ $n\text{++ }\times m = (n\times m) + m$ by definition and since $n \times m \in \mathbb{N}$ and sum of 2 natural numbers is also a natural numbers the induction is closed.(using lemma 2.2.3 in proof(b)).
  - Now using this lemma we can say that the base case is true.
- **Inductive Step** Suppose that $(a\times b)\times c = a \times (b \times c)$. Then we will prove the same for $a\text{++ . }$ $(a\text{++ }\times b)\times c = ((a\times b) + b)\times c$ by definition. Further this is equal to $(a\times b) \times c + b \times c$.
- $a\text{++ } \times (b\times c) = (a\times(b\times c))+(b\times c)$. Due to the inductive hypothesis we know $(a\times b)\times c = a\times (b\times c)$ so $LHS = RHS$ and the induction is closed.

***

### Ex 2.3.4 :

- To prove $\forall a,b \in \mathbb{N} \text{ } (a+b)^2 = a^2 + b^2 + 2ab$. 
- $(a+b)^2 = (a+b)(a+b)$ using the distributive law we write $a(a+b)+b(a+b)= a\dot{}a+a\dot{}b+b\dot{}a+b\dot{}b$. Now using the commutative law we can simplify this as $a^2+2ab+b^2$, which is the $RHS$. Hence proved.

***

### Ex 2.3.5 :

-To prove that $\forall n \in \mathbb{N}, q \in \mathbb{N}-\{0\}, \exists m,r \in \mathbb{N} : (0\leq r \lt q)\wedge(n=mq+r)$
- Let us fix $q$ and induct on $n$
- **Base Case** : for $n=0$ we get $0 = mq + r$, from corollary 2.2.9 we know that $r=0\wedge mq = 0$. From lemma 2.3.3 $m = 0 \vee q = 0$, but we know that $q \in \mathbb{N}-\{0\}$ hence $m=0$. Since $0 \in \mathbb{N}$ so $m,r \in \mathbb{N}$ and also $r + q = q \wedge r \neq q$ which means $0\leq r \lt q$. Hence the base case is true.
- **Inductive Hypothesis** Suppose that for some $n$ the statement is true. We will now prove the same for $n\text{++}$. We can add $1$ to both sides of the inductive hypothesis to get $n+1 = mq + r + 1$, now we can conclude that since $0\leq r\lt q$ then $r+1 = q \vee r+1<q$. Hence we get $(n\text{++} = mq + (r+1)$ for $0 \leq r+1 \lt q)\vee(n\text{++} = (m+1)q+0)$. Hence the induction is closed.
  
***