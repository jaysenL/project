# Numerical Method of  Disease Spread Using                                                     SIR Models
FOR PEER REVIEW 
# SIR Model Simulation Using Euler and RK4 Methods

## Project Description

This project models the spread of an infectious disease using the SIR (Susceptible-Infected-Recovered) model.

The population is divided into three groups:

- S(t): susceptible individuals
- I(t): infected individuals
- R(t): recovered individuals

The model uses a system of ordinary differential equations (ODEs) to describe how disease spreads through a population over time.

The project compares two numerical methods for solving the SIR system:

1. Euler’s Method
2. Fourth Order Runge-Kutta Method (RK4)

The goal is to compare the accuracy and behavior of Euler’s method and RK4 using different time step sizes.

---

# Mathematical Model

The SIR model is defined by:

dS/dt = -β(SI/N)

dI/dt = β(SI/N) - γI

dR/dt = γI

Where:

- β = infection rate
- γ = recovery rate
- N = total population

The total population is assumed constant:

N = S + I + R

---

# Methods Used

This project uses:

- Python
- NumPy
- Matplotlib

Numerical methods implemented:

- Euler’s Method
- RK4 (Runge-Kutta Fourth Order Method)

The program simulates disease spread and generates plots showing:

- susceptible population over time
- infected population over time
- recovered population over time
- comparison between Euler and RK4

---

# Repository Organization

Important files:

| File | Description |
|------|-------------|
| `simulation.ipynb` | Main Jupyter Notebook containing all project code |
| `README.md` | Project description and instructions |

If using separate Python files:

| File | Description |
|------|-------------|
| `sir_model.py` | Defines SIR differential equations |
| `euler_solver.py` | Euler numerical solver |
| `rk4_solver.py` | RK4 numerical solver |
| `simulation.py` | Runs simulations and generates plots |

TO RUN CODE 
How to Run the Code
Option 1: Jupyter Notebook

Open:

simulation.ipynb

Run all cells.

Option 2: Python Script

Run:

python simulation.py










The project I am doing is trying to focus on showing with code the spread of an infectious disease using the SIR model which stands for (susceptible, infected, recovered). The SIR model is a model using ordinary differential equations that describes how people move between three areas when it comes to how certain diseases are tracked for a population and that is people who are  susceptible, infected, and recovered.
I will use numerical methods like Euler’s Method and classical four order rule or (RK4) to solve these equations and compare both of them to see if they are accurate and stable. The goal is to see how different areas of the project like infection rate and recovery rate affect disease and how  the results would look through the graphs.
Project Plan & Timeline
Week 1 (Now)
Create GitHub repository
Research SIR model and equations
Set up project structure
Week 2
Use the SIR model equations
Code Euler method solver
Week 3
Use (RK4) solver
Compare Euler vs RK4 results
Week 4
Add graphs (plots of S, I, R over time)
Test different areas
Week 5
Show results and write explanations
Have code and documentation
Final Week
Finalize README and results
Clean up repository
Resources
Course notes on numerical methods
Python libraries: NumPy, Matplotlib andSciPy 
Reach Goals
Use real world data COVID case data
Use more advanced models (SEIR model with exposed group)


sir-disease-model/
│
├── README.md              
├── requirements.txt      
│                  
│  ── sir_model.py       # Defines SIR differential equations
│  ── euler_solver.py    
│  ── rk4_solver.py      
│  ── simulation.py      # Runs both methods
│
├── data               
│   ── covid_data.csv     # Real-world data (for reach goal)
│
├── results               
│   ── plots            
│   ── comparisons       # Euler vs RK4 comparison results  
│
└── docs                  
    ── report.md          


Updated readme aka projecy updatepart 2 
At this point in my project I am on track with my timeline. I have created the GitHub repository and put the SIR model equations into the files. I have written the functions defining the system of differential equations for the SIR model and finished the initial Euler’s method. I have also started using the RK4 solver and setting up sims to compare both methods.

One challenge I had was correctly putting the number solvers so they could be used later for different values and conditions. At first my numbers were too narrow and caused issues when trying to test different situations. I affixed this by changing the code into functions that can use the parameters infection rate (β), recovery rate (γ) and initial population values.

Another challenge I have was making sure my numbers  particularly with Euler’s method were good when using larger times. This had me go back to course materials to better understand it. When going back and realizing the mistakes I had made I fixed them to allow flexible time to compare results.There have been not many changes to my original plan. I decided to first build a better sim than before so that adding stuff like plotting will be easier later. 

Next Path 

I am currently on track. First, I will complete the RK4 solver by comparing its results to Euler’s method. I will test different times (for example, h=0.1h = 0.1h=0.1 and h=0.01h = 0.01h=0.01) to see how accuracy changes between the two methods.

Next I will run sims using the same initial conditions values for both Euler and RK4 methods. I will compare the results by looking at infection levels and how quickly the disease spreads.

After running the simulations, I will make plots of the susceptible, infected and recovered populations over time. 

Finally I will write the results by seeing the differences between Euler’s method and RK4

Methods Draft (Jupyter)

Problem Setup
The goal of this project is to model the spread of an infectious disease using the SIR model. The population is divided into three parts

S(t) number of susceptible individuals

 I(t) number of infected individuals

R(t) number of recovered individuals

The total population is assumed constant:
N = S(t) + I(t) + R(t)

The system is governed by the following ordinary differential equations:
dS/dt = -β(SI / N)

dI/dt = β(SI / N) - γI

dR/dt = γI

Where:

( beta ) is the infection rate

( gamma ) is the recovery rate

Initial Conditions:
S(0) = S₀,

 I(0) = I₀

R(0) = 0

S(0) = 990

I(0) = 10

R(0) = 0

β = 0.3

γ = 0.1

h = 0.1

0 ≤ t ≤ 100


Assumptions:

Closed population (no births or deaths)

non selective mixing (each individual is equally likely to see each other and get infected)


Euler’s Method
Euler’s method approximates solutions using:

yₙ₊₁ = yₙ + h f(tₙ, yₙ)

Used in SIR system:

Sₙ₊₁ = Sₙ − hβ (SₙIₙ / N)

Iₙ₊₁ = Iₙ + h [β (SₙIₙ / N) − γIₙ]

Rₙ₊₁ = Rₙ + hγIₙ

where h is the time step.

Runge-Kutta Method (RK4)
RK4 improves the answers

yₙ₊₁ = yₙ + (h/6)(k₁ + 2k₂ + 2k₃ + k₄)

k₁ = f(tₙ, yₙ)

k₂ = f(tₙ + h/2, yₙ + (h/2)k₁)

k₃ = f(tₙ + h/2, yₙ + (h/2)k₂)

k₄ = f(tₙ + h, yₙ + hk₃)

This method will be applied to all three equations.


Plan
Define SIR system in sir model

Use  Euler solver in euler

Use RK4 solver in rk4 

Use sim py to run both methods, compare and generate plots


