Download Link: https://assignmentchef.com/product/solved-cop3223c-program-using-functions-assignment-6
<br>
<h1>Objective</h1>

The purpose of this assignment, is for students to demonstrate knowledge of

<ul>

 <li>the basic template of a simple C program</li>

 <li>the design of user defined C functions</li>

 <li>calling user defined functions in C</li>

 <li>how solution to problems can be developed from a set a functions</li>

</ul>




<strong><u>Problem:</u> </strong>

Your little brother is having trouble with arithmetic. Your parents realize that after taking a few weeks of your C programming course, that you could potentially write a computer program that will allow him to practice his arithmetic skills.




In particular, your program will allow your brother to play two separate games:




<ol>

 <li>A game where he has to complete several additions or multiplications.</li>

</ol>




<ol start="2">

 <li>A game where he has to determine a secret number after being told if his guesses are too high or too low.</li>

</ol>




Your program should prompt your brother with the following menu:




<ol>

 <li>Play Arithmetic Game</li>

 <li>Play Guessing Game</li>

 <li>Print Score</li>

 <li>Quit</li>

</ol>




If he chooses <strong>option 1</strong>, then you should prompt him with the following menu choices:




<ol>

 <li>Addition</li>

 <li>Multiplication</li>

</ol>







Your program should then prompt him for the maximum value of the numbers to be used in the problems and the total number of questions.




Then it should play the game by prompting him with the desired number of additions/multiplications. Your program should keep track of how much time he takes for these problems. In addition, 5 penalty seconds should be added for each incorrect response. The total time he takes (taking into account the penalty seconds) will be used to determine his score for the round.




If he chooses <strong>option 2</strong>, then you should prompt him for the maximum integer, n, for the guessing game. Then your program should generate a random integer in between 1 and n, inclusive. After that, it should prompt your brother for his first guess. After each guess, your program should tell him whether to guess higher or lower. This continues until he gets the number exactly. Your program should also keep track of how much time the game takes to play. This value will be used to determine his score for the round.




For <strong>option 3</strong>, simply report your brother’s total score, which is the sum of his scores from each round he plays.




<h2>Scoring Details</h2>

For the arithmetic game, the score your brother earns is equal to the total amount of time (in seconds) it took him to finish the problems (including penalty seconds) divided by the number of problems he solved.




For the guessing game, the score your brother earns is equal to the total amount of time (in seconds) it took him to guess the secret number divided by two times the number of digits in the maximum number allowed in the game. (For example if the maximum number was 1000, and he took 15 seconds to guess the correct number, then his score would be 15/(2*4) = 1.875.)




The score in seconds then must be converted to an integer number of points in between 0 and 10. In particular, the conversion works as shown in the chart below:




<table width="591">

 <tbody>

  <tr>

   <td width="295">Time, t, (in seconds)</td>

   <td width="295">Corresponding Score</td>

  </tr>

  <tr>

   <td width="295">t &lt; 1</td>

   <td width="295">10</td>

  </tr>

  <tr>

   <td width="295">1 ≤ t &lt; 2</td>

   <td width="295">9</td>

  </tr>

  <tr>

   <td width="295">2 ≤ t &lt; 3</td>

   <td width="295">8</td>

  </tr>

  <tr>

   <td width="295">3 ≤ t &lt; 4</td>

   <td width="295">7</td>

  </tr>

  <tr>

   <td width="295">4 ≤ t &lt; 5</td>

   <td width="295">6</td>

  </tr>

  <tr>

   <td width="295">5 ≤ t &lt; 6</td>

   <td width="295">5</td>

  </tr>

  <tr>

   <td width="295">6 ≤ t &lt; 7</td>

   <td width="295">4</td>

  </tr>

  <tr>

   <td width="295">7 ≤ t &lt; 8</td>

   <td width="295">3</td>

  </tr>

  <tr>

   <td width="295">8 ≤ t &lt; 9</td>

   <td width="295">2</td>

  </tr>

  <tr>

   <td width="295">9 ≤ t &lt; 10</td>

   <td width="295">1</td>

  </tr>

  <tr>

   <td width="295">t ≥ 10</td>

   <td width="295">0</td>

  </tr>

 </tbody>

</table>







<h2>Implementation Details</h2>

You will be required to write the four functions described below. (Note: you may write other functions as well, but these <strong>FOUR</strong> are required.)




<ol>

 <li>A function called <strong>arithGame </strong>which takes 3 integer parameters <strong><em>max</em></strong>, <strong><em>quantity</em></strong> and <strong><em>op; </em></strong>and returns a double<strong><em>.</em></strong> This function gives the user <strong><em>quantity</em></strong> arithmetic questions, where each operand ranges from 1 to <strong><em>max</em></strong>, inclusive. The value of <strong><em>op</em></strong> (operator) dictates whether the problems are addition or multiplication problems.   Namely, if <strong><em>op</em></strong> is 1, they are addition problems, otherwise, they are multiplication problems.   The function returns the number of seconds the user took   to play the entire game, divided by the number of problems they solved.</li>

</ol>




