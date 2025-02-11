This table combines the scenarios and hints into an easy reference for choosing the right statistical distribution for a given situation for a given Data Science Problem.

# Table: Distribution Types, Scenarios, and Hints

| Distribution | Type | Scenario 1 | Scenario 2 | Hint: When to Use |
|-------------|------|------------|------------|--------------------|
| **Bernoulli** | Discrete | A coin toss where heads = 1 (success) and tails = 0 (failure). | Checking if a machine works or fails during a single test. | Use for single trials with binary outcomes (success/failure). |
| **Binomial** | Discrete | Counting the number of defective items in a batch of 20 with a 5% defect probability. | Counting the number of customers who make a purchase out of 10 who enter a shop. | Use when counting number of successes in multiple independent trials with the same probability of success. |
| **Uniform (Discrete)** | Discrete | Rolling a fair 6-sided die and observing the outcome. | Randomly selecting a card from a shuffled deck of 52 cards. | Use when all outcomes in a range are equally likely and discrete (e.g., whole numbers). |
| **Uniform (Continuous)** | Continuous | Generating random waiting times uniformly between 2 and 5 minutes. | Randomly assigning a point in a 2D square field for simulation purposes. | Use when all outcomes in a range are equally likely and continuous (e.g., real numbers). |
| **Geometric** | Discrete | Counting the number of coin flips until the first head appears. | Measuring the number of emails sent before receiving a response from a recipient. | Use to model the number of trials needed to achieve the first success in repeated independent trials. |
| **Poisson** | Discrete | Counting the number of cars passing a checkpoint in a 10-minute interval. | Counting the number of customer arrivals at a store during a given hour. | Use when modeling the count of rare events that occur independently in a fixed interval of time or space. |
| **Normal** | Continuous | Modeling the heights of adults in a population. | Analyzing the distribution of students' exam scores in a class. | Use for naturally occurring continuous data that clusters around a mean (e.g., measurements, averages, errors). |
| **Exponential** | Continuous | Modeling the time until the next bus arrives at a bus stop. | Estimating the time between failures of a mechanical component. | Use when modeling time until the next event occurs in a Poisson process. |
| **Negative Binomial** | Discrete | Counting the number of failed attempts before a salesperson makes 5 successful sales. | Modeling the number of unsuccessful free throws before a basketball player makes 3 successful ones. | Use to model number of failures before achieving a fixed number of successes in repeated independent trials. |



## How to Use the Hints:

### Single Trials vs. Multiple Trials:
- Use **Bernoulli** for single trials with binary outcomes.
- Use **Binomial** for multiple trials where you’re counting successes.

### Equally Likely Outcomes:
- Use **Uniform** when all outcomes (discrete or continuous) are equally likely.

### Waiting for Success:
- Use **Geometric** when counting trials until the first success.
- Use **Negative Binomial** when counting failures until a specific number of successes.

### Event Occurrences:
- Use **Poisson** for rare events occurring in a fixed interval.
- Use **Exponential** for modeling the time between events in a Poisson process.

### Continuous Data:
- Use **Normal** for data that naturally clusters around a mean.

