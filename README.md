# ICARUS-Power-Challenge
a repo for icarus' phase 2

---------------------

# Tools used:
qwen ai- for understanding the project and making sense of the steps
circuitjs1- online open source SPICE tool for creating the circuit and obtaining waveforms

---------------------
# Approach & Assumptions:
Instead of a PWL current source a pulse voltage was used since I wasn't able to make PWL source work, I did read about using a current source with a VCCS to make it work, in the official documentation(https://www.falstad.com/circuit/doc/) but since the pulse voltage does a similar job (V=24.494898 and duty cycle=66.6667% approximately gives 6W input power and runs equivalent to 60 mins in 90 mins). Every pulse voltage source is assumed to be of frequency 40Hz, EPS loss=100 ohm, Payload=700 ohm, OBC=500 ohm, TT&C=450 ohm. Battery is consisted of a cell ov voltage 7.4V with internal resistance 10 ohm. Timed loads are connected using a SPST switch which is controlled by pulse voltage sources. Payload has a similar timing as the sun and eclipse while TT&C has a duty cycle of 25%. An OPAMP integrator circuit is used to show qualitative SOC proxy where it's voltage rises with sun's power input and SOC proxy's voltage falls with eclipse.

To see the circuit go to circuitjs1(https://www.falstad.com/circuit/circuitjs.html) and click on file->import from text; now copy and paste the code provided in the txt file inside src/ inside this repository

---------------------

# Links to resources:

Qwen AI was used in this project, here's the chat:
https://chat.qwen.ai/s/dcdc56b9-9614-4dad-9f15-1e8bbc6872cb?fev=0.0.203

Circuitjs1 official documentation also helped:
https://www.falstad.com/circuit/doc/

This reddit post helped to come up with the pulse voltage approach:
https://www.reddit.com/r/AskElectronics/comments/s33dxv/is_there_a_way_to_rapidly_produce_such_a_signal/
