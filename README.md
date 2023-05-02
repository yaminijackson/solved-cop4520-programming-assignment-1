Download Link: https://assignmentchef.com/product/solved-cop4520-programming-assignment-1
<br>
<u>Note 2:</u>

This     assignment     is         individual.

You     can      use      a          programming language         of         your    choice for       this      assignment.

If you do not have a preference for a programming language and a threading library to use for this assignment, I would recommend using C/C++ and POSIX threads.

Here you can find a brief intro to POSIX threads:

https://computing.llnl.gov/tutorials/pthreads/




<u>Problem 1 (30 points)</u>

Your non-technical manager assigns you the task to find all primes between 1 and 10<sup>8</sup>.  The assumption is that your company is going to use a parallel machine that supports eight concurrent threads. Thus, in your design you should plan to spawn 8 threads that will perform the necessary computation. Your boss does not have a strong technical background but she is a reasonable person. Therefore, she expects to see that the work is distributed such that the computational execution time is approximately equivalent among the threads. Finally, you need to provide a brief summary of your approach and an informal statement reasoning about the correctness and efficiency of your design. Provide a summary of the experimental evaluation of your approach. Remember, that your company cannot afford a supercomputer and rents a machine by the minute, so the longer your program takes, the more it costs. Feel free to use any programming language of your choice <em>that supports multi-threading</em> as soon as you provide a ReadMe file with instructions for your manager explaining how to compile and run your program from the command prompt.







<u>Required Output:</u>

Please print the following output to a file named primes.txt:

&lt;execution time&gt;  &lt;total number of primes found&gt;  &lt;sum of all primes found&gt; &lt;top ten maximum primes, listed in order from lowest to highest&gt;




<u>Notes on Output:</u>

<ol>

 <li>Zero and one are neither prime nor composite, so please don’t include them in the total number of primes found and the sum of all primes found.</li>

 <li>The execution time should start prior to spawning the threads and end after all threads complete.</li>

</ol>

<u>Grading policy:</u>

General program design and correctness: 50%

Efficiency: 30%

Documentation including statements and proof of correctness, efficiency, and experimental evaluation: 20% <u>Additional Instructions:</u>

Cheating in any form will not be tolerated. Please, submit your work via webcourses.




<u>Problem 2 (70 points)</u>




The Dining Philosophers problem was invented by E. W. Dijkstra, a concurrency pioneer, to clarify the notions of deadlock and starvation freedom. Imagine five philosophers who spend their lives just thinking and feasting. They sit around a circular table with five chairs. The table has a big plate of rice. However, there are only five chopsticks (in the original formulation forks) available (see Figure 1 of Chapter 1, Exercise 1 from the textbook). Each philosopher thinks. When he gets hungry, he sits down and picks up the two chopsticks that are closest to him. If a philosopher can pick up both chopsticks, he can eat for a while. After a philosopher finishes eating, he puts down the chopsticks and again starts to think.




<ol>

 <li>Write a program (Version 1) to simulate the behavior of the philosophers, where each philosopher is a thread and chopsticks are shared objects. Notice that you must prevent a situation where two philosophers hold the same chopstick at the same time.</li>

</ol>




<ol start="2">

 <li>Write a program (Version 2) that modifies Version 1 so that it never reaches a state where philosophers are deadlocked, that is, it is never the case that each philosopher holds one chopstick and is stuck waiting for another to get the second chopstick.</li>

</ol>




<ol start="3">

 <li>Write a program (Version 3) so that no philosopher ever starves.</li>

</ol>




<ol start="4">

 <li>Write a program (Version 4) to provide a starvation-free solution for any number of philosophers <em>N</em>.</li>

</ol>




Use <strong>multi-threading</strong> in your solution. You can choose any programming language supporting threads for your implementation. Document your solution well. Keep all 4 versions of your solution into 4 separate files or folders. Provide a README.txt file with detailed instructions on how to compile and run your program from the command prompt.




<u>Grading policy:</u>




General program design and correctness: 60%

Efficiency: 20%

Documentation including statements and proof of correctness, efficiency, and experimental evaluation: 20%




<u>Additional Instructions:</u>

Cheating in any form will not be tolerated.

<ul>

 <li><strong>You should submit four program versions and all documentation in one archive file (zip, tarball, etc.).</strong></li>

 <li>Once a philosopher has chosen his seat, he can’t move to a new position o As such he can only use the chopsticks to his left and right.</li>

 <li>Your design must    implement      the       chopsticks      as        shared</li>

 <li>The philosophers should only interact with each other through the chopsticks.</li>

 <li>Output Format:</li>

</ul>

o When    a          philosopher   goes    from    eating  to         thinking          he        should      output:

<ul>

 <li>“%d is         now     
”    o When          a          philosopher            goes    from    thinking          to         hungry            he        should output:</li>

 <li>“%d is         now     
”</li>

</ul>

o When    a          philosopher   goes    from    hungry            to         eating  he        should      output:

<ul>

 <li>“%d is now     eating.
”       o Two adjacent          philosophers      should never  eat       at         the       same   time.</li>

</ul>

<ul>

 <li>The programs       should run      continuously  until    the       letter   ‘n’        is</li>

 <li>The last      executable      (starvation-free)       should accept a          command-line argument       that     represents     the       number          of</li>

</ul>