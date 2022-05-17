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

****

## Some Explanations

Logically proposition/ lemma/ theoram/ corllary are all staements waiting to be proved. However they have different levels of importance.

Here p$\implies$q translates to *if* p *then* q.

1. *Axiom/ Postulate/ Assumption* is a statement that is taken to be true to serve as a basis for further arguments.
2. *Proposition* is a declarative statement expressing opinion that is yet to be proved.
3. *Lemma*  is an easily proved claim which is helpful for proving other propositions and theorems, but is usually not particularly interesting in its own right
4. A corollary is a quick consequence of a proposition or theorem that was proven recently
5. *Converse* is q$\implies$p while the theoram is the statement p$\implies$q.
6. *Inverse* is !p$\implies$!q
7. *Contrapositive* is !q$\implies$!p
8. *Objects* are entities that have certain special properties. ( They may or may not have a physical meaning/ representation.)

****

## Peoano's Axioms

- **Axiom 2.1** : 0 is a natural number.
- **Axiom 2.2** : If n is a natural number then n++ is also a  natural number.
- **Axiom 2.3** : 0 is not the succesoor of any natural number. ie $\forall n \in \N : n$++ $\not ={0}$
- **Axiom 2.4** : Different natural numbers must have different succesors. ie : $\forall n,m \text{ }  n\text{++} = m\text{++} \implies n = m$
- **Axiom 2.5** : If a property P(n) holds P(0) and if P(n) $\implies$ P(n++) is true $\forall\N$ then P(n) holds $\forall\N$.


**Note** : *a priori* is what one knows before hand ie what is assumed to be true before beginning the argument or proof. *a posteiori* is what one knows to be true after the proof or argument has ended.

**Note** : Induction is a useful method of proof. 
    - To prove : there is a property P(n) that is true for all natural numbers $\N$.
    - Step 1 : Prove the base case for (n = 0).
    - Step 2 : Assume that P(n) holds for all numbers till n and prove P(n++).
  
  Induction can be done in other ways also (1) strong induction (2) backward induction (3) transfinite induction.

**Note** : Recursive definitions can be used to assign a unique naturan number for each natural number, Thus it is possible to generate sequences using recursion.

****
## Addition

pg 26 : prove that n++ = n + 1.
*Proof* : by lemma 2.2.2 $(n\text{++}) + 0 = n\text{++}$. By definition $(n\text{++}) + 0 = (n+0)\text{++}$. By lemma 2.2.3 $(n+0)\text{++} = n + (0\text{++})$ which is equal to $n+1$ since $0\text{++} = 1$ by defintion.