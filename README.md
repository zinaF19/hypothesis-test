# Hypothesis Testing

A hands-on introduction to hypothesis testing in Python. The guide notebook walks through the full testing workflow (hypotheses, test statistic, p-value, decision) for data following normal, binomial, and Poisson distributions, and links each test back to what you learnt about distributions and confidence intervals. An exercise notebook and an optional end-to-end guide let you practise the complete workflow on business case studies.

## Learning Objectives

By the end of this repository, you should be able to:

- State null and alternative hypotheses for a business question.
- Select the appropriate hypothesis test based on the data's distribution.
- Perform z-tests, proportion z-tests, and t-tests with scipy and statsmodels.
- Calculate p-values and use a significance level to reject or fail to reject the null hypothesis.
- Check normality with Q-Q plots and the Shapiro-Wilk test before choosing a test.
- Apply the full workflow from raw data to a tested, interpreted hypothesis.
- Test associations between numeric and categorical variable pairs during EDA, reporting effect sizes and avoiding the multiple-testing trap.

## Learning Path

| File / Folder | Description |
|---|---|
| [**1 - Hypothesis Testing Guide**](1_hypo_test_guide.ipynb) | Step-by-step tutorial: z-test on a normal sample, proportion z-test on binomial data, and an exact Poisson test, each as a worked case study. |
| [**2 - Hypothesis Testing Exercise**](2_hypo_testing_exercise.ipynb) | Two business case studies to solve on your own using the 7-step workflow, from data type to tested hypothesis. |
| [**3 - Combined Guide (Optional)**](3_combined_guide.ipynb) | End-to-end walkthroughs that bring distributions, confidence intervals, and hypothesis testing together, including normality checks with Q-Q plots and Shapiro-Wilk. |
| [**4 - Hypothesis Testing for EDA (Optional)**](4_hypothesis_testing_for_eda.ipynb) | Worked EDA session on the tips dataset: the matching test for each variable-pair type (correlation, t-test, ANOVA, chi-square) and the multiple-testing trap. |
| [**5 - Hypothesis Testing for EDA Exercise (Optional)**](5_hypothesis_testing_for_eda_exercise.ipynb) | Apply the pair-type recipe to NYC taxi rides on your own: five exercises including a data-recording artifact and a case where two tests disagree. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Solutions**](solutions/) | Reference solutions for the exercise notebooks. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it, including the `< >` brackets, with your own value. For example, `cd <repo-name>` becomes `cd my-hypothesis-testing`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

Documentation:

- [**scipy.stats reference**](https://docs.scipy.org/doc/scipy/reference/stats.html): Statistical tests and distributions used throughout the notebooks
- [**statsmodels proportions_ztest**](https://www.statsmodels.org/stable/generated/statsmodels.stats.proportion.proportions_ztest.html): The proportion z-test used in the binomial case study
- [**uv documentation**](https://docs.astral.sh/uv/): The package manager used in Setup

StatQuest videos:

- [**Hypothesis Testing and The Null Hypothesis, Clearly Explained!!!**](https://www.youtube.com/watch?v=0oc49DyA3hU): The core idea of hypothesis testing
- [**Alternative Hypotheses: Main Ideas!!!**](https://www.youtube.com/watch?v=5koKb5B_YWo): One-sided and two-sided alternatives
- [**p-values: What they are and how to interpret them**](https://www.youtube.com/watch?v=vemZtEM63GY): What a p-value does and does not tell you
- [**How to calculate p-values**](https://www.youtube.com/watch?v=JQc3yx0-Q9E): Where the number actually comes from
- [**P-hacking**](https://www.youtube.com/watch?v=HDCOUXE3HMM): How repeated testing produces false positives

Going further:

- [**ModernDive: Hypothesis Testing**](https://moderndive.com/v2/hypothesis-testing.html): A simulation-first treatment of the same ideas
- [**Think Stats**](https://greenteapress.com/thinkstats2/html/index.html): A free book applying these tests to real datasets in Python
- [**From Data to Viz**](https://www.data-to-viz.com/): Choosing the right chart when exploring a distribution before testing
