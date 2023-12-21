<h2 align="center"> How to forecast task completion time</h2>

 > In the process of writing. Will be updated.

 
Hello! My name is Kate Hongliang, and I am the head of the development process improvement department. In the article, I will talk about frequently used task estimation methodologies and whether they contain errors. Let's explore how to ask the right questions during estimation. We'll delve into what task resolution time represents, which is not always obvious. We'll attempt to change our mindset and discover a recipe for determining task resolution time.

If you ask any novice researcher in this field, "Why do we need estimation?" they will likely say that they are constantly asked, "When will you complete this task?" and estimation provides the answer to this question. But what if the question itself is incorrect?

## Let's rephrase the question.

"When will you complete this task?"—in psychology, such a question is considered open because it can have an infinite number of answers, and you would still be correct. However, would our client be satisfied with the answer "In 5 years"? In most cases, no.

From a mathematical perspective, an open question is one posed by a simple function T(x1, x2, x3, ..., xn), where xi represents the parameters of our system, including dependencies between tasks, the number of specialists, their experience, technical capabilities, and much more. T is the time to solve the task, the answer.

Solving such a function in mathematics is called solving the direct problem. Direct problems can only be solved in closed systems, where we can directly or indirectly know all values of xi.

In open systems, where the values of all xi are unknown, such a function cannot be solved and has multiple answers to the question.

For open systems, there is a method of searching for solutions, where we adjust the parameters to achieve the desired result of the function T. Knowing the set of parameters xi influencing the result, we can say that for this T, there are sets of values for xi that yield such a result.

In other words, let's ask the question differently: "Can we solve the task by a certain deadline?" This is a closed question with a definite answer and the result we are interested in. In mathematics, such a formulation is called an inverse problem because, to answer it, we specify the expected result of the function and need to explore the set of parameters that fit this answer to understand whether such a result is achievable or not.

To solve inverse problems in mathematics, numerical methods, probability theory, and statistics exist. Knowing the deadline by which we need to complete the task, we can, based on existing resources, determine whether it is possible to solve the task by that deadline and under what conditions.

Think about this and compare two questions: "When will you complete this task?" and "Can we solve the task by a certain deadline?" Which one is easier for you to answer?

Even if the answer to the question "Can we solve the task by a certain deadline?" is "No," using numerical methods, we can set another deadline for task completion and try to adjust the parameters for the new timeframe.

This method does not guarantee 100% adherence to deadlines but allows us to approximate the answer with known variables. The more information available about the task itself and its solving environment, the more chances there are to forecast an accurate answer.

Within this methodology, an amusing scenario can arise when, in response to the counter-question "When do you need it?" you might receive the client's answer "Yesterday!" And with a sense of relief, you can reply, "We're already late."

What is task resolution time?

To understand what time is, we need to consider that there is a certain service—a team—that we view as a black box. Tasks are input into this black box, and we receive results from it.

The customer requests specific tasks, and the team lead with the team says, "Yes, okay." From the moment the team commits to completing the task, we begin counting the time it takes for execution. When Katerina records the result that has been returned to her or delivered to the client, we will conclude the counting of this time. This can be visualized as follows:

> We end up with two time values. The difference between these points in date and time is referred to as Lead Time—the time it takes to complete the task.

If we gather the task resolution times over a certain period and mark points on a graph horizontally, representing the number of days spent on solving tasks, and vertically, representing the number of tasks solved in the same number of days, the distribution of Lead Time can be visualized on the graph:
<p align="center">
  <img src="https://i.imgur.com/AcvGFac.png" alt="Alt Text">
  </p>

  The graph helps understand that even similar tasks can take a different number of days to complete. A task that took us 3 days to complete yesterday might take longer today when we're in a different mindset, for example, 5 days. Various factors influence task completion. The graph shows that all tasks were resolved within 11 days, with a significant volume of tasks being completed in 8 days, although there is a possibility of completing tasks in just one day.
