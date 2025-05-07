

## Question 1: 
Find the general solution for the system corresponding to the following augmented matrix in terms of the free variable $x_{2}$. Each answer is expressed in the form of $ax_{2} + b$ . 
$$\left[\begin{array}{cccc|c}
1 & -4 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 4 \\
0 & 0 & 0 & 1 & -5 \\
\end{array}
\right]$$
#### Solution and Concepts:
**Solution**:
- **Identify pivot and free variables**:
   From the augmented matrix $$\left[\begin{array}{cccc|c}
1 & -4 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 4 \\
0 & 0 & 0 & 1 & -5 \\
\end{array}
\right]$$we see **pivot** positions in columns 1, 3, and 4. Column 2 has no pivot, so $x_{2}$ is a **free variable**.

- **Solve for pivot variables in terms of the free variable**:
   - Row 1: $x_{1}-4x_{2}=2⟹$$$x_{1}=4x_{2}+2$$
   - Row 2: $x_{3}=4$
   - Row 3: $x_{4}=-5$

- **Write the general solution**:
  Let $t=x_{2}$ . Then $$\begin{pmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4} \\
\end{pmatrix} = \begin{pmatrix}
4t + 2 \\
t \\
4 \\
-5 \\
\end{pmatrix}, \quad
  t \in \mathbb{R}.
  $$Equivalently, each variable expressed in the form $ax_{2}+b$:
	  $x_{1} = 4x_{2}+2$ 
	  $x_{2} = 1\cdot x_{2}+0$
	  $x_{3} = 0\cdot x_{2}+4$
	  $x_{4} = 0\cdot x_{2}-5$

------------------------------------------------------------------------

**Key concepts**:
- **Pivot vs. free variables**: Pivot columns correspond to dependent (basic) variables solved in terms of free variables
	- **Pivot variables** are the ones you solve for.
	- **Free variables** are the ones you get to choose — they’re like the "input". The pivot variables depend on whatever values you pick for the free ones.
	  
- **Parametric form**: Free variables (here $x_{2}$) act as parameters tracing out the solution set, which is an affine line in $\mathbb{R^4}$
	- You can describe all the solutions to the system using the free variable like a dial.
		- As you turn the dial (change $x_{2}$), you get different solutions.
		- All those solutions form a line in 4D space — kind of like a line drawn in 3D, but one dimension higher.
		- Imagine dragging a dot along a line — that dot is tracing all the possible solutions by changing $x_{2}$.
	
- **Dimension of solution space:** Number of free variables (1) equals the nullity of the coefficient matrix, indicating a one‑dimensional family of solutions.
	- The number of free variables tells you how many different directions your solutions can go.
		- If there's **1** free variable, then the solutions form a **1D line**.
		- If there were **2** free variables, the solutions would form a **2D plane**, and so on.
		- One free variable = One direction = Line of solutions.







## Question 2: 
Consider the following two row operations that transform the matrix on the left to the matrix on the right. 
$$
\begin{bmatrix}
1 & 2 & 3 \\
-1 & 1 & 1 \\ 
1 & 1 & 0 \\
\end{bmatrix}
\xrightarrow{(1)}
\begin{bmatrix}
4 & -1 & 0 \\
-1 & 1 & 1 \\ 
1 & 1 & 0 \\
\end{bmatrix}
\xrightarrow{(2)}
\begin{bmatrix}
4 & -1 & 0 \\
1 & 1 & 0 \\ 
-1 & 1 & 1 \\
\end{bmatrix}
$$Let $E_{1}$ and $E_{2}$ be the elementary matrices corresponding to the operations in (1) and (2) above respectively. Find $E_{1}E_{2}$ . 

If $E_{1}E_{2}=\begin{bmatrix}a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33}\end{bmatrix}$ , then 
#### Solution and Concepts:
**Solution**:
- **Determine each elementary operation**:
	- **Operation (1):**$$\begin{bmatrix}
1 & 2 & 3 \\
-1 & 1 & 1 \\ 
1 & 1 & 0 \\
\end{bmatrix}
\xrightarrow{(1)}
\begin{bmatrix}
4 & -1 & 0 \\
-1 & 1 & 1 \\ 
1 & 1 & 0 \\
\end{bmatrix}
	  $$Comparing the first 2 rows shows $$[4,-1,0]=[1,2,3]-3[-1,1,1]$$so (1) is the row operation $$R_{1}\to R_{1}-3R_{2}$$
	  - **Operation (2):**$$\begin{bmatrix}
4 & -1 & 0 \\
-1 & 1 & 1 \\ 
1 & 1 & 0 \\
\end{bmatrix}
\xrightarrow{(2)}
\begin{bmatrix}
4 & -1 & 0 \\
1 & 1 & 0 \\ 
-1 & 1 & 1 \\
\end{bmatrix}
	    $$swaps rows 2 and 3: $$R_{2} \leftrightarrow R_{3}$$
