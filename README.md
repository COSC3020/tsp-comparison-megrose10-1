# Traveling Salesperson Problem -- Empirical Analysis

For this exercise, you'll need to take the code from the TSP Held-Karp and TSP
Local Search exercises. This can be your own implementation or somebody else's.
You will now do an empirical analysis of the implementations, comparing their
performance. Both the Held-Karp and the Local Search algorithms solve the same
problem, but they do so in completely different ways. This results in different
solutions, and in different times required to get to the solution.

Investigate the implementations' empirical time complexity, i.e. how the runtime
increases as the input size increases. *Measure* this time by running the code
instead of reasoning from the asymptotic complexity (this is the empirical
part). Create inputs of different sizes and plot how the runtime scales (input
size on the $x$ axis, time on the $y$ axis). Your largest input should have a
runtime of *at least* an hour. The input size that gets you to an hour will
probably not be the same for the Held-Karp and Local Search implementations.

In addition to the measured runtime, plot the tour lengths obtained by both
implementations on the same input distance matrices. The length of the tour that
Held-Karp found should always be less than or equal to the tour length that
Local Search found. Why is this?

Add the code to run your experiments, graphs, and an explanation of what you did
to this markdown file.

I used my TSP Held Karp and Local Search algorithms for comparison. I also asked questions in class. I used https://www.geeksforgeeks.org/how-to-measure-time-taken-by-a-function-to-execute-using-javascript/ to find how to time each implementation, and also when it was harder to write out the distance matrix to test, I asked ChatGPT on how to generate a distance matrix to test since for local search, the distance matrix was large.

In the Held-Karp implementation, it always tries to find the best/shortest tour, while Local Search looks for a good tour using randomness and stops after reaching a certain point, not always finding the best/shortest tour. Looking at my graphs, we see no matter what input size is given to Local Search or Held-Karp, Held-Karp always finds the best tour, so local search can never return a better result, and will always either be equal or more than Held-Karp's best tour. While this may seem like a downside, if your goal is to be faster and you're not too worried with always getting the absolute best tour, Local Search is the way to go. You may be giving up the shortest tour overall, but you're saving time. Both implementations have their benefits, however, in the grand scheme of things, while you may get lucky with your randomization with local search, each implementation have their tradeoffs with either time or finding the best solution.
