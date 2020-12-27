# HMM-and-Modification-to-Viterbi
Modified Viterbi Algorithm to deal with the problem of Unknown words

The Vanilla viterbi algorithm is a basic strategy and has manny shortcomings.
The vanilla Viterbi algorithm we had written had resulted in ~87% accuracy. 
The approx. 13% loss of accuracy was majorly due to the fact that when the algorithm encountered an unknown word (i.e. not present in the training set, such as 'Twitter'), it assigned an incorrect tag arbitrarily. 
This is because, for unknown words, the emission probabilities for all candidate tags are 0, so the algorithm arbitrarily chooses (the first) tag.

Here, I have worked up on two modifications to the algorithm to make it adaptable to presence of unknwom words.
The first version just replaces the "0" emission probabilities with the transition probabilities.
The second version uses a trigram tagger backed by a regexp tagger as a modification to the viterbi algorithm.
