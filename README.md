# RL for Hangman

We first setup a Hangman environment which allows us to play hangman with a particular dictionary of words (and a set of rules). 

We then define a baseline model which matches long and short patterns of an input (based on the training dictionary). A somewhat slow and thorough version of this baseline long-short-pattern matching approach already achieves over 60% accuracy on a (distinct) test dictionary.

Finally we train two RL approaches:

1. Policy Gradient: We train a neural net using a policy gradient approach in tensorflow. We eventually find that training is sped up if we remove the policy and simply train on minimizing the loss function. After some training, we achieve over 50% test accuracy, but continuing with training would lead to better scores. This model is a lot faster than the hard-coded baseline.

2. Deep Q-Learning (DQN): We train a neural net with the same architecture as the one above using a deep q-learning (and it's variations, Double Deep DQN and Dueling Double DQN) approach. Some training leads to slowly increasing test scores, but we did not run it long enough to achieve anything substantial.