- **Write the elementary matrices**:
	- For $R_{1}\to R_{1}-3R_{2}$, the elementary matrix is $$E_{1} = I + (-3)E_{1,2} = \begin{bmatrix}
1 & -3 & 0 \\
0 & 1 & 0 \\ 
0 & 0 & 1 \\
\end{bmatrix}
	  $$
	  
	  - For swapping $R_{2}$ and $R_{3}$, the elementary matrix is the permutation $$E_{2}=\begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & 1 \\ 
0 & 1 & 0 \\
\end{bmatrix}$$
- **Compute the product $E_{1}E_{2}$:$$E_{1}E_{2}=\begin{bmatrix}
1 & -3 & 0 \\
0 & 1 & 0 \\ 
0 & 0 & 1 \\
\end{bmatrix}
  \begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & 1 \\ 
0 & 1 & 0 \\
\end{bmatrix} = \begin{bmatrix}
1\cdot1+(-3)\cdot0 & 1\cdot0+(-3)\cdot0 & 1\cdot0+(-3)\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot0+1\cdot0 & 0\cdot0+1\cdot1 \\ 
0\cdot1+0\cdot0 & 0\cdot0+0\cdot1 & 0\cdot0+1\cdot0 \\
\end{bmatrix} = \begin{bmatrix}
1 & 0 & -3 \\
0 & 0 & 1 \\ 
0 & 1 & 0 \\
\end{bmatrix}
  $$
------------------------------------------------------------------------

**Key Concepts**:
- **Elementary matrices** encode single row‑operations: adding a multiple of one row to another, or swapping rows.
	- Elementary matrices are like tiny instruction sheets that tell you to do **one simple thing** to a matrix row:
		- Either **swap two rows**, or
		- **Add or subtract** a multiple of one row to another.
		- If matrices are like recipes, then an elementary matrix is just **one step** in that recipe — like “add 2 × Row 1 to Row 3” or “switch Row 2 and Row 4.”
		  
- **Matrix Multiplication** of elementary matrices composes their corresponding operations in sequence: here $E_{1}E_{2}$ applies the swap first, then the row-addition.
	- When you multiply two elementary matrices, it’s like **stacking row operations** in order.
		- **$E₂$** might be “swap two rows.”
		- **$E_{1}$** might be “add 3 times one row to another”
		- So $E_{1}E_{2}$ could mean: 
		  Do $E_2$ **first** (swap rows),
		  then $E_{1}$ (add rows)
	- Matrix multiplication applies steps **from right to left**, like doing instructions backwards.
	  
- The resulting product $E_{1}E_{2}$ itself is the single matrix that, when left-multiplied by the original, effects *both* operations in order. 
	- If you combine two elementary matrices ($E_{1}$ and $E_{2}$) by multiplying them, you get **one matrix** that does **both steps** at once.
	- So instead of applying the two row operations one after the other, you can just **multiply the original matrix by the product $E_{1}E_{2}$**, and it will do both operations **in the correct order**.




## Question 3: 
Use the Gauss-Jordan elimination method to find the inverse matrix of the matrix $$\begin{bmatrix}0 & 3 & -5 \\ 0 & 2 & -4 \\ 1 & -3 & 0\end{bmatrix}$$ Choose the elementary row operations (in 5 steps) that will lead you to the inverse. 
#### Solution and Concepts:
**Solution**:
- **Set up the augmented matrix**: $$\left[\begin{array}{ccc|ccc}
0 & 3 & -5 & 1 & 0 & 0 \\
0 & 2 & -4 & 0 & 1 & 0 \\
1 & -3 & 0 & 0 & 0 & 1 \\
\end{array}
\right]
  $$
  - **Swap $R_{1}$ and $R_{3}$**
	  - Bring a 1 into the $(1,1)$ pivot position:  $$
		    R_{1}\leftrightarrow R_{3} ⟹ \left[\begin{array}{ccc|ccc}
1 & -3 & 0 & 0 & 0 & 1 \\
0 & 2 & -4 & 0 & 1 & 0 \\
0 & -3 & -5 & 1 & 0 & 0 \\
\end{array}
\right]
		    $$
- **Scale $R_{2}$ to make its pivot 1**: $$R_{2} \to \frac{1}{2}R_{2} ⟹ \left[\begin{array}{ccc|ccc}
1 & -3 & 0 & 0 & 0 & 1 \\
0 & 1 & -2 & \frac{1}{2} & \frac{1}{2} & 0 \\
0 & -3 & -5 & 1 & 0 & 0 \\
\end{array}
\right]
  $$
