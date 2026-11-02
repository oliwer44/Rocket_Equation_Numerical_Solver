# Rocket Equation Numerical Solver

A Python project that numerically solves and visualizes the velocity profile of a rocket over time based on Tsiolkovsky's Rocket Equation using SciPy's Initial Value Problem solver (`solve_ivp`).

## 📌 Features

* **Numerical Integration:** Solves the continuous differential motion of a rocket using `scipy.integrate.solve_ivp`.
* **Configurable Propulsion Parameters:** Easily modify effective exhaust velocity ($v_e$), initial rocket mass ($m_0$), and propellant consumption rate ($\dot{m}$).
* **Data Visualization:** Generates a clean 2D plot showing instantaneous velocity ($m/s$) as a function of burn time ($s$).

## 📐 Mathematical Background

The trajectory calculation is built upon the **Tsiolkovsky Rocket Equation**:

$$
\Delta v(t) = v_e \ln \left( \frac{m_0}{m(t)} \right)
$$

Where:
* $v_e$ = Effective exhaust velocity ($m/s$)
* $m_0$ = Initial total mass (wet mass) ($kg$)
* $m(t) = m_0 - \dot{m} t$ = Instantaneous mass at time $t$ ($kg$)
* $\dot{m}$ = Mass flow rate / propellant burn rate ($kg/s$)

The script evaluates the continuous evolution of velocity over a time interval $t \in [0, 10]$ seconds.

## 🛠️ Prerequisites & Installation

Ensure you have Python installed along with the required scientific computing libraries:

```bash
pip install numpy matplotlib scipy
```

## 🚀 How to Run

1. Navigate to the project directory:
   ```bash
   cd Rocket_Physics
   ```

2. Execute the Python script:
   ```bash
   python rocket_equation_numerical_solver.py
   ```

## 📊 Output

Upon execution, the script displays a Matplotlib window illustrating the rocket's velocity curve across the defined 10-second burn duration.