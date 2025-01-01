# Essence of calculus

## 1 The essence of calculus

**"The art of doing mathematics is finding that <span style="color:DodgerBlue">special case</span> that contains all the germs of generality." --- <span style="color:gold">David Hilbert</span>**

### 1.1 The Beginning Story

The story starts more simply, just you and a circle, let's say with radius 3. You're trying to figure out its area, and after going through a lof of paper trying different ways to chop up and rearrange the piecies of that area.

![calculus_0.png](./images/calculus_0.png)

Many of which might lead to their own interesting observations, maybe you try out the idea of slicing up the circle into many concentric rings. These should seem promising because it resprects the symmetry of the circle, and math has a tendency to reward you when you respect its symmetries.

![calculus_1.png](./images/calculus_1.png)

Let's take one of those rings, which has some inner radius $r$ that's between $0$ and $3$.

![calculus_2.png](./images/calculus_2.png)

If we can find a nice expression for the area of each ring like this one, and if we have a nice way to add them all up, it might lead us to an understanding of the full circle's area.

Maybe you start by imagining straightening out this ring. And you could try thinking through exactly what this new shape is and what its area should be, but for simplicity, leet's just approximate it as a rectangle.

The width of that rectangle is the circumference of the original ring, which is $2\pi r$. Then the thickness? Well, that depends on how finely you chopped up the circule in the first place, which was kind of arbitrary.

![calculus_3.png](./images/calculus_3.png)

### 1.2 The Small Chop $dr$

In the sprit of using what will come to be standard calculus notation, let's call that thickness $dr$ for a tiny difference in the radius from one ring to the next. Maybe you thinnk of it as something like 0.1.

![calculus_4.png](./images/calculus_4.png)

So approximating this unwrapped ring as a thin rectangle, its area is $2\pi r$ => $2\pi rdr$ -> the little thickness. And even though that's not perfect, for smaller and smaller choices of $dr$, this is actually going to be a better and better approximation for that area.

Since the top and the bottom of this shape are going to get closer and closer to being exactly the same length. So let's just move forward with the approximation.

Keeping in the back of our minds that it's slightly wrong, but it's going to become **more accurate for smaller and smaller choices of <span style="color:DodgerBlue">$dr$</span>**. That is, if we slice up the circle into thinner and thinner rings.

So just to sum up where we are, you've broken up the area of the circle into all of these rings, and you're approximating the area of each one of those as $2\pi rdr$, where the specific value for that inner radius ranges from $0$ for the smallest ring up to just under $3$ for the biggest ring, spaced out by whatever the thinkness is that you choose for $dr$, something like 0.1.

![calculus_5.png](./images/calculus_5.png)

And notice that the spacing between the values here corresponds to the thickness $dr$ of each ring, the difference in radius from one ring to the next.

### 1.3 The Rectangles Approximation

In fact, a nice way to think about the rectangles approximating each ring's area is to fit them all upright side by side along this axis. Each one has a thickness $dr$, which is why they fit so snugly right there together, and the height of any one of these rectangles sitting above some specific value of $r$, like 0.6, is exactly $2\pi$ times that value $r$.

![calculus_6.png](./images/calculus_6.png)

That's the circumference of the corresponding ring that this rectangle approximates.

![calculus_7.png](./images/calculus_7.png)

Each of these rectangles ony approximates the area of the corresponding ring from the circle. For smaller and smaller choices of $dr$, you might at first think that turns the problem into a monstrously large sum. I mean, there's many many rectangles to consider, and the decimal precision of each one of their areas is going to be an absolute nightmare.

But notice, all of their areas in aggregate just looks like the area under a graph. and that portion under the graph is just a triangle, a triangle with a base of 3 and a height of that's $2\pi * 3$.

#### ![calculus_8.png](./images/calculus_8.png)

Or if the radius of our original circle was some other value **$R$**, that area comes out to be $\pi R^{2}$.

But if you want to think like a mathematician here, you don't just care about finding the answer, you care about developing general problem-solving tools and techniques.

### 1.4 The Hard Problem

You had this **hard problem** that could be approximated with the sum of many **small numbers/values**, each of wich looked like $2\pi dr$, for values of $r$ ranging between $0$ and $3$.

![calculus_9.png](./images/calculus_9.png)

Remember, the small number $dr$ here represents our choice for the thickness of each ring, and there are two important thing to note about <span style="color:DodgerBlue">**$dr$**</span>.

first of all, not only is $dr$ a factor in the quantities we're adding up $2\pi dr$, it also gives the spacing between the different values of $r$.

