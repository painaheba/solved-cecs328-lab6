Download Link: https://assignmentchef.com/product/solved-cecs328-lab6
<br>
<strong>Programming assignment 6. </strong>

Write a recursive function to calculate the <em>minimum positive subsequence sum</em> (MPSS). In other words, of all subsequences whose sum adds to a positive number, you want to determine the minimum of such sums.

<strong><u>Hint</u></strong>:

➢ Use the same idea of divide and conquer algorithm for MSS, but now it is not so easy to compute MPSS<sub>middle</sub>, (<strong>Explain why</strong>? (<u>You could make a counter example on a piece of</u> <u>paper</u>)




<strong><u>To find MPSS<sub>middle</sub></u></strong><u>:</u>

<ol>

 <li>For each subarray there are <em>n/2</em> such subsequence sums. (Find them and save them in 2 different arrays called S<sub>L</sub> and S<sub>R</sub>) (e.g. Let’s say that the left subarray is: a<sub>L</sub> = [ 2, -3, 1, 4, -6] ➔ S<sub>L </sub>= [-2, -4, -1, -2, -6])</li>

 <li>Using quicksort, sort S<sub>L</sub> in <em>ascending</em> order and S<sub>R</sub> in <em>descending</em></li>

 <li>Define two markers: i and j: Let i be the index marker of S<sub>L</sub>, and j for S<sub>R</sub>.</li>

 <li>Set s<sub>min</sub> = <em>inf</em>. Now start iterating through S<sub>L</sub> and S<sub>R</sub>:

  <ol>

   <li>If s = S<sub>L</sub>(i) + S<sub>R</sub>(j) ≤ 0, then increment i.</li>

   <li>Else if s &lt; s<sub>min</sub>, then set s<sub>min</sub> = s, and increment j,</li>

   <li>Otherwise, we have s &gt; s<sub>min</sub>, in which case we increment j.</li>

   <li>Set MPSS<sub>middle</sub> = s<sub>min</sub> when the elements of S<sub>L</sub> or S<sub>R</sub> have been exhausted.</li>

  </ol></li>

 <li><strong><u>Calculate</u> </strong>the time complexity of your algorithm for finding MPSS on paper and show your answer to me. Running time should satisfies <em>T(n) = Θ(nlog<sup>2</sup> n).</em></li>

 <li><strong><u>Explain how/why the algorithm</u> </strong>for MPSS<sub>middle</sub> (You may write your answer on paper)</li>

</ol>




Ask the user for the size of the array (<em>n</em>) and generate <em>n</em> random numbers between -20 to 20.

<strong><u>Example</u></strong>:

<strong><u>Input</u></strong>:    A = [2, -3, 1, 4, -6, 10, -12, 5.2, 3.6, -8],  <strong><u>Output</u></strong>: MPSS = 0.8


