---
title: "Concepts to Understand Reinforcement Learning"
date: 2021-04-17
lastmod: 2021-05-17
tags: ["reinforcement-learning", "introductory"]
math: true
---

>In which I explain what is reinforcement learning, where it fits in the whole as a machine learning paradigm.
>Some of the basic concepts of reinforcement how they interact with each other and some possible directions.


## Introduction
Reinforcement learining — RL — seems to be the hot topic in machine learning nowadays, it's the basis for the [algorithm that beat the Go champion](https://www.scientificamerican.com/article/how-the-computer-beat-the-go-master/), a game in which, pundits claim, a computer would not be able to beat a human within this century and also it is what makes you spend more when shopping online. I believe that when starting to learn a new topic two things are necessary:

- What it means as a whole, the big picture.
- The first principles, which are the basis for every other concept.

This makes it possible to formulate and understand 99% of reinforcement learning problems. This article explains what RL represents at a high level and the basic ideas. This, I believe, is enough to understand the basics of anything related to reinforcement learning.

## The Big Picture

Reinforcement learning like machine learning can be described in very simple terms like creating a computer program that learns from data, and after learning performs some action when more data is presented to it. Simple as that, we don't need to complicate it further in this article. Specifically in Reinforcement Learning, learning takes place through interactions in certain situations and depending on the situation and action, it ends up receiving more or less rewards.

The rewards received in each interaction show how to behave better in the future ie **learning** by trial and error. However our program is not happy with only immediate gratification, it tries to act in each situation in order to maximize future rewards.

Every time our program takes an action it can modify the way information, data, will present itself in the future, a change in the environment. This is probably the biggest difference between reinforcement learning and the other areas of machine learning and what makes it shine on specific problems.

In summary, there are three main features in RL:

- Learning by trial and error.
- Maximization of future rewards.
- Interaction and modification of future information through actions.

## Elements

Now that we have in mind what reinforcement learning represents as a whole, we need to stop looking at the forest and start looking at the trees. So let's get into the details of what are the necessary parts of a basic RL model.

Since these concepts are rather abstract, we'll use a simple and practical example like a tic-tac-toe game. In a tic-tac-toe game we are creating a program whose goal is to win most of the games played and games against opponents (human or other programs) learn to win more games in the future.

### The Agent

The first element is the agent that represents the program programmed to play Tic-Tac-Toe. In RL the agent is any entity that is performing actions and receiving rewards. In practice it does not necessarily need to be a computer program, it can be a mechanism or even a living being depending on the problem. However for most purposes it is an algorithm that someone ends up programming, meaning a computer program :P.

### The Environment

Environment is everything that is not considered the agent. In our case of a tic-tac-toe it could be the opponent, the board and the entire universe, including all its quantum states, but in practice it  only represents the things around the agent relevant to the problem being solved. In our case it would be the board and the opponent. The agent performs actions in the environment and through it receives rewards and information that it can use, this information is known as environmental states.

### States

States are the situations and information that make up the environment. We can say that the environment is composed of all possible states and states are the situations that arise for the agent through interaction with the environment. In mathematical terms these states are represented by data or variables that represent each state.

The states in our example would be all possible combinations of a tic-tac-toe game. Each time a player makes a move, the game configuration, the board as a whole and which squares are occupied and empty, change and a new state appears to the agent.

It is important to mention that in the literature there is a subtle distinction between the states already mentioned above and the states that our agent actually receives information about, known as observations because they are states that are actually observed by the agent. States represent all possible information including the ones that the agent does not have access to. The term States ends up being used much more frequently, even when one is actually talking about observations.

In our tic-tac-toe game, the states, which include information that our agent does not have access to, would include the opponent's thoughts and their future moves, whereas the observations would only be the information the ones that the agent has access, the configurations of the the pieces on the board.

Mathematically, states are described through:

$$ s \in S $$

a state $s$ belonging to the set of all possible states $S$.