<ol start="2">

 <li>A function called<strong> guessGame </strong>which takes 1 integer parameter <strong><em>max</em></strong> and returns a double. This function allows the user to play the guessing game where the randomly generated number lies in between 1 and max, inclusive.   The value returned is the number of seconds the user took to finish the game divided by the 2 times the number of digits in the number max.</li>

</ol>

<strong> </strong>

<ol start="3">

 <li>A function called<strong> numDigits </strong>which takes an integer parameter <strong><em>number</em></strong> and returns an integer which is equal to the number of digits in number.</li>

</ol>

<strong> </strong>

<ol start="4">

 <li>A function called <strong>numPoints </strong>which takes a double parameter<strong> timesec </strong>and returns an integer. Returns the number of points the user has earned based on time. In particular, if time is less than 1, 10 is  Otherwise, if it is less than 2, 9 is  returned, etc. If time is greater than or equal to 10,  then 0 is returned.</li>

</ol>




<h2>Other Useful Information</h2>




To generate a random number from 0 to b  in C  we use the function call rand()%(b+1).   If you want to generate a number from a to b, use the function call rand()%(b+1-a) + a.




For example to get a random number from 5 to 25 inclusive we use rand()%21 + 5  Seed the random number generator at the beginning of your program. Do this exactly once. Here is the line of code:




srand(time(0));




In order to use this you need to include stdlib.h and time.h at the top of the program.




Please use the following constants for ADD and MULT




#define ADD 1

#define MULT 2




In order to calculate how much time something takes, you can use the time function. In particular, the function call time(0) returns a double that represents the number of seconds after some time. In order to effectively use this, you must call the function twice: once right before you start what you want to time, and once right afterwards. Subtract these two values to obtain the amount of time a segment of code took. Here is a short example:




int start = time(0);

/* Insert code you want to time here. */ int end = time(0); int timespent = end – start;

printf(“Your code took %d seconds.
”, timespent);




In order to carry out the scoring function, it may be helpful to look at the following functions in the math library:




double ceil(double x);

double floor(double x);




Remember, if you want to convert a double to a corresponding integer, you can use a cast as in the example below, where we assume that value is an integer and seconds is a double:




value = (int)seconds;




<strong><u>References</u> </strong>

Textbook: Chapters 3 and 4







<strong><u>Restrictions</u> </strong>

Name the file you create and turn in <em>game.c</em>.







<h1>Submission of Assignment</h1>

Your assignment should be submitted via Webcourses by the deadline. No assignments will be accepted via email.  Your submission should include a single .c file called <strong>game.c.</strong> . Remember that your program will be graded using DevC++ ,  so be sure that your submitted code runs correctly in this IDE.  If you do not have DevC++ on your personal machine, you may use a computer in any lab to test your code.







<strong><em><u>Sample run 1</u> </em></strong>




Please make a selection from the following:

<ol>

 <li>Play Arithmetic Game.</li>

 <li>Play Guessing Game.</li>

 <li>Print Score.</li>

 <li></li>

</ol>

<strong><em>1 </em></strong>

Would you like, 1)Addition or 2)Multiplication?

<strong><em>1 </em></strong>

What is the maximum number you would like?

<strong><em>100 </em></strong>

How many problems do you want?

<strong><em>4 </em></strong>

What is 21+86?

<strong><em>107 </em></strong>Correct, great job!

What is 87+96?

<strong><em>173 </em></strong>

Sorry, that’s incorrect, the answer is 183.

What is 86+70?

<strong><em>156 </em></strong>Correct, great job!

What is 55+4?

<strong><em>59 </em></strong>

Correct, great job!

You took an average of 6.000000 seconds per question.

Your score for the round is 4.

Please make a selection from the following:

<ol>

 <li>Play Arithmetic Game.</li>

 <li>Play Guessing Game.</li>

 <li>Print Score.</li>

 <li></li>

</ol>

<strong><em>2 </em></strong>

Enter the maximum number for the game. <strong><em>100 </em></strong>

Enter the guess!

<strong><em>50 </em></strong>

Your guess is too high, try again.

Enter your guess!

<strong><em>30 </em></strong>

Your guess is too high, try again.

Enter your guess! <strong><em>10 </em></strong>

Your guess is too high, try again.

Enter your guess!

<strong><em>5 </em></strong>

Your guess is too low, try again.

Enter your guess!

<strong><em>7 </em></strong>

Your guess is too high, try again.

Enter your guess!

<strong><em>6 </em></strong>

Great, you guessed the correct number 6 in 6 guesses in 10 seconds.

Your score for the round is 9.

Please make a selection from the following:

<ol>

 <li>Play Arithmetic Game.</li>

 <li>Play Guessing Game.</li>

 <li>Print Score.</li>

 <li></li>

</ol>

<strong><em>3 </em></strong>

Your score is 13.

Please make a selection from the following:

<ol>

 <li>Play Arithmetic Game.</li>

 <li>Play Guessing Game.</li>

 <li>Print Score.</li>

 <li></li>

</ol>

<strong><em>4 </em></strong>

Thank you for playing!





