# Numerical Method of  Disease Spread Using                                                     SIR Models
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

