# Introduction
This project involves the implementation of first-order and Nth-order Markov models. The models were used on sentences and writing pieces to calculate transition probabilities and generate new text.
# Pseudocode
```
get_next_word
For every state in the Markov model:
  Add up how many times each possible next word occurs
  Convert counts into probabilities by dividing by the total
Look up the list of possible next words for the current state
Look up the corresponding probabilities for those next words
Randomly select one next word using those probabilities
Return the selected word


generate_random_text

Set random number generator with seed
Determine the Markov model order at the time 
Create a starting state using “*S” order number
Set the current state to the start state
Create an empty list to store the generated random words

Create a loop:  
  Pick the next word based on the current state
  If the next word equals “*E”
  Stop generating words
  If not,
      Add the word to the list
      To move to the next state, update the current state by dropping the oldest word and shifting to add the new word 

Join all the generated words to form a sentence
Return the sentence

Markov model for one fish two fish

Create an empty Markov model
Open the one_fish_two_fish.txt
Create an empty string to store the text
For each line in the file:
       Remove extra whitespaces from the line
	Add the line to the empty string
Use the string to train the Markov model with an order of 3 	
         
Markov model for sonnet
Create empty Markov model
Open sonnets.txt
Start with empty string for one sonnet
For each line in the file:
  Remove extra whitespace from the line
If the line is blank:
  Add the sonnet to the Markov model
  Reset the sonnet text to empty
Else:
  Add the line to the current sonnet text
Generate a random text sequence from the Markov model
```

# Successes
One of our biggest successes was that we learnt how a Markov model worked practically and how to implement them.


# Struggles
One struggle we faced was making current_word a tuple in the get_random_text function for n > 1. At first, the function we built was taking current_word as a string and trying to replace the tuple with a string. 
We initially struggled with placing the random seed on the right function so that it doesn't cause the randomness to reset every call and potentially lead to repetitive outputs. 

# Personal Reflections
## Group Leader
Sneha: Jersha and Connor were both great group members. We were able to meet three times to work through the code together and problem solve.  I had never worked with Markov models before, so I found the implementation to be a little challenging  It was very helpful to talk through the logic involved in Markov model implementation in order find solutions for bugs in our code.

## Other member
Aaronie Jersha Jenyfred: My group members were great to work with. This is my first time learning about Markov Models and I initially had a hard time understanding how to work around it but as a group we were able to co-ordinate very well in terms of building & debugging the code and trying to overcome some challenging errors. Discussing about the bugs and improvising the code together surely helped me understand the topic better. 

# Generative AI Appendix
As per the syllabus
