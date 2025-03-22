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

Things get mmore interesting when the forces acting on a body depend on where that body is. For example, studying the motion of planets, stars, and moons, gravity can no longer be considered a constant. Given two bodies, the pole on one of them is in the direction of the other, with a strength inversely proportional to the square of the distance between them.

![de_16](./images/de_16.png)

As always, the rate of change of position is velocity, but now the rate of change of velocity, acceleration, is some function of position, so you have this dance between two mutually interacting variables, reminiscent of the dance between the two moving bodies which they describe.

### 1.2 Higherorder different equations

This is reflective of the fact that often in differential equations, the puzzles you fae involve finding a function whose derivative and higher order derivatives are defined in terms of the function itself.

![de_17](./images/de_17.png)

In physics it's most common to work with second order differential equations, which means the highest derivatives you find in this expression is a second derivative.

Higher order differential equations would be ones involving third derivatives, forth derivatives, and so on, puzzles with more intricate clues.

![de_18](./images/de_18.png)

The sensation you get when you really meditating on one of these equations is one of solving an infinite continous jigsaw puzzle. In a sense, you have to find infinitely many numbers, one for each point in time t, but they're constrained by a very spcific way that these values intertwine with their own rate of change, and the rate of change of that rate of change.

![de_19](./images/de_19.png)

Let's review the deceptively simple eample, a pendulum. How does this angle $\theta$ that it makes with the vertical change as a function of time?

This is often as an example in introductory physic classes of harmonic motion, meaning it oscillates lke a sine wave. More specifically, one with a period of 2 pi times the square root of L over g, wher L us the length of pendulum and g is the strength of gravity.

![de_20](./images/de_20.png)

However, these formulas are actually **_lies_**, or rathe approximations which only work in the realm of small angles. If you were go and measure an actual pendulum, what you find is that as you pull it out farther, the period is **longer** than what the high school physics formular would suggest.

![de_21](./images/de_21.png)

When you pull it out really far, this value of $\theta$ ploted versus time doesn't even look like a sine wave anymore.

### 1.3 Pendulum different equations

To understand what's really going on, first things first,let's set up the different equation.

We'll measure the position of the pendulum's weight as a distance $x$ along this arc, and if this angle $\theta$ we care about is measured in radians, we can write $x$ as $L\theta$, where $L$ is the length of the pendulum.

![de_22](./images/de_22.png)

As usual, gravity pulls down with an acceleration of $g$, but because the pendulum contrains the motion of this mass, we have to look at the component of this acceleration in the direction of motion.

![de_23](./images/de_23.png)

So the component of gravity in the direction of motion opposite this angle will be $-gsine\theta$.

![de_24](./images/de_24.png)

Here we're considering $\theta$ to be positive when the pendulum is swung to the right, and negative when it's swung to the left. This $-sin$ in the acceleartion indicates that it's always pointed in the opposite direction from displacement.

So what we have is that the second derivative of x, the acceleration $\ddot{x}$, is $-gsine\theta$.

![de_25](./images/de_25.png)

As always, it's nice to do a quick gut check that our formula makes physical sense. When $\theta$ is 0, $sin0 = 0$, so there's no accerleration in the direction of movement.

![de_26](./images/de_26.png)

When $\theta$ is 90 degrees, $sin\theta$ is 1, so the acceleration is the same as it would be for freefall.

![de_27](./images/de_27.png)

And because $x = L\theta$, that means the second derivative of $\theta$ is ${-g\over{L}}sine\theta$

![de_28](./images/de_28.png)

To be a little more realistic, let's add in a term to account for the air resistance, which mayve we model as being proportional to the velocity. We'll write this as $-\mu \dot{\theta}$, where $\mu$ is some constant that encapsulates all the air resistance and friction and such that determines how quickly the pendulum loses energy. This is a particular juicy different equation.

![de_29](./images/de_29.png)

It's not eqsy to solve, but it's not so hard that we can't resonably get some meaningful understanding out of it.

