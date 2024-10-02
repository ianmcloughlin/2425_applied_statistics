# Applied Statistics

Applied Statistics runs from September to December 2024 at [ATU](https://www.atu.ie).
We will use [Python](https://docs.python.org/3/), [Jupyter](https://docs.jupyter.org/en/latest/) notebooks, and [GitHub](https://github.com/) throughout.

![A futuristic lecture.](img/lecture.jpeg)


## Assessment

**The deadline for all assessment elements is Friday, 20 December 2024.**

Submission instructions [are given below](#repository-20).

This assessment brief is available from the beginning of the semester. 
If anything is unclear, make sure to ask questions well before the deadline.

## Purpose

The purpose of the assessment is for you to demonstrate ability in the following.

1. Describe the stochastic nature of real-world measurements.

2. Source documentation to programmatically perform a statistical test.

3. Select an appropriate statistical test to investigate a claim.

4. Perform a statistical test on a data set.

The assessment consists of three overlapping parts: a GitHub repository containing all your work (20%), a series of tasks (40%), and a small project (40%).


## Feedback

Guidance on your expected progress will be provided during lectures.
At certain points during the semester, submitted repositories will be reviewed.
Feedback may be given individually, to the whole class, or both, depending on what is necessary.
To get the most benefit from the feedback, ensure you regularly commit and push your work to GitHub.

If you have any questions, ask them well in advance of the deadline.
Pay close attention to the marking scheme and the advice below.
They are based on feedback given to previous students in this and other modules.
You should treat it as a form of [feed-forward](https://www.qaa.ac.uk/docs/qaas/focus-on/a-student-guide-to-feedback-feedforward.pdf) to help you improve.


## Repository (20%)

Start by creating a new repository on [GitHub](https://github.com).
Include in it only work that is part of your submission.
Make sure your final submission is in the `main` branch, though you can use other branches for development.
Your grade will be based on the last commit made on or before the deadline.


### Submit Your Repository Info

**Immediately** submit your GitHub username and repository name using [this form](https://forms.office.com/e/kev0hd06GR). 
The form is only accessible through your ATU student account.  
You can find your username and repository name in the browser's address bar when viewing your repository on GitHub.
In the browser's location bar your will see something like `github.com/<username>/<repository_name>/`


### Organize Your Repository

Your work should be easy to showcase during a technical interview.
An interviewer should be able to understand and interact with your work without any assistance.
This will have a significant impact on your mark for this and other components.

To this end, make sure your repository is well-structured and includes:
  - A clear [README.md](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes).
  - A relevant [`.gitignore` file](https://github.com/github/gitignore).
  - [No unnecessary files or folders](https://realpython.com/python-git-github-intro/#what-not-to-add-to-a-git-repo).
  - Lowercase file and folder names, except for files like `README.md`.
  - No spaces or special characters in filenames. Underscores, hyphens, and full stops are okay.

### Private Repositories  

You can make your repository private.
If you do, add `ianmcloughlin` [as a collaborator](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository#inviting-a-collaborator-to-a-personal-repository).


### Choosing a GitHub Username  

Your GitHub username will be visible to potential employers.
Choose wisely.
You can use your real name, but a pseudonym is also fine if it’s reasonable.
Avoid using your student number.
You can [change your username by following the instructions on GitHub](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-user-account-settings/changing-your-github-username).



## Tasks (40%)

Complete all tasks in a notebook called `tasks.ipynb` in your repository.

For each task, you should write your code in code cells while using MarkDown cells to give explanations and insights into your code.
Break up your code into smaller, manageable cells whenever possible.
Each code cell should focus on a single step in your overall solution.

Include comments in all code cells to tell the reader what each statement does.
Write clean, readable, and efficient code, using meaningful variable names and consistent formatting.
You should follow Python coding standards and guidelines such as [PEP8](https://peps.python.org/pep-0008/).

Make regular commits to your repository while completing the tasks.
Your commit history should demonstrate how each solution to each task evolved.
There should be several commits for each task demonstrating incremental improvements, clarifications, and revisions.

### Task 1: Permutations and Combinations

Suppose we alter the Lady Tasting Tea experiment to involve twelve cups of tea.
Six have the milk in first and the other six having tea in first.
A person claims they have the special power of being able to tell whether the tea or the milk went into a cup first upon tasting it.
You agree to accept their claim if they can tell which of the six cups in your experiment had the milk in first.

Calculate, using Python, the probability that they select the correct six cups.
Here you should assume that they have no special powers in figuring it out, that they are just guessing.
Remember to show and justify your workings in code and MarkDown cells.

Suppose, now, you are willing to accept one error.
Once they select the six cups they think had the milk in first, you will give them the benefit of the doubt should they have selected at least five of the correct cups.
Calculate the probability, assuming they have no special powers, that the person makes at most one error.

Would you accept two errors? Explain.

### Task 2: numpy's Normal Distribution

In this task you will assess whether `numpy.random.normal()` properly generates normal values.
To begin, generate a sample of one hundred thousand values using the function with mean `10.0` and standard deviation `3.0`.

Use the `scipy.stats.shapiro()` function to test whether your sample came from a normal distribution.
Explain the results and output.

Plot a histogram of your values and plot the corresponding normal distribution probability density function on top of it.

### Task 3: t-Test Calculation

Consider the following dataset containing resting heart rates for patients before and after embarking on a two-week exercise program.

| Patient ID |  0 |  1 |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 |
|:-----------|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Before     | 63 | 68 | 70 | 64 | 74 | 67 | 70 | 57 | 66 | 65 |
| After      | 64 | 64 | 68 | 64 | 73 | 70 | 72 | 54 | 61 | 63 |

Calculate the t-statistic based on this data set, using Python.
Compare it to the value given by `scipy.stats`.
Explain your work and list any sources used.

### Task 4: ANOVA

In this test we will estimate the probability of committing a type II error in specific circumstances.
To begin, create a variable called `no_type_ii` and set it to `0`.

Now use a loop to perform the following test 10,000 times.

1. Use `numpy.random.normal` to generate three samples with 100 values each. Give each a standard deviation of `0.1`. Give the first sample a mean of `4.9`, the second a mean of `5.0`, and the third a mean of `5.1`. 

2. Perform one-way anova on the three samples and add `1` to `no_type_ii` whenever a type II error occurs.

Summarize and explain your results.


## Project (40%)

Complete the project in a single notebook called `project.ipynb` in your repository.
The same style should be used as detailed above: explanations in MarkDown and code comments, clean code, and regular commits.
Use plots as appropriate.

In this project, you will analyze the [PlantGrowth R dataset](https://vincentarelbundock.github.io/Rdatasets/csv/datasets/PlantGrowth.csv).
You will find [a short description](https://vincentarelbundock.github.io/Rdatasets/doc/datasets/PlantGrowth.html) of it on [Vicent Arel-Bundock's Rdatasets page](https://vincentarelbundock.github.io/Rdatasets/).
The dataset contains two main variables, a treatment group and the weight of plants within those groups.

Your task is to perform t-tests and ANOVA on this dataset while describing the dataset and explaining your work.
In doing this you should:

1. Download and save the dataset to your repository.

2. Describe the data set in your notebook.

3. Describe what a t-test is, how it works, and what the assumptions are.

3. Perform a t-test to determine whether there is a significant difference between the two treatment groups `trt1` and `trt2`.

4. Perform ANOVA to determine whether there is a significant difference between the three treatment groups `ctrl`, `trt1`, and `trt2`.

5. Explain why it is more appropriate to apply ANOVA rather than several t-tests when analyzing more than two groups.


## Marking Scheme

Each component will be graded based on the following four categories.
Each category carries equal weight.

Remember, your repository is what will be evaluated.
It should demonstrate evidence of the criteria outlined for each category.
That said, the examiners' overall impression of the submission may affect marks in each category.

You are expected to make steady progress on the assessment throughout the semester.
This should be reflected in your commit history.
Huge commits, especially late in the semester, will not be accepted.
At any stage you may be asked to discuss the work to date in your repository.

If you encounter issues with your repository, seek help well before the deadline.
Do not delete any files or commits without first consulting the lecturer.


### Research
 - Evidence of research on relevant topics.
 - Appropriate referencing.
 - Building upon the literature and documentation.
 - Comparisons to similar work.
  
### Development
 - Clear, concise, and correct code.
 - Appropriate tests.
 - Knowledge of different approaches and algorithms.
 - Clean architecture.
  
### Documentation
 - Clear explanations of concepts.
 - Concise comments in code and elsewhere.
 - Appropriate README for repository.
  
### Consistency
 - Tens of commits, each representing a reasonable amount of work.
 - Literature, documentation, and code evidencing work on the assessment.
 - Evidence of reviewing and refactoring.


## Advice

The freedom provided in open-style assessments such as this one can feel challenging.
You need to decide how to start, what content to include, how much to cover, and how to make the work your own. 

The assessment is designed to provide you with opportunities for independent thinking and decision-making.
Employers value graduates who can take initiative, work independently, and make design decisions with minimal guidance.
We expect you to have basic programming knowledge and be able to find information on your own.

You should have a clear plan before you start coding.
Your submission should include both your plan and an explanation of any design choices you made.

Make sure to follow ATU's policies and regulations which are on the [Student Hub](https://studenthub.atu.ie).
Pay particular attention to any policies on plagiarism and the Student Code.
If you're unsure about anything, ask the lecturer.