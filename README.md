# Quickstart guide:
1. I was using `virtualenv` to handle packages
2. Install dependencies
```bash
pip install -r requirements.txt
```

# AirPump failures

A customer is manufacturing devices containing air pumps that provide pressure for a machine cycle. Ideally, the air pressure rises sharply and remains stable throughout the machine's cycle, where it drops sharply. However, it can happen that the air pressure drops due to pump failure, or the air pressure rises or drops slowly.

The goal of the project is to detect a pump failure.
The typical air pump failure is a temporary pressure decrease in the first half of the cycle.


## Data structure


### Data

The data consists of the following columns (in this particular order):

- MachineId - Id of the machine
- MeasurementId - Id of the measured cycle
- Pressure - Air pressure (kPa)

The data does not contain timestamps, but for each machine and measured cycle combination, observations (i.e. rows) of the pressure values are ordered by time, and the time intervals between individual observations are always the same.

### Labels

The labels consists of the following columns (in this particular order):

- MachineId - Id of the machine
- MeasurementId - Id of the measured cycle
- PumpFailed - True if pump failed
- SlowStart - True if the pressure rised slowly
- SlowEnd - True if the pressure dropped slowly


## Your task:

- Develop a predictive model for the PumpFailed column and report its performance in appropriate metrics.
- Explain your model.


## Notes

- We suggest you to use Python and Jupyter notebook for this assignment.


## Requirements

- Spend maximum of one working day on this assignment
- Document your work so the Jupyter notebook is self-explanatory