Secondly, the smaller our choice for dr, the better the approximation. Adding all of those numbers could be seen in a different pretty clever way as adding the areas of many thin rectangles sitting underneath a graph, the graph of the function $2\pi r$ in [this case](#calculus_8png).

Then, this is key, by considering smaller and smaller choices for $dr$, corresponding to better and better approximations of the original problem, the sum, thought of as the aggregate area of those rectangles, approaches the **area under the graph**.

Because of that, you can conclude that the answer to the original question, is full unapproximated precision, is exactly the same as the area underneath thi graph.

A lot of other hard problems in math and science can be broken down and approximated as the sum of many small quantities, things like figuring out how far a car traveled based on its velocity at each point in time.

![calculus_10.png](./images/calculus_10.png)

In a case like that, you might range through many differnet points in time, and at each one multiply the velocity at that time times a tiny change in time, $dt$, which would give the corresponding little bit of distance traveled during that little time.

![calculus_11.png](./images/calculus_11.png)

If finer and finer approximations of the original problem corresponding to thinner and thinner rings, then the original problem is equivalent to finding the area under some graph.

The point now is that you, as the mathematician having just solved a problem by reframing it as the area under a graph, might start thinking about how to find the areas under other graphs.

### 1.5 What If Other Scenarios

We were lucky in the circle problem that the relevant area turned out to be a triangle, but imagine instead something like a parabola, the graph of $x^{2}$.

![calculus_12.png](./images/calculus_12.png)

We'll fix that left endpoint in place at 0, and let the right endpoint vary. Are you able to find a funciton, $A(x)$, that gives you the area under this parabola between 0 and x?

![calculus_13.png](./images/calculus_13.png)

A functiion $A(x)$ likes this is called an integral of $x^{2}$. Calculus holds within it the tools to figure out what an integral like this is. We know it gives the area under the graph of $x^{2}$ between some fixed left point and some variable right point, but we don't know what it is.

![calculus_14.png](./images/calculus_14.png)

This relationship between tiny changes to the mystery function and the values of $x^{2}$ itself is true at all inputs, not just 3. And any funciton defined as the area under some graph has this property.

![calculus_15.png](./images/calculus_15.png)

Here, we're stumbling into another big idea from calculus -> derivatives.

![calculus_16.png](./images/calculus_16.png)

## 2 The paradox of the derivative

**"So far as te theories of mathematics are about <span style="color:DodgerBlue">reality</span>, they are not <span style="color:OliveDrab">certain</span>: so far as they are <span style="color:OliveDrab">certain</span>, they are not about <span style="color:DodgerBlue">reality</span>." --- <span style="color:Gold">Albert Einstein</span>**

### 2.1 Goals

1. Learn derivatives

- It's actaully a very subtle idea: The things is though, there's some subtlety to this topic, and a lot of potential for paradoxes if you're not careful.

2. Avoid paradox

- It's common for people to say tha the deivative measures an instantaneous rate of change, but when you think about it, that phrase is actually an </span sytle="color:FireBrick">oxymoron</span>.
- Chane is something that happens between separate points in time, when you blind yourself to all but just a singe instant, there is not really any room for change.

![calculus_17.png](./images/calculus_17.png)

### 2.2 Understand the Challenge of Calculus Fathers

The instantaneous rate of change is actually nonsense, it makes you appreciate just how clear the father of calculus were in capturing the idea that phrase is meant to evoke, but with a perfectly sensible piece of math, the derivative.

![calculus_18.png](./images/calculus_18.png)

![calculus_19.png](./images/calculus_19.png)

![calculus_20.png](./images/calculus_20.png)

![calculus_21.png](./images/calculus_21.png)

If we were to plot the car's velocity in meters per second as a function of time $v(t)$, it might look like this bump.

![calculus_22.png](./images/calculus_22.png)

These two curves are definitely related to each other. If you change the specific distance vs fime function, you'll have some different velocity vs time function.

![calculus_23.png](./images/calculus_23.png)

![calculus_24.png](./images/calculus_24.png)

Exactly how does velocity depend on a distance vs time function? -> Think critically about what velocity means.

Be ware of that the velocity at a single moment makes no sense. If I show you a picture of a car, just a snapshot in an instant, and I ask you how fast it's going? You'd have no way of telling me.

What you'd need are two separate points in time to compare. That way you can compute whatever the change in distance acroos those times is, divided by the change in time.

![calculus_25.png](./images/calculus_25.png)

That's what velocity is, it's the distance traveled per unit time. We want to associate individual points in time with a velocity, but actually computing velocity requires comparing two separate points in time

![calculus_26.png](./images/calculus_26.png)

If that feels strange and paradoxical, good! You're grapping with the same conflicts that the fathers of calculus did. If you want a deep understanding for rates of change, not jsut for a moving car, but for all sorts of things in science, you're going to need to resolve this apparent paradox.

### 2.3 First, the Real World

Let's think about what the car's speedometer is probably doning.

![calculus_27.png](./images/calculus_27.png)

Graphically, you can imagine zooming in on some point of this distance vs the time graph above $t = 3$. That $dt$ is a small step to the right, since time is on the horizontal axis, and that $ds$ is the resulting change in the height of the graph, since the vertical axis represents the distance traveled.

![calculus_28.png](./images/calculus_28.png)

So $ds/dt$ is something you can think of as the rise over run slope between two very close point on this graph. We could apply this to any other point in time, so we consider this expression $ds/dt$ to be a function of t $f(t)$. Something where I can give you a tome $t$ and you can give me back the value of this ratio at that time, the velocity as a function of time.

![calculus_29.png](./images/calculus_29.png)

This idea of $ds/dt$, a tiny change in the value of the funciton s divided by the tiny change in the input that caused it, that's almost what a derivative is.

![calculus_30.png](./images/calculus_30.png)

Even though a car's speedometer will actually look at a concrete change in time, like 0.01 seconds, and even though the drawing program here is looking at an actual concrete change in time, in pure math the derivative is not this ratio $ds/dt$ for a specific choice of $dt$.

![calculus_31.png](./images/calculus_31.png)

Instead, it's whatever that ratio approaches as your choice for $dt$ approaches 0. Luckily there is a really nice visual understanding for what it means to ask what this ratio approaches.

### 2.4 Second, the Mathematics

![calculus_32.png](./images/calculus_32.png)

Remember, for any specific choice of $dt$, this ratio $ds/dt$ is the slope of a line passing through two separate points on the graph. As $dt$ approaches 0, and as those two points approach each other, the slope of the line approaches the slope of a line that's tangent to the graph at whatever point $t$ we're looking at.

![calculus_33.png](./images/calculus_33.png)

So the true honest-to-goodness pure math derivative is not the rise over run slope between two nearby points on the graph, it's equal to the slope of a line tangent to the graph at a single point.

Notice that I am not saying that whatever happens when $dt$ is infinitely small, whatever that would mean. Nor am I saying that you plug in 0 for $dt$.

This $dt$ is always a finite small non-zero value, it's just that it approaches 0 is all.

![calculus_34.png](./images/calculus_34.png)

It's healthiest for you to think of this slope not as some instantaneous rate of change, but instead as the **best constant approximation for a rate of change around the point**.

### 2.5 Using $d$ announces that $dt -> 0$

The convention in calculus is that whenever you're using the letter $d$ like $dt -> 0$, you're kind of announcing your intention that eventually you're going to see what happens as $dt$ approaches 0.

For example, the honest-to-goodness pure math derivative is written as $dt/dt$,
even though it's technically not a fraction per se.

![calculus_35.png](./images/calculus_35.png)

But whatever that fraction approaches for smaller and smaller nudges in $t$.

![calculus_36.png](./images/calculus_36.png)

### 2.6 An Eample

![calculus_37.png](./images/calculus_37.png)

![calculus_38.png](./images/calculus_38.png)

We could more generally say that the derivative of $t^{3}$ as a function of t is $3(t)^{2}$ => ${ds\over{dt}}(t) = 3(t)^2$.

Now take a step back, because that's beatiful. The derivative is this crazy complicated idea. We've got tiny changes in distance over tiny changes in time, but instead of looking at any specific one of those, we are talking about what that thing approaches.

In Practice, you wouldn't go through all this algebra each time. Knowing that the derivative of $t^{3} = 3t^{2}$ is one of those things that all calculus students learn how to do immediately without having to re-derive it each time.

### 2.7 "Instantaneous rate of change" -> Paradoxes

Think about the actual car traveling according to this $t^{3}$ distance function, and consider its motion at the moment $t=0$, right at the start. Now ask yourself whether or not the car is moving at that time.

![calculus_39.png](./images/calculus_39.png)

On the one hand, we can compute its speed at that point using the derivative, which for time $t=0$ works out to be 0. Visually, this means that the tangent line to the graph at that point is perfectly flat, so that car's quote-unquote intantaneous velocity is 0, and that suggests that obviously it's not moving.

On the other hand, if it doesn't start moving at time 0, when does it start moving? Is the car moving at the time 0? Do you see the paradox? The issue is that the question makes no sense.

**At time <span style="color:FireBrick">$t=0$</span>, is the car <span style="color:Gold">moving?</span>**

It references the idea of change in a moment, but that doesn't actually exist. That's just not what the derivative measures.

What it means for the derivative of a distance function to be 0 is that the **best constant approximation** for the car's velocity around that point is **$0{m\over{s}}$**.

![calculus_39.png](./images/calculus_39.png)

For example, if you look at an actual change in time, say between 0 and 0.1 seconds, the car does move. It moves 0.001m. That's very small, and importantly, it's very small compared to the change in time, giving an average speed of only $0.01{m\over{s}}$.

![calculus_40.png](./images/calculus_40.png)

Remember, what it means for the derivatiive of this motion to be 0 is that for smaller and smaller nudges in time, this ratio of meters per second approaches 0.

![calculus_41.png](./images/calculus_41.png)

But that's not to say tha the car is static. Approximating its movement with a constant velocity of 0 is, after all, just an **approximation**.

So whenever you hear people refer to th derivative as an instantaneous rate of change, a prhase which is intrinsically oxymoronic, I want you to think of that as a conceptural shorthand for the best constant approiimation for rate of change.

![calculus_42.png](./images/calculus_42.png)

## 3 Derivative formulas through geometry

**"You know, for a mathematician, he did not have enough <span style="color:DodgerBlue">imagination</spn>. But he has become a poet and now he is fine." --- <span style="color:Gold">David Hilbert</span>**

### 3.1 Start with $x^{2}$

What is the derivative of $x^{2}$? That is, if you were to look at some value x, and compare it to a value slightly bigger,just $dx$ bigger, what's the corresponding change in the value of the funciton --- $df$?

And in particular, what's $df/dx$, the rate at which this funciton is changing per unit change in $x$.

![calculus_43.png](./images/calculus_43.png)

As a first step for intuition, we know that you can think of this ratio $df/dx$ as the slope of a tangent line to the graph of $x^{2}$, and from that you can see that the slope generally increases as x increases.

At zero, the tangent line is flat, and the slope is zero.

![calculus_44.png](./images/calculus_44.png)

At $x = 1$, it's somehting a bit steeper. But looking at graphs isn't generally the best way to understand the precise formula for a derivative.

![calculus_45.png](./images/calculus_45.png)

For that, it's best to take a more literal look at what $x^{2}$ actually means, and in this case, let's go ahead and picture a square whos side lenght is $x$.

![calculus_46.png](./images/calculus_46.png)

If you increase $x$ by some tiny nugde, some little $dx$, what's the resulting change in the area of that square? That slight change in area is what $df$ means in the context. It's the tiny increase to the value of $f(x) = x^{2}$, caused by increasing $x$ by that tiny nudge $dx$.

![calculus_47.png](./images/calculus_47.png)

Now you can see that there's 3 new bits of area i this diagram, two thin rectangles and a minuscule square.

![calculus_51.png](./images/calculus_51.png)

- The two thin rectangles each have side lengths of $xdx$, so they account for $2xdx$ units of new area.
- The little square there has an area of $dx^{2}$, but you should think of that as being really tiny, negligibly tiny.
  - In principle, $dx$ should be thought of as a truly tiny amount, and for those truly tiny amounts, for these truly tiny amounts, a good rule of thumb is that you can ignore anything that includes a $dx$ raised a power greater than 1.
  - That is, a tiny change square is a negligible change.

**$df = 2xdx$ => ${df\over{dx}} = 2x$**

### 3.2 How about $x^{3}$

![calculus_48.png](./images/calculus_48.png)

Each of those thin squares has a volume of $x^{2}dx$, the area of the face times that little thickness $dx$. So in total this gives us $3x^{2}dx$ of volume change.

And to be sure there are other slivers of volume here along the edges, and that tiny one in the corner left-up, but all of that volume is going to be proportional to $dx^{2}$, so we can safely ignore them.

What that means in terms of graphical intuition is that the slope of the graph of $x^{3}$ at every signle point $x$ is exactly $3x^{2}$.

![calculus_49.png](./images/calculus_49.png)

Reasoning about that slope, it should make sense that in this derivative is high on the left and then $0$ at theo orgin and then high again as you move to the right.

### 3.3 Abstract the Rules

![calculus_50.png](./images/calculus_50.png)

WHen you nudge that input $x$, increasing it slightly to $(x + dx)^{n}$, working out the exact value of that nudged output would involve multiplying togther these n separate $(x + dx)$ terms.

The full expansion would be really complicated, but part of the point of derivatives is that most of that complication can be ignored.

![calculus_52.png](./images/calculus_52.png)

The first term in your expansion is $x^{n}$. This analogous to the area of the original square, or the volume of the original cube from our previous examples.

For the next terms in the expansion you can choose mostly $x$s with a single $dx$. Since there are n different parentheticals from which you could have chosen that single $dx$, this gives us a separate terms,

![calculus_53.png](./images/calculus_53.png)

![calculus_54.png](./images/calculus_54.png)

THis is analogous to how the majority of the new area in the square came from those two bars, each with area $x$ times $dx$, or how the bulk of the new values in the **cube**.

![calculus_55.png](./images/calculus_55.png)

### 3.4 $f(x) = 1\over{x}$

Now on the hand you could just blindly try applying the power rule as $x^{-1} = -1x^{-2}$. Let's have some fun and see if we can reason about this geometrically, rather than just plugging it through some formula.

The value $1\over{x}$ is asking what number multiplied by x eqauls 1?
![calculus_56.png](./images/calculus_56.png)

Imagine a little rectangle puddle of water sitting in two dimensions whose area is 1. Let's say that its width is x, whch means that the height has to be $1\over{x}$, since the total area of it is 1.

![calculus_57.png](./images/calculus_57.png)

If you increased x up to 3, then the other side has to be squished down to $1\over{3}$.

![calculus_58.png](./images/calculus_58.png)

If you think of this width x of the puddle as being in the xy-plane, then the corresponding output $1\over{x}$, the height of the graph above that point, is whatever the height of your puddle has to be maintain an areaa of 1.

![calculus_59.png](./images/calculus_59.png)

So with this visual in mind, for the derivative, imagine nudging up that value of x by some tiny amount, some tiny $dx$. How must the height of this rectangle change so that the area of the puddle remains constant at 1?

That is, increasing the width by $dx$ adds some new area of the right here. So the puddle has to decrease in height by some $d({1\over{x}})$, so that the area lost off of that top cancels out the area gained.

![calculus_60.png](./images/calculus_60.png)

### 3.5 $sin(\theta)$

![calculus_62.png](./images/calculus_62.png)

![calculus_61.png](./images/calculus_61.png)

## 4 Visualizing the chain rule and product rule

**"Using the chain rule is like peeling an onion: you have to deal with each layer at a time, and if it is too big you will start crying." --- <span style="color:Gold">(Anonymous professor)</span>**

### 4.1 Sum: ${d\over{dx}}(sin(x) + x^{2})$

![calculus_63.png](./images/calculus_63.png)

![calculus_64.png](./images/calculus_64.png)

![calculus_65.png](./images/calculus_65.png)

### 4.2 Product: ${d\over{dx}}(sin(x)x^{2})$

**<span style="color:MediumPurple">Not the best visualization</span>**

If you're dealing with a product of two things, it helps to understand it as some kind of area. In this case, maybe you try to configure some metal setup of a box where the side lengths are $sin(x)$ and $x^{2}$.

Since these are functions, you might think of those sides are adjustable, dependent on the value ofx, which maybe you think of as this number that you can just freely adjust up and down.

Focus on that top side who changes as the function of $sin(x)$. As you change this value of x up from 9, it increases up to a length of 1 as sine of x moves up towards its peak.

![calculus_66.png](./images/calculus_66.png)

And after that it starts to decreas as $sin(x)$ comes down from 1. In the same way, that height there is always changing as $x^{2}$.

![calculus_67.png](./images/calculus_67.png)

So $f(x)$, defined as the product of these functions, is the area of this box. The nedge $dx$ caused that width to change by some small $dsine(x)$, and it caused that height to change by some $dx^{2}$.

![calculus_68.png](./images/calculus_68.png)

This gives us three little snippets of new area:

- A thin rectangle on the bottom whose area is its width - $sin(x)$ => $sin(x)d(x^{2})$
- A thin rectangle on the right whose area is its height $x^{2}$ => $x^{2}d(sin(x))$
- The little bit in the corner, but we can ignore that. Its area is ultimately proportional to $d(x^{2})$ that becomes negligibe as $dx$ goes to 0.

![calculus_69.png](./images/calculus_69.png)

![calculus_70.png](./images/calculus_70.png)

### 4.3 Composition: ${d\over{dx}}(sin(x^{2}))$

![calculus_71.png](./images/calculus_71.png)

![calculus_72.png](./images/calculus_72.png)

![calculus_73.png](./images/calculus_73.png)

![calculus_74.png](./images/calculus_74.png)

![calculus_75.png](./images/calculus_75.png)

![calculus_76.png](./images/calculus_76.png)

The cancellation of $dh$ is not just a notation trick! That is a genuine reflection of what's going on with the tiny nudges that underpin everything we do derivatives.

![calculus_77.png](./images/calculus_77.png)
