# Home Electronics Lab

Controlling the Siglent SDS1104X-U oscilloscope and SDG1032X Arbitrary Waveform Generator with SCPI.

Prerequisites:

- `pip3 install -U pyvisa`
- `pip3 install -U matplotlib`

## Data Logger

![Data Logger](img/datalogger.png)

Samples active oscilloscope channels in Roll mode at the trigger point. Outputs each sample's timestamp, elapsed time, and voltage of the active channels to `stdout` in CSV format. Optionally plots the output. It is assumed that each channel is set up with the optimal vertical scale and position.

`datalogger.py [-i <interval>] [-n <limit>] [-p]`

where *interval* is the sample interval in seconds (default is 1), and *limit* is the maximum number of samples (default is unlimited). To plot the output, specify a limit and the `-p` argument. For example

`datalogger.py -n 100 -p`