At first glance, you might think that the sine function relates to the sine wave pattern for the pendulum. Ironically, though, what you'll eventually find is that the opposite is true.

![de_30](./images/de_30.png)

The presence of the sine in this equation is precisely why real pendulums don't oscillate with a sine wave pattern. If that sounds odd, consider the fact that here, the sine function is talking $\theta$ as an input, but in the approximate solution you might see in a physics class, $\theta$ itself is oscillating as the output of a sine function.

![de_31](./images/de_31.png)

Clearly something fishy is afoot. One thing I like this example is that, even though it's comparatively simple, it exposes an important truth about differential equation that you need to grapple with. Thet are really freaking hard to solve!

In this case, if we remove that dampening term, we can just barely write down an analytic solution, but' it's hilariously completed. It involves all these functions probably never heard of, written in terms of intergrals and weird inverse integral problems.

![de_32](./images/de_32.png)

When you step back, presumably the reason for fining a solution is to then be able make computations and build an understanding for whatever dynamics you're studying.

![de_33](./images/de_33.png)

In this case, those questions have been punted off to figuring out how to compute, and more importantly, understand, these new functions.

![de_34](./images/de_34.png)

So instead, in the study of differential eequations, we often do a sort of short circuit, and skip the the actual solution part, since it's unattainnable, and go straight to building and making computation from the equation alone.

![de_35](./images/de_35.png)

### 1.4 Visualization

Start by visualizing all possible states in a two-dimensional plane.

![de_36](./images/de_36.png)

By the state of the pendulum, is that you can describe it with two numbers: the angle $\theta$ and the angular velocity $\dot{\theta}$. You can freely change either one of those two values without necessarily changing the other, but the accelearation is purely a function of those two values.

![de_37](./images/de_37.png)

So each point of thi two-dimensional plane fully describes the pendulum at any given moment. You might think of these aas all possible initial conditions of that pendulum. If you know the initial angle and the angular velocity, that's enough to predict how the sytem will evolve as time moves forward.

![de_38](./images/de_38.png)

What you're looking at now, this inward sprial, is a fairly typical trajectory for our pendulum. Notice how at the start, as $\theta$ decreases, $\dot{\theta}$, the y-coordinate, gets more negative.

![de_39](./images/de_39.png)

Which makes sense, because the pendulum moves faster in the leftward direction as it approaches the buttom. Keep in mind, even though the velocity vector on this pendulum is pointed to the left, the velue of that velocity is always being represented by the vertical component of our space.

![de_40](./images/de_40.png)

It's important to remind yourself that this state space is an abstract thing, and is distinct from the physical space where the pendulum itself lives and moves. Since we're modeling this as losing some of its energy to air resistance, this trajectory spirals inward, meaning the peak velocity and peak displacement each go down a bit with each swing. Our point is, in a sense, attracted to the origin, where $\theta$ and $\dot{\theta}$ both equal $0$.

With this space, we can visualize a differential equation as a vector field. The pendulum state is a vector [$\theta$, $\dot{\theta}$]. Maybe you think of that as an arrow from the origin, or maybe you think of it as a point.

![de_41](./images/de_41.png)

What matters is that it has two coordinates, each a function of time. Taking the derivative of that vector gives its rate of change, the direction and speed that it will tend to move in this diagram.

![de_42](./images/de_42.png)

That derivative is a new vector, [$\dot{\theta}$, $\ddot{\theta}$], which we visualize as being attached to the relevant point in space.

The first component for this rate of change vector is $\dot{\theta}$, which is also a coordinate in our space. The higher up we are in the diagram, the more the point tends to move to the right, and the lower we are, the more it tends to move to the left.

![de_43](./images/de_43.png)

![de_44](./images/de_44.png)

The vertical component is $\ddot{\theta}$, which is our differential equation lets us rewrite entirely in terms of $\theta$ and $\dot{\theta}$ itself. in other words, the first derivative of our state vector is some function of that vector itself, with most of the intricacy tied up in that second coordinate.

![de_45](./images/de_45.png)

During the same all points of this space will show how that state ends to change from any position.

