# AirPressure

Your customer is manufacturing devices containing air pumps. Each machine consists of 4 air pumps. Ideally, the air pressure rises sharply and remains stable throughout the machine's cycle, where it drops sharply. However, it can happen that the air pressure drops due to pump failure, or the air pressure rises or drops slowly. The aim of the project is to detect such behavior for the customer.


## Data structure


### Data

The data consists of the following columns (in this particular order):

- SiteId - Id of location where the machine is located
- DeviceId - Id of the machine
- MeasurementId - Id of the individual measurement
- PumpId - Id of the pump (0 - 3)
- Pressure - Air pressure (Pascals)
- PumpActive - Information whether the pump was active

The data does not consist timestamps as they are not relevant.

### Labels

The labels consists of the following columns (in this particular order):

- SiteId - Id of location where the machine is located
- DeviceId - Id of the machine
- MeasurementId - Id of the individual measurement
- PumpId - Id of the pump (0 - 3)
- PumpFailed - True if pump failed
- SlowStart - True if the preasure rised slowly
- SlowEnd - True if the presure dropped slowly


## Your task:


- Perform an exploratory analysis of the data.
- Develop a predictive model for the PumpFailed column and report its accuracy in appropriate metrics.
- Explain your model.


## Notes

- We suggest you to use Python and Jupyter notebook for this assignment.
- If you have some time remaining you can build predictive models for the rest of label columns.


## Requirements

- Spend maximum of one working day on this assignment
- Document your work so the Jupyter notebook is self-explanatory