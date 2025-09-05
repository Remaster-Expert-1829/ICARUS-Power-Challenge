Output and Observations:

The battery voltage, current and SOC proxy screenshots are available in the figures folder in this repository.
When sun is supplying the power, battery gets charged hence the soc proxy voltage increases while during an eclipse the sun discharges so the SOC proxy voltage also falls. Due to the suddent connection and disconnection of TT&C, the current rises/falls depending on whether TT&C resistance is active or not.


Element to function mapping:

PWL Current Source → Solar panels + MPPT controller (delivers ~6W during sun periods)
Battery + Series Resistance → Li-ion battery pack with internal resistance (7.4V nominal with voltage droop)
EPS Loss Resistor (0.2Ω) → Converter and wiring efficiency losses
Timed Resistive Loads → OBC(continuous), TT&C (bursts), Payload (sun-only)
OPAMP Integrator Circuit → State of Charge (SOC) estimation via coulomb counting
