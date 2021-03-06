# Walking_Marvin
Using OpenAI Gym to teach Marvin how to walk

[GymAI Docs](https://gym.openai.com/docs)

# Thought Processes

After messing with the code of examples I have come to realize
that AI is all about saving previous iterations and the reward
value that came with that decision. The goal is to then test
a random decision against the save decision and if it is better
you then update the saved decision.

# Observations

Each set of actions is an array of 4 different float values which relate to the joints
of Marvin (Ex. [-0.01040708, -0.03782682, -0.02203254,  0.00013583]). There is a variety of different mathematical matrice equations catered to the evolution strategy to find different float values that may be best. You then go about getting one of those values and sending it
as a action then comparing the reward value and saving it if the reward is better than the previous iterations reward.

Still trying to figure out where exactly it checks to see if the current episode is better than the previous to learn...

Looking at other solutions seems to be the best way to go. Reading the mathematical theories behind evolution is a great way to go about it as well such as [Evolution Strategies as a Scalabale Alternative to Reinforcement Learning](https://arxiv.org/pdf/1703.03864.pdf)

# Current Progress

My code is finally doing something interesting. Marvin is walking about as good a dog standing, actually that may be too much credit. I now just need to figure out how to keep him learning as he goes and make beter decisions rather than just grab random data from the time.

![First Steps GIF](https://media.giphy.com/media/3o7aD5GTkoAoPvz3uU/giphy.gif)