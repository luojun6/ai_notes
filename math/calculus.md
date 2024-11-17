# Essence of calculus

## 1 The essence of calculus

**"The art of doing mathematics is finding that <span style="color:DodgerBlue">special case</span> that contains all the germs of generality." --- David Hilbert**

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

In the sprit of using what will come to be standard calculus notation, let's call that thickness $dr$ for a tiny difference in the radius from one ring to the next. Maybe you thinnk of it as something like 0.1.

![calculus_4.png](./images/calculus_4.png)

So approximating this unwrapped ring as a thin rectangle, its area is $2\pi r$ => $2\pi rdr$ -> the little thickness. And even though that's not perfect, for smaller and smaller choices of $dr$, this is actually going to be a better and better approximation for that area.

Since the top and the bottom of this shape are going to get closer and closer to being exactly the same length. So let's just move forward with the approximation.

Keeping in the back of our minds that it's slightly wrong, but it's going to become **more accurate for smaller and smaller choices of <span style="color:DodgerBlue">$dr$</span>**. That is, if we slice up the circle into thinner and thinner rings.

So just to sum up where we are, you've broken up the area of the circle into all of these rings, and you're approximating the area of each one of those as $2\pi rdr$, where the specific value for that inner radius ranges from $0$ for the smallest ring up to just under $3$ for the biggest ring, spaced out by whatever the thinkness is that you choose for $dr$, something like 0.1.

![calculus_5.png](./images/calculus_5.png)

And notice that the spacing between the values here corresponds to the thickness $dr$ of each ring, the difference in radius from one ring to the next.

In fact, a nice way to think about the rectangles approximating each ring's area is to fit them all upright side by side along this axis. Each one has a thickness %dr$, which is why they fit so snugly right there together, and the height of any one of these rectangles sitting above some specific value of $r$, like 0.6, is exactly $2\pi$ times that value $r$.

![calculus_6.png](./images/calculus_6.png)

That's the circumference of the corresponding ring that this rectangle approximates.

![calculus_7.png](./images/calculus_7.png)

Each of these rectangles ony approximates the area of the corresponding ring from the circle. For smaller and smaller choices of $dr$, you might at first think that turns the problem into a monstrously large sum. I mean, there's many many rectangles to consider, and the decimal precision of each one of their areas is going to be an absolute nightmare.

But notice, all of their areas in aggregate just looks like the area under a graph. and that portion under the graph is just a triangle, a triangle with a base of 3 and a height of that's $2\pi * 3$.

#### ![calculus_8.png](./images/calculus_8.png)

Or if the radius of our original circle was some other value **$R$**, that area comes out to be $\pi R^{2}$.

But if you want to think like a mathematician here, you don't just care about finding the answer, you care about developing general problem-solving tools and techniques.

You had this **hard problem** that could be approximated with the sum of many **small numbers/values**, each of wich looked like $2\pi dr$, for values of $r$ ranging between $0$ and $3$.

![calculus_9.png](./images/calculus_9.png)

Remember, the small number $dr$ here represents our choice for the thickness of each ring, and there are two important thinsg to note about <span style="color:DodgerBlue">**$dr$**</span>.

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

**"So far as te theories of mathematics are about <span style="color:DodgerBlue">reality</span>, they are not <span style="color:OliveDrab">certain</span>: so far as they are <span style="color:OliveDrab">certain<span>, they are not about <span style="color:DodgerBlue">reality</span>." --- Albert Einstein**

Goals:

1. Learn derivatives

- It's actaully a very subtle idea: The things is though, there's some subtlety to this topic, and a lot of potential for paradoxes if you're not careful.

2. Avoid paradox

- It's common for people to say tha the deivative measures an instantaneous rate of change, but when you think about it, that phrase is actually an </span sytle="color:FireBrick">oxymoron</span>.
- Chane is something that happens between separate points in time, when you blind yourself to all but just a singe instant, there is not really any room for change.

![calculus_17.png](./images/calculus_17.png)

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

That's what velocity is, it's the distance traveled per unit time.