- **Eliminate the $x_{2}$-entries in $R_{1}$ and $R_{3}$
	- $R_{1} \to R_{1}+3R_{2}$
	- $R_{3} \to R_{3}-3R_{2}$ $$ \left[\begin{array}{ccc|ccc}
1 & 0 & -6 & 1.5 & 1.5 & 1 \\
0 & 1 & -2 & 0.5 & 0.5 & 0 \\
0 & 0 & 1 & -0.5 & -1.5 & 0 \\
\end{array}
\right]
	  $$
-  **Eliminate the $x_{3}$-entries in $R_{1}$ and $R_{2}$
	- $R_{1} \to R_{1}+6R_{3}$
	- $R_{2} \to R_{2}+2R_{3}$ $$ \left[\begin{array}{ccc|ccc}
1 & 0 & 0 & 6+1.5(-1) & ? & ? \\
0 & 1 & 0 & 2+0.5(-1) & ? & ? \\
0 & 0 & 1 & -0.5 & -1.5 & 0 \\
\end{array}
\right]
	  $$Filling in the arithmetic: $$ \left[\begin{array}{ccc|ccc}
1 & 0 & 0 & 6 & -\frac{15}{2} & 1 \\
0 & 1 & 0 & 2 & -\frac{5}{2} & 0 \\
0 & 0 & 1 & -\frac{1}{2} & -\frac{3}{2} & 0 \\
\end{array}
\right]
	  $$Thus the right-hand block is $A^{-1}$: $$ A^{-1}=\left[\begin{array}{ccc}
 6 & -\frac{15}{2} & 1 \\
 2 & -\frac{5}{2} & 0 \\
-\frac{1}{2} & -\frac{3}{2} & 0 \\
\end{array}
\right].
	  $$
------------------------------------------------------------------------

**Key Concepts**:
- **Gauss-Jordan elimination** transforms $[A \;| \;I]$ to $[I\;|\;A^{-1}]$ by applying elementary row-operations
	- Gauss–Jordan elimination is a step-by-step process where you use row operations to turn a matrix $A$ into the identity matrix $I$.
	- But you don’t do this to A alone—you attach the identity matrix next to A like this:
	  $[A \;|\; I] ←$ this is called an **augmented matrix**.
		- While you’re turning **$A$ into $I$** on the left,
		- The **right side** (which started as $I$) is **changing** — and it eventually becomes $A⁻¹$ (the inverse of $A$).
		  
- **Row–swaps**, **scaling**, and **row–adds** correspond to multiplying on the left by elementary matrices; composing them yields $A^{-1}$
  
- Each pivot operation zeroes out the off‑pivot entries in its column, producing the identity on the left.
	- When you're using row operations to solve a matrix, each **pivot operation** focuses on one column at a time.
	- The **pivot** is the main number you're working with (usually a 1).
	- The goal is to make **everything else in that column become 0**, except the pivot.
	- Doing this for each column step-by-step turns the left side of your matrix into the **identity matrix** — a matrix with 1’s on the diagonal and 0’s everywhere else.
	  
- The final right block is guaranteed to be $A^-1$ provided $\det(A)\neq0$; here $\det(A)=-2\neq0$
	- When you use Gauss–Jordan elimination to turn $[A \;| \;I]$ into $[I \;|\; A⁻¹]$, you’ll **only get $A⁻¹$** on the right **if $A$ can be inverted**.
		- If **$\det(A) ≠ 0$**, then A **has an inverse**.
		- If **$\det(A) = 0$**, then A **does not** have an inverse.



## Question 4: 
Let $A=\begin{bmatrix}2 & -1 & 1 & -3 \\ 1 & 7 & -2 & 2 \\ -2 & 0 & 4 & 6\end{bmatrix}$ and $B$ be the matrix obtained from $A$ by performing first the row operation $-3R_{3}+R_{1}\to R_{1}$ , then the row operation $R_1 \xleftrightarrow{} R_3$ . 

The third row of $B$ is : 
#### Solution and Concepts:
**Solution**:
- **First row operation - $-3R_{3}+R_{1}\to R_{1}$:
	- Original rows of $A$: $$R_{1} = [2,-1,1,-3], \quad R_{3}=[-2,0,4,6].$$
	- Compute $-3R_{3}=[6,0,-12,-18].$
	- Update $R_1$: $$R_{1} = [2,-1,1,-3]+[6,0,-12,-18]=[8,-1,-11,-21].$$
- **Second row operation -** swap $R_1$ and $R_3$ ($R_{1}\leftrightarrow R_{3}$)
	- After the swap, the rows of $B$ are $$R_{1}=[-2,0,4,6],\quad R_{2}=[1,7,-2,2],\quad R_{3}=[8,-1,-11,-21]$$
