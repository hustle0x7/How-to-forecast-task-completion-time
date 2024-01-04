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

 ## Predicting task completion times is challenging. Many researchers have attempted to answer the question, "When will tasks be completed?"

Forecasting is difficult, and it's important to acknowledge this fact. Regardless of the approach we try, it is a complex cognitive process that has engaged the minds of many, including Daniel Kahneman, Troy Magennis, Dmitry Bakardzhiev, Stephen McConnell, and others. Numerous books have been dedicated to evaluating intellectual work.

We are not alone, and if we make mistakes in our predictions, it's normal; those who came before us also made errors.

One of the most popular inventions for the IT industry is the use of Story Points for estimation. Ron Jeffries proposed them as an alternative to precise time estimation demanded by managers. Ron devised them for the development process in a framework called XP, and somehow they transitioned into Scrum. Later, he wrote an article apologizing for his invention.

Let's consider examples from two researchers, Mike Cohn and Ajay Reddy, to understand that estimating task completion time is indeed not straightforward.

**The first example** involves Mike Cohn actively promoting an estimation methodology based on Story Points, recommended for assessing tasks and determining their resolution timelines. I'll provide an example from his old book, "Agile Estimating and Planning." To explain the connection between Story Points and task completion time, he suggested the following approach:

<p align="center">
  <img src="https://i.imgur.com/Uhihs89.png" alt="Alt Text">
  </p>

  To verify this claim, we can construct such a graph based on the Lead Time distribution for our teams using Story Points. In our company, we conducted this experiment, and here are the results:

  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/de2/f0f/668/de2f0f668ea8aae52800ac5993295664.png" alt="Alt Text">
  </p>
  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/a02/015/cf0/a02015cf0826b18dca391fc97c522983.png" alt="Alt Text">
  </p>
  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/ae9/5d0/a20/ae95d0a20f8c3c9dd2441cbedf0d026b.png" alt="Alt Text">
  </p>
  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/184/fe2/ad7/184fe2ad79c19abcec76a77d0dc9c3fc.png" alt="Alt Text">
  </p>
In a simple version, we can represent these distributions in one of the forms of the Weibull distribution, as illustrated in the example with the yellow graph:

  <p align="center">
  <img src="https://i.imgur.com/WlMUZRa.png" alt="Alt Text">
  </p>

  As seen from the distribution graphs for Story Points 1, 2, 3, 5, the actual Lead Time, firstly, does not follow a normal distribution pattern as depicted in Mike's book. Secondly, the distribution of Lead Time for tasks with different Story Point estimates appears very similar. In other words, tasks with different Story Point estimates were completed in roughly the same amount of time with minor variations.

I conducted a similar experiment across different teams and found no significant correlation between Story Points estimates and task resolution time.

The question arises: Was Mike Cohn correct?

The unequivocal answer is no. He made a mistake.

**The second example** is Ajay Reddy's approach. He tackled the problem from a different angle in his book "Scrumban [R]Evolution, The: Getting the Most Out of Agile, Scrum, and Lean Kanban (Agile Software Development Series)."

Ajay attempted to create a correlation graph between Story Points and task resolution time to find an optimal formula for Story Points.

  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/5e3/9c5/ad2/5e39c5ad2abe075a0d5468ab02a7dc63.png" alt="Alt Text">
  </p>

  Within this experiment, Ajay Reddy sought to find which Story Points estimate aligns better with task resolution time. Through the experiment, he identified that using estimates as powers of two results in a more linear correlation, if one exists.

We have constructed graphs for several teams (services) utilizing Story Points for estimation and found a typical pattern:

  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/762/bcd/97a/762bcd97aad0b8f8a7cbde837733803f.png" alt="Alt Text">
  </p>

  The question arises: how did Ajay conduct his experiment that resulted in some correlation, while we found no correlation at all?

The answer: it's possible that it was an experiment with result fitting or a specific case where correlation appeared.

