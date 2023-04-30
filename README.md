Download Link: https://assignmentchef.com/product/solved-cs2420-program-5-priority-queues-autocomplete
<br>
Write a program to implement <em>autocomplete</em> for a given set of <em>N</em> strings and nonnegative weights. That is, given a prefix, find all strings in the set that start with the prefix, in descending order of weight.

Autocomplete is an important feature of many modern applications. As the user types, the program predicts the complete <em>query</em> (typically a word or phrase) that the user intends to type. Autocomplete is most effective when there are a limited number of likely queries. Google uses it to save you from typing the entire query.  Cell phones use it to speed up text input.

The application predicts how likely it is that the user is typing each query and presents to the user a list of the top-matching queries, in descending order of weight. These weights are determined by historical data, such as frequencies of search queries from other Google users, or the typing history of a cell phone user. For the purposes of this assignment, you will have access to a set of all possible queries and associated weights (and these queries and weights will not change).

The performance of autocomplete functionality is critical in many systems. According to one study, the application has only about 50<em>ms</em> to return a list of suggestions for it to be useful to the user. Moreover, in principle, it must perform this computation <em>for every keystroke typed into the search bar</em> and <em>for every user</em>!

In this assignment, you will implement autocomplete by using binary search to find the set of queries that start with a given prefix; and using a priority queue of the matching queries to produce the top k possibilities in descending order by weight.

<strong>Part 1:</strong> <strong>Create a max priority queue</strong> as a skew heap.  A max priority queue is a data structure that allows at least two operations: insert which does the obvious thing and deleteMax, that finds, returns, and removes the maximum element in the priority queue.  We also want the heaps to implement a merge operation.  Verify your priority queue works by creating a small test case which shows various combinations of the following operations:

<ul>

 <li>inserts into two different queues,</li>

 <li>prints the queue prettily (so the tree structure can be seen),</li>

 <li>merges the queues,</li>

 <li>deletes max</li>

</ul>

Create test cases which allows you (and the grader) to verify this is working.

<strong>Part 2: Perform autocomplete. </strong>

<ol>

 <li>Read in the file and store it in an array of Terms.</li>

 <li>For each target word (of length r), provide the top “count” matches using the following procedure</li>

</ol>

(a)   Using a binary search on the Term array, find all words  whose first r letters match that of the target word.

<strong>(b)  Put all terms found in part (a) into a priority queue.  </strong> Using weight as a priority, output the top “count” terms.

<strong>Input format</strong>

The first line of the SortedWords.txt file is the number of terms in the file. The remaining items are the word followed by its frequency.

<strong>User Interface</strong>

Allow the user to input (a) the prefix of a word (b) the number of outputs s/he wants to see  (count)

<strong>Output format  </strong>The output will look something like:

Substring: acc  count=9

<table width="70">

 <tbody>

  <tr>

   <td width="70">according</td>

  </tr>

  <tr>

   <td width="70">accept</td>

  </tr>

  <tr>

   <td width="70">account</td>

  </tr>

  <tr>

   <td width="70">access</td>

  </tr>

  <tr>

   <td width="70">accident</td>

  </tr>

  <tr>

   <td width="70">accuse</td>

  </tr>

  <tr>

   <td width="70">accomplish</td>

  </tr>

  <tr>

   <td width="70">accompany</td>

  </tr>

  <tr>

   <td width="70">accurate</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<em>This assignment was developed by Matthew Drabick and Kevin Wayne.Copyright © 2014.</em>

<em> </em>