- So the final answer is (third row of $B$): $$R_{3}=[8,-1,-11,-21]$$
------------------------------------------------------------------------

**Key Concepts**:
- **Elementary row operations** can be applied in sequence to transform a matrix; combining a multiple of one row with another then swapping rows is captured by left‑multiplication by appropriate elementary matrices.
  
- **Row addition and swapping** affect only the targeted rows, making it straightforward to track the resulting entries.





## Question 5: 
Use the Gauss-Jordan elimination method to find the inverse of the matrix 
$$ A = 
\begin{bmatrix}
1 & 2 & 6c  \\
-4 & -7 & -4 \\ 
0 & 0 & 2 \\
\end{bmatrix}
\quad
\text{where } c \text{ is some constant.}
$$If $A^{-1}=\begin{bmatrix}a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33}\end{bmatrix}$ , then 
#### Solution and Concepts:
**Solution**:
- **Set up the augmented matrix $[A\;|\;I]$:$$\left[\begin{array}{ccc|ccc}
1 & 2 & 6c & 1 & 0 & 0 \\
-4 & -7 & -4 & 0 & 1 & 0 \\
0 & 0 & 2 & 0 & 0 & 1 \\
\end{array}
\right]
  $$
- **Eliminate the $(2,1)$ entry by $R_2\to R_{2}+4R_{1}$**: $$R_{2}:[-4,-7,-4]+4[1,2,6c]=[0,1,24c-4],\quad [0,1,0]+4[1,0,0]=[4,1,0].$$ $$\left[\begin{array}{ccc|ccc}
1 & 2 & 6c & 1 & 0 & 0 \\
0 & 1 & 24c-4 & 4 & 1 & 0 \\
0 & 0 & 2 & 0 & 0 & 1 \\
\end{array}
\right]
  $$
- **Eliminate the $(1,2)$ entry by $R_1\to R_{1}-2R_{2}$**: $$R_{1}:[1,2,6c]-2[0,1,24c-4]=[1,0,6c-48c+8]=[1,0,8-42c],$$ $$[1,0,0]-2[4,1,0]=[-7,-2,0]$$$$\left[\begin{array}{ccc|ccc}
1 & 2 & 8-42c & -7 & -2 & 0 \\
0 & 1 & 24c-4 & 4 & 1 & 0 \\
0 & 0 & 2 & 0 & 0 & 1 \\
\end{array}
\right]
  $$
- **Normalize the third row by $R_3\to\frac{1}{2}R_{3}$:$$
  R_{3}=[0,0,1\;|\;0,0,\frac{1}{2}].
  $$
- **Eliminate above the $(3,3)$ pivot**: 
	- $R_{1}\to R_{1}-(8-42c)R_{3}$
	- $R_2\to R_{2}-(24c-4)R_{3}$
	  
	  Computations on the right side:
	  $R_{1}$-$\text{rhs}$ : $[-7,-2,0]-(8-42c)[0,0,\frac{1}{2}]=[-7,-2,-\frac{8-42c}{2}]=[-7,-2,21c-4]$,
	  $R_{2}$-$\text{rhs}$ : $[4,1,0]-(24c-4)[0,0,\frac{1}{2}]=[4,1,-\frac{24c-4}{2}]=[4,1,-12c+2]$.
	  
	  So the final augmented matrix is $$\left[\begin{array}{ccc|ccc}
1 & 0 & 0 & -7 & -2 & 21c-4 \\
0 & 1 & 0 & 4 & 1 & -12c+2 \\
0 & 0 & 1 & 0 & 0 & \frac{1}{2} \\
\end{array}
\right]
	  $$
- So the answer $A^{-1}$: $$ A^{-1} = \begin{pmatrix}
-7 & -2 & 21c-4 \\
4 & 1 & -12c+2 \\ 
0 & 0 & \frac{1}{2}
\end{pmatrix}
  $$
----------------------------------------------------------------

**Key Concepts:**
- **Block‑triangular structure** (a zero row in the third column below) simplifies the process, allowing one to isolate the last pivot quickly.
	- If your matrix already has some **zeros in helpful spots**, especially **below the pivots**, it’s easier and faster to solve.
		- A **block-triangular structure** just means your matrix is partly shaped like a triangle — with zeros in places you’d normally try to make zero anyway.
		- A **block-triangular structure** just means your matrix is partly shaped like a triangle — with zeros in places you’d normally try to make zero anyway.
		  
- **Normalization** of each pivot (scaling a row to make the pivot 1) and **elimination** above and below pivots systematically produces the inverse.
	- To turn a matrix into its inverse using Gauss–Jordan elimination, you follow two main steps over and over:
			- **Normalize the pivot** – If the pivot (the main number in a row) isn’t 1, you divide the whole row to make it 1.
			- **Eliminate everything else in the pivot’s column** – 1. Use row operations to make all the numbers **above and below the pivot become 0**.