You are right to question my conclusions. Predictive estimation, as an assessment without feedback based on results analyzed statistically, makes little sense for forecasting timelines. Even in experiments conducted in a gamified form, one can discover that the correlation between task completion time and Story Points estimates or person-hours, or similar methods referred to as predictive estimation, is practically negligible.

One such game we conducted as a workshop together with Evgeny Stepchenko at the Flow Days conference in 2022. It's called NoEstimate. You might try running this workshop to gain a better understanding of the topic.

**Conclusion:** forecasting is challenging, and simple methods for determining task completion time in an intellectual environment may only work as an exception rather than a well-established technique.

## Why tasks are solved differently?

Understanding this question is aided by Dave Snowden and his Cynefin framework. He divides the domain of action into several domains. Depending on the domain, decision-making methodologies for systems, situations, and tasks will differ. One of Dave's main discoveries is the systematization of different types of environments in which your system operates. Different methods of influence and management should be applied in these environments. Dave identifies five main domains: Simple, Complicated, Complex, Chaos, and Confusion.

The framework requires a separate article for a detailed description, so I'll only note that in the realm of intellectual work, we encounter different situations and environments, often dealing with environments in a transitional form. While most project and task assessment methods work well when associated with the Simple and sometimes Complicated domains, many cases require addressing issues in the Complex and Chaos domains.

The same framework suggests trying to understand the situation you are in and transitioning from the Chaos domain to the Simple domain, using methods from the discipline called "Change Management" to simplify the system, including management, and reduce costs by reducing risks.

Another interesting problem is that people tend to simplify the causes of problems and solution methods while making decisions based on their current state, including emotional states. This hinders both a sober assessment of tasks and the erroneous decision-making based on irrelevant experiences. These problems are well discussed in the book "Thinking, Fast and Slow" by Daniel Kahneman.

The complexity of predicting tasks is often explained in a more straightforward way. Imagine that Vasily estimated the task and was in a good mood when he said he would complete it in two hours. However, Peter will start working on the task in a bad mood two weeks after the forecast. After Peter's actions, Katherine will work on the task, determining the quality of the solution. Moreover, the task will wait for the completion of other tasks that Katherine worked on.

How can Vasily's estimate affect the actual completion time? And we haven't even considered that the task estimated by Vasily may be blocked by a solution from another team. Also, Vasily did not anticipate that it would be blocked at the time of forecasting.

## Why Tasks Are Solved Differently

Understanding this question will benefit us with Dave Snowden and his Cynefin framework. He divides the domain of action into several domains. Depending on the domain, decision-making methodologies for systems, situations, and tasks will differ.

One of Dave's key discoveries is the systematization of different types of environments in which your system operates. Different environments require different methods of influence and management. Dave identifies five main domains: Simple, Complicated, Complex, Chaos, and Confusion.

Describing the framework requires a separate article, so I'll just note that within intellectual work, we often encounter different situations and environments, quite frequently in a transitional form. Most project evaluation and task methods work well when associated with the Simple and sometimes Complicated domains. However, many times, tasks need to be solved in the realm of Complex, Complicated, and sometimes Chaos.

The framework suggests trying to understand your situation and moving from Chaos to Simple using change management methods to simplify the system, including management and cost reduction by reducing risks.

Another interesting problem is that people tend to simplify the causes of problems and methods of solving them while making decisions based on their current state, including emotional state, hindering both a sober assessment of tasks and making mistaken decisions based on irrelevant experience. Daniel Kahneman's book "Thinking, Fast and Slow" delves into such problems.

Often, the complexity of forecasting tasks is explained by a simpler way. Imagine Vasily estimated the task, and he was in a good mood when he said he would complete it in two hours. Peter will start working on the task two weeks after the forecast in a bad mood. After Peter's actions, Catherine will work on the task, determining the quality of the solution, and the task will also wait for the completion of other tasks that Catherine worked on.