![de_46](./images/de_46.png)

How that state tends to change from any position. As is typical with vector field, we artificially scale down the vectors when we draw them to prevent clutter, but use color to loosely indicate magnitude.

Notice we've effectively broken up a single second-order equation into a system of two first-order equations.

![de_47](./images/de_47.png)

We might even give $\dot{\theta}$ a different name, to emphasize that we're really thinking of two separate values, intertwined via mutual effect they have on one another's rate of change. This is a common trick in the study of differential equations.

![de_48](./images/de_48.png)

Instead of thinking about higher order changes of a single value, we often prefer to think ofthe first derivative of vector values.

What exactly some of these trajectory lines say about the possible ways of the pendulum evovles from different starting conditions.

For example, in regions where $\dot{\theta}$ is quite high, the vectors guide the point to travel to the right quite a ways before settling down into an inward sprial. This corresponds to a pendulum with a high enough initial velocity that it fully rotates around several times before setting into a decaying back and forth.

![de_49](./images/de_49.png)

![de_50](./images/de_50.png)

When I tweak this air resistance term, $\mu$, say increasing it, you can immediately see how this will result in trajectories that sprial inward faster, which is to say the pendulum slows down faster.

![de_51](./images/de_51.png)

![de_52](./images/de_52.png)

![de_53](./images/de_53.png)

That's obvious when I call it the air resistance term, but imagine that you saw these equations out of contet, not knowing that they described a pendulum. It's not obvious just looking at them that increasing this value of $\mu$, means the system as a whole tends towards some attracting state faster.

What's wonderful is that any system of ordinary differential equations can be describe by a vector filed like this, so it's a very general way to get a feel them.

![de_54](./images/de_54.png)

Usually, though, they have many more dimensions. For example, consider the famous three-body problem, which is to predict how three masses in three-dimensional space evolve if they act on each other with gravity, and if you know their initial positions and velocities.

![de_55](./images/de_55.png)

### 1.5 Three body problem

Usually, though, they have many more dimensions, each mass has three coordinates describing its position, and three more describing its momentum. So the system has 18 degrees of freedom in total, and hence an 180dimensional space of possible states.

![de_56](./images/de_56.png)

A single point meandering through an 18-dimensional space that we cannot visualize, obediently taking steps through time based on whatever vector it happens to be sitting on from moment to moment, completely encoding the position and the moemta of the three masses we see in ordinary, physical 3D space.

![de_57](./images/de_57.png)

In practice, you can reduce the number of dimensions here by taking advantage of the symmetries of your setup, but the point that more degrees of freedom results in higher dimensional state spaces remains the sane.

### 1.6 Phasespace

![de_58](./images/de_58.png)

In math, we often call a space like this a phase space. We use that term broadly for spaces encoding all kinds of states of changing systems, but you should know that in the context of physics, especially Hamiltonian mechanics, the term is often reserved for a more special case, namely a space whose axes represent position and momentum.

![de_59](./images/de_59.png)

So a physicist would agree that the 18-dimensional space describing the three-body problem is a phase space, but they might ask that we make a couple of modifications to our pendulum setup for it to properly deserve the term.

![de_60](./images/de_60.png)

For those of you who just watched the block collision video, the planes we worked with there would be called phase spaces by math folk, though a physicist might prefer other terminology.

![de_61](./images/de_61.png)

Just know that the specific meaning may depend on your context. It may seem like a simple idea, depending on how well indoctrinated you are to modern ways of thinking about math, but it's worth keeping in mind that it took humanity quite a while to really embrace thinking of dynamics spatially like this, especially when the dimensions get very large.

![de_62](./images/de_62.png)

![de_63](./images/de_63.png)

One reason its powerful is that you can ask questions, not just about a single intial condition but about a whole spectrum of initial states. The collection of all possible trajectories is reminiscent of a moving fluid.

![de_64](./images/de_64.png)
![de_65](./images/de_65.png)

So we call it **phase flow**, to take one example of why phase flow is a fruitful idea, consider the quetion of stability.
![de_66](./images/de_66.png)