## Question 6: 
Given that $A=\begin{pmatrix}0 & -2 & 0\\ 1 & -3 & 2 \\ 0 & -1 & -1\end{pmatrix}$ and $B=\begin{pmatrix}a & 0 & -1 \\ 2 & 1 & c \\ 0 & b & 4\end{pmatrix}$ , find **$AB$**. 
#### Solution and Concepts:
**Solution**:
- **Compute $AB$ entrywise**: 
	- By definition, $(AB)_{ij}=\sum^{3}_{k=1}{A_{ik}B_{kj}}$ . Writing $$A=\begin{pmatrix}0 & -2 & 0\\ 1 & -3 & 2 \\ 0 & -1 & -1\end{pmatrix}, \quad B=\begin{pmatrix}a & 0 & -1 \\ 2 & 1 & c \\ 0 & b & 4\end{pmatrix}
	  $$we compute row by column:
		- **Row 1 of $AB$**:
		  $(AB)_{11} = 0\cdot a+(-2)\cdot2+0\cdot0=-4$,
		  $(AB)_{12}=0\cdot 0+(-2)\cdot1+0\cdot b=-2$,
		  $(AB)_{13}=0\cdot (-1)+(-2)\cdot c+0\cdot 4=-2c$
		- **Row 2 of $AB$**:
		  $(AB)_{21}= 1\cdot a + (-3)\cdot2 + 2\cdot0 = a - 6,$
		  $(AB)_{22}= 1\cdot0 + (-3)\cdot1 + 2\cdot b = 2b - 3,$
		  $(AB)_{23}= 1\cdot(-1) + (-3)\cdot c + 2\cdot4 = 7 - 3c$
		- **Row 3 of $AB$**:
		  $(AB)_{31}= 0\cdot a + (-1)\cdot2 + (-1)\cdot0 = -2,$
		  $(AB)_{32}= 0\cdot0 + (-1)\cdot1 + (-1)\cdot b = -1 - b,$
		  $(AB)_{33}=0\cdot(-1) + (-1)\cdot c + (-1)\cdot4 = -c - 4$
		  
- **Assemble the product matrix for answer**: $$AB = \begin{pmatrix}
  -4      & -2       & -2c\\
  a - 6   & 2b - 3   & 7 - 3c\\
  -2      & -1 - b   & -c - 4
\end{pmatrix}. $$
----------------------------------------------------------------

**Key Concepts**:
- **Matrix multiplication** is not entry-wise but defined by the dot product of rows of the first matrix with columns of the second.
	- When you multiply two matrices, you **don’t** just multiply matching numbers in each spot.
		- You take a **row** from the first matrix
		- And a **column** from the second matrix
		- Then you **multiply the matching numbers** in the row and column and **add them up**. That total becomes **one entry** in the new matrix.
		  Ex. For specifically the spot for $AB_{11}$ (Row 1, Column 1),  Row 1 of $A$ was $[0,-2,0]$, Column 1 of $B$ was $[a,2,0]$:
		  - Multiply each pair and add:
			  $0\times a = 0$
			  $-2\times2=-4$
			  $0\times0=0$
			  Total: $0+(-4)+0=-4$, so $AB_{11}=-4$

- The $(i,j)$-**entry** of the product captures how the $i$th linear combination of rows of $A$ interacts with the $j$th column of $B$.
- **Parameters**  $a$, $b$, and $c$ carry through linearly into the corresponding entries of $AB$.




## Question 7: 
Given $A=\begin{bmatrix}a & 1 & -2 & 3 \\ b & 3 & 1 & 0 \\ c & 0 & 1 & 2 \\ d & 6 & -2 & 1\end{bmatrix}$ , 

1. Find the cofactor $C_{41}$ of $A$ :
2. Given the cofactors of $A$:
   $C_{12}=2,\;C_{22}=-1,\;C_{32}=-4,\;C_{42}=1$ , find $\det(A)$ :
#### Solution and Concepts:
![[Untitled 17.pdf]]



## Question 8: 
1. Find the area of the triangle in the $\mathbb{R^2}$ plane whose vertices are given by $(0,0),\;(-1,4)$ and $(7,-2)$ :
2.  Find the volume of the parallelepiped defined by the vectors $$
   \begin{bmatrix} 
-2 \\
0 \\
-1 \\
\end{bmatrix} , \;
\begin{bmatrix} 
1 \\
2 \\
5 \\
\end{bmatrix} \; \text{and }
\begin{bmatrix} 
-2 \\
0 \\
-1
\end{bmatrix}
   $$ 
#### Solution and Concepts:
![[Untitled 18.pdf]]

