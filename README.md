Download Link: https://assignmentchef.com/product/solved-snlp-exercise-5
<br>
<h2>Mutual Information</h2>

<h3>1.1                    Independence of variables</h3>

Let <em>X</em><sub>1</sub>, <em>X</em><sub>2 </sub>and <em>Y </em>be binary random variables. Assume that we know that I(<em>X</em><sub>1</sub>; <em>Y </em>) = 0 and I(<em>X</em><sub>2</sub>; <em>Y </em>) = 0. Is it correct to say that I(<em>X</em><sub>1</sub>, <em>X</em><sub>2</sub>; <em>Y </em>) = 0? Prove or provide a counter example.

<h3>1.2                      Mutual information and entropy</h3>

Imagine that you play a game with your friend who chooses an object in the room and you need to guess which object it is. You are allowed to ask the friend questions and the answer is a deterministic function of both the object <em>o </em>and your question <em>q</em>, i.e. <em>f</em>(<em>o,q</em>). The output of this function can be represented as a random variable <em>A</em>.

Suppose that the object <em>O </em>and question <em>Q </em>are also random variables that are independent of each other. Then <em>I</em>(<em>O</em>;<em>Q,A</em>) can be interpreted as the amount of uncertainty about <em>O </em>that we remove if the values of question <em>Q </em>and answer <em>A </em>are known. Show that <em>I</em>(<em>O</em>;<em>Q,A</em>) = <em>H</em>(<em>A</em>|<em>Q</em>). Provide an interpretation to this equation.

Hint: <em>H</em>(<em>X</em>) = 0 if <em>X </em>is deterministic.

<h2>2      Encoding</h2>

<h3>2.1                       Huffman encoding</h3>

The Huffman encoding algorithm is an optimal compression algorithm when only the frequency of individual letters are used to compress the data. The main idea is that more frequent letters get shorter code. You can find a detailed explanation here: <a href="https://en.wikipedia.org/wiki/Huffman_coding#Informal_description">https://en.wikipedia.org/wiki/Huffman_coding#</a>

<a href="https://en.wikipedia.org/wiki/Huffman_coding#Informal_description">Informal_description</a><a href="https://en.wikipedia.org/wiki/Huffman_coding#Informal_description">.</a>

Suppose that you have a string <em>BBBDBACCDBDBACC</em>. Use the Huffman algorithm to calculate the binary encoding for this string. Report the code you obtained for each character, and use it to encode the string.

Based on the formula from the lecture, calculate the optimal code length. How does it relate to the actual length of the code you obtained?

<h3>2.2                       Entropy and encoding</h3>

Let’s assume that you encountered a new language which has 3 vowels and 3 consonants.

<ol>

 <li>First, you counted the individual letter frequencies and got the followingresult:</li>

</ol>

<table width="199">

 <tbody>

  <tr>

   <td width="36">p</td>

   <td width="36">t</td>

   <td width="36">k</td>

   <td width="36">a</td>

   <td width="36">i</td>

   <td width="20">u</td>

  </tr>

  <tr>

   <td width="36">1/8</td>

   <td width="36">1/4</td>

   <td width="36">1/8</td>

   <td width="36">1/4</td>

   <td width="36">1/8</td>

   <td width="20">1/8</td>

  </tr>

 </tbody>

</table>

Using the distribution from above, compute per-letter entropy <em>H</em>(<em>L</em>) for the given language.

<ol>

 <li>After doing some research, you realized that the language has a syllablestructure. All words consist of CV (Consonant Vowel) syllables. Now you have a better model of the language and the joint distribution P(C,V) looks as follows:</li>

</ol>

<table width="112">

 <tbody>

  <tr>

   <td width="23"> </td>

   <td width="39">p</td>

   <td width="30">t</td>

   <td width="20">k</td>

  </tr>

  <tr>

   <td width="23">ai</td>

   <td width="39"></td>

   <td width="30"></td>

   <td width="20">0</td>

  </tr>

  <tr>

   <td width="23">u</td>

   <td width="39">0</td>

   <td width="30"></td>

   <td width="20"> </td>

  </tr>

 </tbody>

</table>

Compute the per-letter <em>H</em>(<em>L</em>) and per-syllable <em>H</em>(<em>C,V </em>) entropy using the probabilities from the table above.

Note that in order to obtain the probabilities of individual letters, you will need to estimate the marginal probabilities from the table above and then divide the marginal probabilities by two. This is needed because the table presents per-syllable, not per-letter statistics.

<ol>

 <li>Compare per-syllable probabilities based on the probability distribution</li>

</ol>

in (a) to the result you obtained in (b). Explain the difference.

<h2>3        Out-of-Vocabulary Words</h2>

<h3>OOV and vocabulary size</h3>

In this exercise you will use the multilingual corpus provided in exercise5_corpora to investigate the relation between the vocabulary size and the OOV rate in different languages. For each corpus, lower-case the text, remove non-alphabetical characters, and apply whitespace-based tokenization.

<ol>

 <li>Partition each corpus into a training corpus (80% of the word tokens) anda test corpus (20% of the word tokens).</li>

 <li>Construct a vocabulary for each language by taking the most frequent 10k(10,000) word types in the training corpus. The vocabulary set should be ranked by frequency from the most frequent to the least frequent.</li>

 <li>Compute OOV rate (percentage) on the test corpus as the vocabularygrows by 1k words. This means that you should increase the vocabulary size starting from 1k words to 2k, 3k, 4k etc.</li>

 <li>For each language, plot a logarithmic curve where the x-axis representsthe size of the vocabulary and the y-axis represents the OOV rate. Each curve should have a legend to identify the language of the text corpus. Write your observations regarding the OOV rate for different languages.</li>

</ol>

Your solution should include the plot for part (d) and the source code to reproduce the results.

<h2>4      Bonus</h2>

<h3>Many questions</h3>

Similar to part 1.2, imagine that you play a game with your friend and try to identify an object by asking questions and the friend gives you binary answers (yes or no). Let’s assume that you need to ask 6.5 questions on average to guess the object and that all your questions are good (i.e. reduce the search space in an optimal way). Can you find a lower bound to the number of objects in the game? Justify your answer.