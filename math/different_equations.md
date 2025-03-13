# Differential Equations

## 1 Differential equations, a tourist's guide

**"Since Newtown, mankind has come to realize that the <span style="color:GreenYellow">laws of physics</span> are always expressed in the <span style="color:DodgerBlue">language of differential equations</span>." --- <span style="color:Gold">Steven Strogatz</span>**

### 1.1 Introduction

Differential equations araise whenever it's easier to describe change than absolute amounts. It's easier to say why population sizes, for examples, grow or shrink than it is to describe why they have the particular values they do at some point in time.

![de_0](./images/de_0.png)

It may be easier to describe the why you love for someone is changing than why it happens to bewhere it is now.

![de_1](./images/de_1.png)

In physics, more specifically Newtonian mechanics,motion is often describe in terms of force, and force determines acceleration, which is a statement about change.

![de_2](./images/de_2.png)

These equations come in two different flavors:

- Ordinary Different Equations, or ODEs, involving functions with a single input, often thought of as time
- Partial Different Equations, or PDEs, dealing with functions that have multiple inputs.

![de_3](./images/de_3.png)

Partial different equations are something we often think of them as involving a whole continuum of values changing with time, like the temperature at every point of a solid body, or the velocity of a fluid at every point in space.

![de_4](./images/de_4.png)

Ordinary different equations, our involve only a finite collection of values changing with time. And it doesn't have to be time per say, your one indenpent variable could be something elese, but things changing with time are the prototypical and most common example of different equations.

![de_5](./images/de_5.png)

Physics offeres a nice playground for us here, with simple examples to start with, and no shortage of intricacy and nuance as we delve deeper.

![de_6](./images/de_6.png)

![de_7](./images/de_7.png)

Consider the trajectory of something you throw in the air.

![de_8](./images/de_8.png)

The force of gravity near the surface of Earth causes things to accelerate downward at $9.8m/s^{2}$. It means if you look at that object free from other forces, and records its velocity at every second, these velocity vectors will accrue an additional small downward component of $9.8m/s$ everu second, we call this constant 9.8 for gravity.

![de_9](./images/de_9.png)

Focus on the y-coordinate as a function of time, whose derivative in turn gives the vertical component of acceleration.

![de_10](./images/de_10.png)

![de_11](./images/de_11.png)

![de_12](./images/de_12.png)

For compactness, let's write the first derivative as $\dot{y}$ and the second derivative as $\ddot{y}$. Our equation says that $\ddot{y}$ is equal to negatie $g$, a simple constant.

![de_13](./images/de_13.png)

This is one we can solve by integrating, which is essentially working the question backwards. First, to find velocity, what function has negative $g$ as a derivatie? => $-gt$, or more specifically, $-gt + v_{0}$, $v_{0}$ -> the initial velocity.

Notice that there are many functions with this particular derivative, so you have an extra degree of freedom which is determined by an inital condition.

![de_14](./images/de_14.png)

Now what function has this as a derivative? It turns out to be negative one-half g times t squared plush that initial velocity times t, and again we're free to add an additional constant without changing the derivative, and that constant is determined by whatever the inital position is.

![de_15](./images/de_15.png)

There you go, we just solved a different equation, figuring out what a function is based on information about its rate of change.

### 1.2 Higherorder different equations

### 1.3 Pendulum different equations

### 1.4 Visualization

### 1.5 Phasespace

### 1.6 Love

### 1.7 Computing