----------------------------------------------------------------

**Key Concepts**:
- **Triangle area in $\mathbb{R^2}:\frac{1}{2}|\det[u \;v]|$** measures the parallelogram spanned by $u$, $v$, halved for a triangle
- **Parallelepiped volume in $\mathbb{R^3}$**$:|\det[\mathbf{a}\,\mathbf{b}\,\mathbf{c}]|$; if any two spanning vectors are linearly dependent (identical here), the volume is zero.


## Question 9: 
Find the value of $k$ so that the matrix $\begin{bmatrix}3 & k & -1 \\ -3 & 2 & 1 \\ 1 & 0 & 1\end{bmatrix}$ is **NOT** invertible :
#### Solution and Concepts:
![[Untitled 19.pdf]]



## Question 10: 
Given that $A,\;B$ and $C$ are $3\times3$ matrices with $\det(A)=-2,\;\det(B)=4,\;\det(C)=3$ , find the following determinants:
1. $\det(A^2B^T)=$
2. $\det(A^2+B^2)=$
3. $\det(CB^{-1})=$
#### Solution and Concepts:
![[Untitled 20.pdf]]



## Question 11: 
Given that the reduced echelon form of the augmented matrix of a linear equation system (with variables $x_{1},\;x_{2},\;x_{3},\;x_{4},\;x_{5}$) is $$\left[\begin{array}{ccccc|c}
1 & -2 & 0 & 2 & 0 & -3 \\
0 & 0 & 1 & 3 & 0 & 8\\
0 & 0 & 0 & 0 & 1 & 5\\
\end{array}
\right]$$
1. Identify the free variables $x_{i}$ and $x_{j}$ where $(i < j)$ :
2. Express the solutions of the linear equation system in terms of free variables $x_{i}$ and $x_{j}$ in the following format: $$ \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\ 
x_{4} \\
x_{5} \\
\end{bmatrix} = \begin{bmatrix}
a_{1} \\
a_{2} \\
a_{3} \\ 
a_{4} \\
a_{5} \\
\end{bmatrix} + x_{i}\begin{bmatrix}
b_{1} \\
b_{2} \\
b_{3} \\ 
b_{4} \\
b_{5} \\
\end{bmatrix} + x_{j}\begin{bmatrix}
c_{1} \\
c_{2} \\
c_{3} \\ 
c_{4} \\
c_{5} \\
\end{bmatrix}
   $$
#### Solution and Concepts:
![[Untitled 21.pdf]]

----------------------------------------------------------------

**Key Concepts**:
- **Free vs. basic variables:** Pivot columns yield basic variables solved in terms of the free ones.
- **Parametric vector form:** The general solution of a consistent linear system with two free variables is an affine plane (here in $\mathbb{R}^5$), expressed as a particular solution $a$ plus linear combinations of direction vectors $b$ , $c$.
- **Dimension of solution space:** Number of free variables (2) equals the dimension of the solution space.

## Question 12: 
- Let $V$ be the vector space of all $2\times2$ matrices with real number entries.
- Let $H_{1}$ be the subset of $V$ that contains all $2\times2$ upper triangle matrices 
- Let $H_2$ be the subset of $V$ that contains all $2\times2$ with at most one non-zero entry (that is, every entry in each matrix in $H_2$ is zero with at most one exception)

Based on the statements above, choose all statements that are correct:
1. $H_1$ is closed under scalar multiplication
2. $H_1$ is a subspace of $V$
3. $H_2$ is closed under matrix addition
4. $H_2$ is closed under scalar multiplication 
5. $H_2$ is NOT a subspace of $V$ 
6. $H_1$ is closed under matrix addition
#### Solution and Concepts:
![[Untitled 22.pdf]]



## Question 13: 
Let $V$ be vector space of all $3\times2$ matrices with real number entires. Find the coordinate vector $[M]_{B} =\begin{bmatrix}m_{1}\\m_{2}\\m_{3}\\m_{4}\\m_{5}\\m_{6}\\\end{bmatrix}$ of the matrix $M=\begin{bmatrix}2 & 5 \\ 1 & -7 \\ -3 & 4\end{bmatrix}$ under the standard basis $B=\{\begin{bmatrix}1 & 0 \\ 0 & 0 \\ 0 & 0\end{bmatrix},\; \begin{bmatrix}0 & 1 \\ 0 & 0 \\ 0 & 0\end{bmatrix},\; \begin{bmatrix}0 & 0 \\ 1 & 0 \\ 0 & 0\end{bmatrix},\; \begin{bmatrix}0 & 0 \\ 0 & 1 \\ 0 & 0\end{bmatrix},\; \begin{bmatrix}0 & 0 \\ 0 & 0 \\ 1 & 0\end{bmatrix},\; \begin{bmatrix}0 & 0 \\ 0 & 0 \\ 0 & 1\end{bmatrix}\}$
#### Solution and Concepts:
![[Untitled 23.pdf]]