The origin of our space corresponds to the pendulum standing still, and so does this point over here, representing when the pendulum is perfectly balanced upright.

![de_67](./images/de_67.png)

These are the so-called **fixed points** of our system, and one natural question to ask is whether or not they're stable, that is, with tiny nudges to the sytem result in a state that tends back towards that fixed points, or away from it?

Physical intuition for the pendulum makes the answer here kind of obvious, but how would you think about stability just looking at the equations, say if they arose in some completely different less intuitive context?

![de_68](./images/de_68.png)

The intuition for the relevant computations are guided heavily by the thought of looking at small regions in space around a fixed point, and asking whether the flow tends to contract or expand.

![de_65](./images/de_65.png)

### 1.7 Love

And speaking of attraction and stability, let's take a brief side-step to talk about love.

**"Since Newton, mankind has come to realize that the <span style="color:gold">laws of physics</span> are always expressed in the language of <span style="color:dodgerblue">differential equations</span>. --- Steven Strogatz"**

![de_69](./images/de_69.png)
![de_70](./images/de_70.png)
![de_71](./images/de_71.png)

Imagine you've been flirting with someone, but there's been some furustrating inconsistency to how mutual your affection seems, and perhaps during a momnet when you turn your attention towards physics to keep your mind off the romantic turmoil, mulling over the broken-up pendulum equations, you suddenly understand the on-off-again dynamics.

![de_72](./images/de_72.png)

You've notice that your own affection tends to increase when your companion seems interested in you, but decrease when they seem colder. That is, the rate of change of your love is proportional to their feelings for you.

But this sweetheart of your is precisely the opposite, strangely attracted to you when you seem ininterested, but turned off once you seem too keen.

![de_73](./images/de_73.png)
![de_74](./images/de_74.png)
![de_75](./images/de_75.png)

The phase space for these equations looks very similiar to the center part of your pendulum diagram. The two of you will go back and forth between affection and repulsion in an endless cycle. A metaphor of pendulum swings in your feelings would not just be apt, but mathematically verified.

![de_76](./images/de_76.png)

In fact, if your partner's feelings were further slowed when they feel themselves too in love, let's say out of a fear of being made vulnerable, we'd have a term matching the friction in the pendulum, and you too would be destined to inward spiral towards mutual ambivalence. I hear wedding bells already.

![de_77](./images/de_77.png)

The point is that two very different-seeming laws of dynamics, one from physics, involving a single variable, and another from, chemistry, with two variables, actually have a very similiar structure, easier to recoginize when you're looking at the phase diagram.

![de_78](./images/de_78.png)

Most notably, even though the equations are different, for example there's no sine function in the romance equations, the phase space exposes an underlying similarity nevertheless.

![de_79](./images/de_79.png)

In other words, we're not just studying a pendulum right now, the tactics you develop to study one case have a tendency to transfer to many others.

### 1.8 Computing

One way to do this is to essentially simulate what the universe would do, but using finite steps instead of the infinitesimals and limits defining calculus.

![de_80](./images/de_80.png)

Tha basic idea is that if you are at some point in the phase diagram, take a step based on the vector you're sitting on for a small time step, $\Delta{t}$. Specifically, take a step equal to $\Delta{t}$ times that vector $\Delta{t}\vec{v}$.

![de_81](./images/de_81.png)

As a reminder, in drawing these vector fields, the magnitude for each vector has been artificially scaled down to prevent clutter.

![de_82](./images/de_82.png)

When you do this repeatly, you final location will be an approximation of $\Delta{t}$, where $t$ is the sum of all those time steps. Now it's inaccurate because the time steps $\Delta{t}$ of $0.5$ is way too big.

![de_83](./images/de_83.png)

If we turned it down, say to 0.01, you can get a much more accurate approximation, it just takes more repeated steps is all. In this case, computing $\Delta$ of $10$ requires 1000 little steps.

![de_84](./images/de_84.png)

Luckily, we live in a world with computers, so repeating a simple task 1000 is as simple as articulating that task with a programming language.
