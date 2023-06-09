Download Link: https://assignmentchef.com/product/solved-cs1010-assignment-6-add-frequency-permutation
<br>
QUESTION 1 Add, Frequency, Permutation

In this question, you are asked to write a program that addstwo non-negative numbers which can be arbitrarily large.The types provided by C can only represent a number up to acertain value.  We have seen that `long long int` is noteven big enough to represent 21!.

For this question, we will represent a number using anarbitrarily long string consisting of characters (of type`char`) `’0’` to `’9’` (note: not integer 0 to 9).  Csupports arithmetic operations on `char` values as well.  Toconvert between the numerical value of a digit character, wecan do the following:

– To convert from a digit character to its numerical value,we subtract the `char` `’0’`.  For instance, `’6′ – ‘0’`will give us the value `6`.

– To convert from a numerical value of a digit to itscharacter, we add the `char` `’0’`.  For instance, `6 + ‘0’`will give us the character `’6’`.

You can read a sequence of non-space characters from thestandard input using `cs1010_read_word`, and print asequence of characters (i.e., a string) to the standardoutput using `cs1010_println_string`.

Write a program `add` that reads from the standard input twonon-negative numbers represented as strings consisting ofdigits ‘0’ to ‘9’, and prints to the standard output the sumof the two numbers.

Your program should use `assert` liberally to check if youare accessing the correct indices.  Every time you access anarray element with index `i`, you should check if `i` iswithin the memory allocated for the array.

You will likely need to use the C standard library function`strlen`, which returns you the number of characters in astring (excluding the terminating ‘ ’).  Look up on how touse this function on your own.  You might need casting ofthe return value to avoid warnings.

The grading criteria for this question is:Your algorithm must add in O(n) time to receive 2 efficiency marks.

### Sample Run“`<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="dbb4b4b2acaf9babbeeaeae2">[email protected]</a>:~/as06-skeleton$ ./add112<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="8ce3e3e5fbf8ccfce9bdbdb5">[email protected]</a>:~/as06-skeleton$ ./add7815<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="fb9494928c8fbb8b9ecacac2">[email protected]</a>:~/as06-skeleton$ ./add99999911000000<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="335c5c5a444773435602020a">[email protected]</a>:~/as04-skeleton$ ./add14000605140006051400060514006051933091193309119330911933091193309119332311993605193914259336963333696“`

# Question 2: Frequency )———————————-

Write a program `frequency`, that, given two strings,consists of alphabets ‘a’ to ‘z’, checks if the samealphabet appears the same number of times in both strings(but maybe in a different order).

For instance, `nus` and `sun` have the same alphabetsappearing the same number of times.  But `soc` and `nus`do not.

Your program should read, from the standard input,

– a string S1, consists of n lowercase alphabets (`a` to `z`)– a string S2, consists of n lowercase alphabets (`a` to `z`)

and print, to the standard output, `YES` if the same set ofalphabets appear the same number of times in both strings,`NO` otherwise.

Your solution must take no more than O(n) time.

A solution that takes longer than O(n) will receive 0 marksfor efficiency.  Furthermore, your solution needs to becorrect to receive marks for efficiency.

### Sample Run“`<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="82ededebf5f6c2f2e7b3b3bb">[email protected]</a>:~/as06-skeleton$ ./frequencysunnusYES<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5738383e202317273266666e">[email protected]</a>:~/as06-skeleton$ ./frequencynussocNO“`

# Question 3: Permutation————————————

Write a program `permutation`, that, given two strings,consists of alphabets ‘a’ to ‘z’, S1 and S2, checks if S2 isa permutation of some substring of S1.  A substring oflength k is a consecutive sequence of k characters from astring.

For instance, `nus` is a permutation of a substring of`suntec`, since `suntec` contains `sun`.  `ntu` is also apermutation of a substring of `suntec`, since `suntec`contains `unt`.  `smu` is not a permutation of any substringof `suntec`.

Your program should read, from the standard input,

– a string S1, consists of k characters, chosen from `a` to `z`– a string S2, consists of n characters, chosen from `a` to `z`

and print, to the standard output, `YES` if S2 is apermutation of some substring of length k from S1, and `NO`otherwise.