----------------------------------------------------------------

**Key Concept:** Under the standard (matrix entry) basis, the coordinate vector of $M$ is simply the list of its entries in the order corresponding to the basis elements.

## Question 14: 
Let $T$ be a linear transformation from $\mathbb{R^3}$ to $\mathcal{P}_{2}$ defined by $$ T(\begin{bmatrix}
a_{1} \\
a_{2} \\
a_{3} \\
\end{bmatrix}) = (9a_{1} - 3a_{2} + 5a_{3})x^2 + (3a_{1}+a_{2}-4a_{3})x+8a_{1}-4a

$$Let $\mathcal{B}=\{\begin{bmatrix}1 \\ 0 \\ 0 \end{bmatrix},\; \begin{bmatrix}0 \\ 1 \\ 0 \end{bmatrix},\; \begin{bmatrix}0 \\ 0 \\ 1 \end{bmatrix}\}$ be the basis for $\mathbb{R^3}$ and $\mathcal{B'}$ = $\{ x^2,\;x,\;1\}$ be a basis for $\mathcal{P}_{2}$ . 
Find the standard matrix of $A$ of $T$ with respect to $\mathcal{B}$ and $\mathcal{B'}$ 

If $A=\begin{bmatrix}a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33}\end{bmatrix}$ then:
 
#### Solution and Concepts:
![[Untitled 24.pdf]]



## Question 15: 
Let $A$ be a $7\times9$ matrix. If the nullity of $A$ is 6, find its rank:
#### Solution and Concepts:
![[Untitled 25.pdf]]

----------------------------------------------------------------

- **Key Concept:** The number of free parameters (nullity) plus the number of leading variables (rank) always equals the total number of variables (columns).
- **Interpretation:** Even though $A$ maps $\mathbb{R}^9$ into $\mathbb{R}^7$, its image is only a 3-dimensional subspace of $\mathbb{R}^7$.


## Question 16: 
Let $A$ be a $4\times4$ matrix whose determinant is -4 
- Let $A_{1}$ be the matrix obtained from A by performing the row operation $12\mathbb{R_{4} + \mathbb{R_{1}} \to R_{1}}$
- Let $A_{2}$ be the matrix obtained from A by performing the row operation $\mathbb{R_{1} \leftrightarrow R_{4}}$
-  Let $A_{3}$ be the matrix obtained from A by performing the row operation $8\mathbb{R_{2} \to R_{2}}$
Then, 
$\det(A_1) =$
$\det(A_2) =$
$\det(A_3) =$
#### Solution and Concepts:


![[Untitled 26.pdf]]

## Question 17: 
Let $A$ be a $3\times3$ matrix such that its cofactor matrix is $C=\begin{pmatrix}-3 & -2 &7 \\ -4 & 1 & 2 \\ 0 & -2 & 5\end{pmatrix}$ and $\det(A)=-\frac{1}{5}$  . 
Find the inverse matrix of $A$ (Find $A^{-1}$) :
#### Solution and Concepts:
![[Untitled 28.pdf]]

----------------------------------------------------------------

- The **cofactor matrix** $C$ has entries $C_{ij}=(-1)^{i+j}\det(M_{ij}).$
- The **adjugate** is its transpose, $\text{adj}(A)=C^T$.
- The inverse is given by $A^{-1}=\frac{1}{\det(A)}\text{adj}(A)$
- Here, the negative determinant in the denominator flips the sign of every entry in the adjugate.

## Question 18: 
Let $u=\begin{bmatrix}-2 \\ 3 \\ 1 \\\end{bmatrix},\;v=\begin{bmatrix}0 \\ -1 \\ 4 \\\end{bmatrix},\;b=\begin{bmatrix}-4 \\ 2 \\ -8 \\\end{bmatrix}$ . Determine if $b$ is a linear combination of $u, v$. That is, if $b = a_{1}u+a_{2}v$ for some constant $a_{1}, a_{2}$.  
#### Solution and Concepts:
![[Untitled 29.pdf]]



## Question 19: 
Solve the linear equation system $\left\{\begin{array}{rcl}2x_{1}-5x_{2}=a \\ 5x_{1}-13x_{2}=b\end{array}\right.\quad$using Cramer's rule. Express your answer in terms of $a$ and $b$ : 
#### Solution and Concepts:
![[Untitled 30.pdf]]

----------------------------------------------------------------

**Key Concept:** Cramer’s rule expresses each variable as the ratio of a determinant where that variable’s column is replaced by the constants, over the determinant of the original coefficient matrix.

## Question 20: 
Let $T:\mathbb{R^5 \to R^3}$ be a linear transformation defined by $T(x)=Ax$ where $$A = \begin{bmatrix}
1 & 1 & -2 & 1 & 0 \\
0 & 0 & 1 & 3 & 1 \\
-2 & -2 & 5 & 1 & 1 \\
\end{bmatrix}
$$What is 
1. $\text{Rank}(T) =$
2. $\text{Nullity}(T) =$
#### Solution and Concepts:
![[Untitled 31.pdf]]

----------------------------------------------------------------

- **Key Concept:** Row‑reduction reveals the number of independent columns ($\mathrm{rank}$), and the dimension of the solution space of $Ax=0$ is the number of free variables ($\mathrm{nullity}$).
- **Interpretation:** The map $T$ sends $\mathbb{R}^5$ onto a 2‑dimensional subspace of $\mathbb{R}^3$, with a 3‑dimensional kernel in its domain.

## Question 21: 
Given that the inverse of the matrix $A$ is $A^{-1}=\begin{bmatrix}5 & 2 & 0  \\ 1 & -2 & 3  \\ -1 & 2 & 2\end{bmatrix}$ , find the solution of the linear equation system $A\begin{bmatrix}x_{1} \\x_{2} \\x_{3}\end{bmatrix}=\begin{bmatrix}1 \\-1 \\3\end{bmatrix}$
#### Solution and Concepts:
![[Untitled 32.pdf]]



## Question 22: 
Find the characteristic polynomial of the matrix $A=\begin{bmatrix}5 & 0 & 0  \\ -2 & 2 & -4  \\ 4 & -5 & 3\end{bmatrix}$ . If the polynomial is $-\lambda^3+c_{1}\lambda^2+c_{2}\lambda+c_{3}$ , then :
#### Solution and Concepts:
![[Untitled 27.pdf]]

----------------------------------------------------------------

- **Characteristic polynomial:** $\det⁡(A−λI)$.
- **Expansion along a row with zeros** simplifies the determinant.
- **Matching form:** Expand and collect like terms to identify coefficients $c_1,c_2,c_3$

## Question 23: 
Find the eigenvalues of the matrix $A=\begin{bmatrix}-7 & -3 & 8 \\ 0 & 5 & -3 \\ 0 & -4 & 6\end{bmatrix}$
#### Solution and Concepts:
![[Untitled 33.pdf]]



## Question 24: 
Given that $A$ is a $3\times3$ matrix with eigenpairs $(3, \begin{bmatrix}1 \\ 2 \\ 7\end{bmatrix}),\;(-7, \begin{bmatrix}1 \\ -2 \\ 2\end{bmatrix})\;$ and $(-2, \begin{bmatrix}2 \\ 1 \\ -1\end{bmatrix})\;$ ,
Find the matrix $M=\begin{bmatrix}b_{11} & b_{12} & b_{13} \\ b_{21} & b_{22} & b_{23} \\ b_{31} & b_{32} & b_{33}\end{bmatrix}$ such that $M^{-1}AM=\begin{bmatrix}-7 & 0 & 0 \\ 0 & -2 & 0 \\ 0 & 0 & 3\end{bmatrix}$
#### Solution and Concepts:
![[Untitled 34.pdf]]



## Question 25: 
Given that $A$ is a $6\times6$ matrix and that $A$ has eigenvalues -1, 1 and 4 whose algebraic multiplicities are 1, 3 and 2 respectively:
1. Find the determinant of $A$ : $\det(A) =$
2. Let $B$ be a matrix that is similar to $A$. Find the determinant of $B^2$ : $\det(B^2) =$
#### Solution and Concepts:
![[Untitled 35.pdf]]



## Question 26: 
Suppose that the vectors $[1, -2, 0]$ and $[2,3,-1]$ form the sides of a parallelogram. Find the lengths of the two diagonals of the parallelogram. Round 3 decimal places.
#### Solution and Concepts:
![[Untitled 36.pdf]]



## Question 27:
Select the pairs of vectors that are orthogonal to each other:
1. $[2,-1,-2,1]\text{ and }[1,0,-2,-7]$
2. $[1,1,2]\text{ and }[3,2,-3]$
3. $i-2j\text{ and }2i+j+k$
4. $[a,b]\text{ and }[-b,a]$
5. $[0,8,0,1,0,6]\text{ and }[1,0,9,0,3,0]$
6. $[2,2,2]\text{ and }[-2,4,-2]$
#### Solution and Concepts:
![[Untitled 37.pdf]]



## Question 28: 
Find the angle (in degrees, no radians) between the vectors $7i-j+2k$ and $-2i-j+3k$ . Express answer as a numerical number and round off to exactly 3 digits. 
#### Solution and Concepts:
![[Untitled 38.pdf]]






