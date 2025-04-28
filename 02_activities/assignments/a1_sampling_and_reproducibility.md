# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author:Ezinneifechukwunyelu Ndubueze

```
1. Sampling 1 : Infection 
Sampling procedure : random selection 
Function used: np.random.choice
Sample size: 10% of 1000 = 100
Sampling frame:800+200=1000(entire population)
Distribution: uniform 
Relationship to the article: this is setting the  the number of infected people using the iinfection rate 

2. Sampling 2: Primary Contact Tracing 
Sampling procedure : random selection 
Function used: np.random.rand
Sample size: <20% of 100 (20 people)
Sampling frame:only infected people(100)
Distribution : Bernoulli
Relationship to the article: this is setting the  the number of infected people who can be contact traced from the infected population

3.Sampling 3: Secondary contact tracing 
Sampling procedure : stratified sampling with wedding and brunch as two stratas
Function used: N/A
Sample size: 2
Sampling frame: only infected people(100)
Distribution : not sure what type of distribution, but it will be 2 points for the 2 infected people selected for tracing
Relationship to the article: random selection of 2 infected people to see if they are traced to the same event


4. code does not reproduce the graph in the post

5. result are not reproduciable. varies with every run

6. To make code reproduciable, set a seed at the beginning of the code using np.random.seed.
seed set to 1515 in code

## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
