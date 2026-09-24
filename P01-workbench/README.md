# Practical 01 --- Your MLOps Workbench

*A clean environment, a pinned library list, and a run that repeats itself*

SCSE3040 Machine Learning Operations · Bennett University · Session 2026-27

| | |
|---|---|
| Follows lectures | L01-L02 |
| Course Outcome | CO1 |
| Duration | 120 minutes |
| Peak memory | ~250 MB |
| Extra software | nothing beyond the course venv |
| Marks | 10 |

## Aim

1. Find out which Python is actually running your code.
2. Write down the exact library versions your project needs.
3. Make a program that gives the same answer every single time.
4. Save your work in git with a proper first commit.

## Before you start

- The course virtual environment is installed. If not, follow `labs/SETUP.md` first.
- You have opened this notebook from inside the `labs/P01-workbench/` folder.
- Nothing else. This is the first practical of the course.

## Background


**MLOps** (Machine Learning Operations) is the work of taking a model out of a
notebook and keeping it running for real users. Almost every problem in that
job comes from one sentence: *"but it works on my machine"*.

It works on your machine because your machine has a particular Python, with
particular libraries, at particular versions. Your friend's machine has
different ones. The server has different ones again. The same code then gives
a different answer, or no answer at all.

Professionals solve this in three steps, and today you will do all three.

1. **A virtual environment.** A private folder holding one Python and one set
   of libraries, used by one project only. Installing something for this course
   then cannot break another project on the same laptop.
2. **A pinned requirements file.** A plain text list saying *exactly* which
   version of each library you used --- `numpy==2.5.1`, not just `numpy`.
   Anybody can then rebuild your environment.
3. **A seed.** Machine learning uses random numbers: which rows go into
   training, where a model starts. Random means *different every run*, which
   means results you cannot check. Fixing the **seed** makes the randomness
   repeat, so your result can be checked by someone else.

Together these give you **reproducibility**: same code plus same data plus same
versions gives the same answer, on any machine, on any day. Everything else in
this course is built on top of that.


## What you will do

1. **Which Python is running this notebook?**
2. **What is installed in this environment?**
3. **Freeze those versions into requirements.txt**
4. **Random numbers change every time you ask**
5. **A seed makes the randomness repeat**
6. **Build the delivery dataset, twice**
7. **Look at the data you just made**
8. **Record what you ran**
9. **Save your work in git**

## Your turn

- **T1 --- Change the seed.** The dataset was built with seed **42**. Build it with seed **7**
- **T2 --- Write your own pinned requirements file.** Write a file `work/my_requirements.txt` containing exactly three lines,
- **T3 --- Fingerprint a run.** Write a function `fingerprint(path)` that takes the path of a CSV file

## What to submit

1. This notebook, with every cell run and its output visible.
2. The file `work/my_requirements.txt` that you wrote in Task T2.
3. A screenshot of the output of the last walkthrough cell (`git log`).

## Marking

| What is marked | Marks |
|---|---|
| Walkthrough run end to end, outputs visible | 3 |
| Task T1 --- seeds control randomness | 2 |
| Task T2 --- a correctly pinned requirements file | 2 |
| Task T3 --- a working fingerprint function | 3 |
| **Total** | **10** |

## Read more

- Python docs --- Virtual environments and packages --- <https://docs.python.org/3/tutorial/venv.html>
- pip --- Requirements files --- <https://pip.pypa.io/en/stable/reference/requirements-file-format/>
- NumPy --- Random generator and seeds --- <https://numpy.org/doc/stable/reference/random/generator.html>
- Pro Git --- Getting started --- <https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup>

---

*Open `P01.ipynb` in Jupyter and work through it top to bottom.
The notebook contains everything in this handout, plus the code.*

I used ChatGPT (OpenAI) as an AI assistance tool while working on this assignment. It was used for understanding the assignment requirements, clarifying concepts, discussing implementation approaches, and debugging/explaining code.