How can Vasily's estimate affect the actual completion time? And we haven't even considered that the task estimated by Vasily could be blocked by a solution from another team. Moreover, Vasily did not anticipate that it would be blocked at the time of forecasting.

**Conclusion:** To make forecasts, you first need to determine the situation, the system, the domain in which your system is located. You are almost always in the domain of dealing with risks. To answer the question "When will you complete this task?" we need more information about how the system works as a whole in its environment.

Is it possible to build a system where forecasts can be made with a high degree of accuracy?

Conclusion. To make forecasts, you first need to determine in which situation, system, or domain your system is located. You are almost always in the area of working with risks. To answer the question "When will you complete this task?" we need more information about how the system operates as a whole in its environment.

Is it possible to build a system where accurate forecasts can be given with a high degree of accuracy?

## How to build a system to consistently meet deadlines?

The process of creating value in IT can be divided into two main stages:

1. **Upstream**: The process of selecting and analyzing tasks that we want to implement.
2. **Downstream**: The process of developing and delivering value to the client or customer.

It is essential to build and improve any system starting from the end of the process.

Let's focus on Downstream. The Downstream process is managed either by the teams themselves or team leads, sometimes technical leaders.

To establish a process with a predictable deadline for Downstream, the main rule is to impose a limitation on the concurrently tackled work. Techniques such as WIP limits, CONWIP limits can help with this, and if the team is working on different types of tasks, the Capacity Allocation technique can be beneficial.

> For those using Story Points or hour estimation, the WIP limits technique may seem counterintuitive, especially when dealing with tasks of varying complexity. The real challenge lies in understanding that a Sprint is not just a two-week iteration where we pick various tasks. Instead, it is a period during which the entire team collaboratively tackles one goal, referred to as the sprint goal. In many cases, the Sprint process is not necessary for organizations, as both this tool and Scrum itself are highly contextual and closely tied to the Complex domain (per Cynefin). Recommending the game Featureban can enhance understanding of how WIP limits function."

By setting constraints on development, the Downstream process will involve selecting tasks that progress at different speeds due to varying risks and types of work. The limitation on concurrently executed work itself will balance the team's focus.

  <p align="center">
  <img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/024/64c/990/02464c990247457f1ab0482ad48ec34f.png" alt="Alt Text">
  </p>
  <p align="center">
  Over time, the team will achieve a balance in the work taken on, ensuring an even mix of complex, long-term tasks and relatively simple, quick tasks. This will result in a consistent delivery of completed work and positively impact overall task resolution times.
  </p>

 The goal of these activities is to determine the natural constraint on the number of tasks being concurrently addressed in the system for all types, enabling its use in planning.

Key insights into building the Downstream process have been eloquently explained by Alexey Pimenov in his presentation "Harry Team Leads and Modern Management."

**Now, let's focus on the Upstream process.** Project Managers or Product Owners typically oversee this process, answering the question "What exactly needs to be done?"

> Many stages of the Upstream process often hide behind a single term – Backlog. The use of the term Backlog can serve as an indicator of how well the Upstream process is structured. If you find yourself using the term Backlog, there may be room for improvement.

Common problems associated with Upstream include:

1. Lack of dedicated task screening stages — no defined rule funnel.
2. Development tasks can be taken from any stage by elevating their priority.
3. Absence of analysis regarding the risks transferred from Upstream to Downstream when priorities change and task screening rules are violated.

A robust Upstream is built using a "rule funnel" to ensure that the number of tasks reaching Downstream is comparable to what Downstream can process. With knowledge of Downstream limitations, we can determine the quantity of tasks to prepare for work. Hence, the formulation of task screening rules from Upstream should retain only those tasks that can be implemented and those needed in the near future. Anything else is discarded.

The role of Upstream is to minimize risks that may pass into the Downstream process. At each stage of Upstream, a set of rules should be in place to mitigate the risk of a task not being completed. For instance, the Definition of Ready – rules formulated in the last stage before Downstream, where we can check for dependencies and ensure clear task formulation.


