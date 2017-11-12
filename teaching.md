## Course Title

A hands-on tutorial on Deep Reinforcement Learning

## Course Introduction

This is a very short yet informative tutorial on deep reinforcement learning. This course aims to get students started at writing deep reinforcement learning agent to solve real-world problem. This course will be delivered by Dex and not affilated by any organisations or university. You are welcome to drop by and listen and write your own agent.

If most feedback are positive and some can follow up, Dex may consider open an optional course at next semester.

## Time & Location

Time: TBA
Location: TBA

## teaching timeline

| durartion(min) | content                     |
|----------------|-----------------------------|
| 1              | pre: explain why in English |
| 10             | Python Introduction         |
| 5              | Git Usage                   |
| 10             | Deep Learning Introduction  |
| 10             | Reinforcement Introduction  |
| 5              | Demo                        |
| 10             | Explain Code                |
| 5              | DQN                         |
| 5              | FAQ                         |

## FAQ

### What is Deep Learning? What does machine learn?

* Definition from Geoffrey Hinton [[source]](https://www.youtube.com/watch?v=XG-dwZMc7Ng&t=47s)
> your brain has more than 10 billion neurons in it, the way it works is at each moment each neuron has to decide whether to go ping and it bases that decision on pings it gets from other neurons and it weights those pings so some pings itakes a lot of notice of and these pings tell it either you should go ping or you shouldn't go ping and it changes those weights so by changing how much it listens to otehr neurons a neuron can change how it behaves and that's how you learn everything
> so that just leaves one question which is what's the principle for changing how much you listen to other neurons and that's called a learning algorithm and deep learning is a learning algorithm for chaning how much neuron you're on will reply on other neurons to decide whether to go ping 

* Ping defintion
> query (another computer on a network) to determine whether there is a connection to it.
contact a person briefly (especially electronically).

* Ping original defintion
> make or cause to make a ping.(a short high-pitched ringing sound, as of a tap on a crystal glass.
)

### What is Reinforcement Learning?

Key idea: Learning by interaction.

Unlike supervised learning, where we explicitly instructs machine what to do. In reinforcement leanring, we evaluates the actions based on rewards we get by interacting with environment (observation).

### How does Deep Q-Network Work?

```
Initialize replay memory D to size N
Initialize action-value function Q with random weights
for episode = 1, M do
	Initialize state s_1
	for t = 1, T do
		With probability ϵ select random action a_t
		otherwise select a_t=argmax_a  Q(s_t,a; θ_i)
		Execute action a_t in emulator and observe r_t and s_(t+1)
		Store transition (s_t,a_t,r_t,s_(t+1)) in D
		Sample a minibatch of transitions (s_j,a_j,r_j,s_(j+1)) from D
		Set y_j:=
			r_j for terminal s_(j+1)
			r_j+γ*max_(a^' )  Q(s_(j+1),a'; θ_i) for non-terminal s_(j+1)
		Perform a gradient step on (y_j-Q(s_j,a_j; θ_i))^2 with respect to θ
	end for
end for
```

## Assignment

The assignment of this tutorial is to build a deep reinforcement learning agent to play a video game. You do not need to hand code a game using pygame. You can try use `gym/env` from OpenAI.

You can submit your assignment to *dex@stellarcoder.com*

## Additional Introduction for SA-Office

With AlphaGo winning the world championship, Deep Reinforcement Learning has become a hot topic, especially in China. This time we invited a Year 3 Student Dex who has co-authored a pepar on the field. If you want to know how to write code to implement deep reinforcement leraning agents, you are welcome to this lecture. If you cannot wait to the lecture, you can check this repo[1].

