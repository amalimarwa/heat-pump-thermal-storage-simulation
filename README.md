# Heat Pump & Thermal Storage Simulation (Python)

This project models the dynamic operation of a heat pump supplying a residential building over a 24-hour period.  
It combines thermodynamic COP estimation, heating load modeling, regression-based forecasting, and ODE-based thermal storage simulation with on/off control.

The objective is to explore system performance, control behavior, and overall energy efficiency using Python.

---

## Model Components

- Outdoor temperature sinusoidal profile  
- Building heating load calculation (U·A·ΔT conduction model)  
- Carnot-based heat pump COP estimation  
- Electrical power consumption calculation  
- Linear regression forecasting of heating load  
- Dynamic tank temperature simulation using `scipy.solve_ivp`  
- On/Off control with safeguard temperature limit  

---

## Key Performance Metrics (Example Run)

- Average COP: **9.20**  
- Seasonal-like COP proxy (Q/P): **7.55**  
- Total daily heating energy: **16.128 kWh**  
- Total daily electric energy: **2.136 kWh**  
- Daily average tank temperature: **41.18 °C**  
- Heat pump ON time: **~100%**  

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/amalimarwa/heat-pump-thermal-storage-simulation.git
```

### 2. Navigate into the project folder

```bash
cd heat-pump-thermal-storage-simulation
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook heat_pump_simulation.ipynb
```

You can run the project using:

- Jupyter Notebook  
- Google Colab  
- Anaconda  
- Any Python virtual environment  


## Example Results

### Outdoor Temperature Profile
![Outdoor Temperature](figures/Outdoor_Temp.png)

### Heat Pump COP
![COP](figures/COP.png)

### Heating Load & Regression
![Load Forecast](figures/Load_Forecast.png)

### Tank Temperature (On/Off Control)
![Tank Temperature](figures/Tank_Temp.png)

## Future Improvements

- Implement PID control instead of On/Off control
- Include tank heat losses to ambient
- Simulate multi-day operation
- Add seasonal performance evaluation (SCOP)
- Integrate real weather dataset input
