This is a guide file for using the proposed DNN-based Yield maximization method. This file consists of three parts. One of the files (PHFF\Spice_Syntax_Data_Generation) is related to the PHFF example and the other one (LLTFF\Spice_Syntax_Data_Generation) is related to the LLTFF example and a separate file (Sample) from the article and is a simple sample of yield maximization that is defined for a problem with three variables in which the neural network is embedded and does not require additional hard and complicated implementation.

In the folder related to these two examples, there is a high-performance or low-power technology file (Technology_model\ 16HP/LP_Cmos_packed.mod) that must be copied to the path of the Bin folder of the Spice software so that this library applies to the example and the software. 

...\ngspice Version\Spice64\bin

Then copy the example itself in the same path next to the main software (ngspice.exe) file and browse the technology and PHFF or LLTFF  to the software by writing  this command in the command line:

PHFF.cir or LLTFF .cir

This code (LLTFF_Tran_Data_Generation.cir) simultaneously creates the desired circuit and by sweeping the selected design variables, it can generate the desired performance metrics such as setup time or power. There is also a similar file (LLTFF_DC_Data_Generation.cir) for generating data in the DC mode of the circuits.

In the Generated Data folder (Generated_Data.zip), all the data generated in the previous step is available for each performance metric. Also, each neural network code that has been learned (trained) for specific performance metrics and its saved model (weights, bias) are provided. In this regard, the below address must be deleted in the performance metric Python Code, and insert your special path to this data for each performance metric. 

'/content/drive/MyDrive/ColabNotebooks/ResearchCodes/Statistical_Design/setup_time.csv

In the Yield Maximization folder, there is also the final code of the proposed method, which by receiving the data set and the path of the neural network-based models and other initial settings, can perform the yield maximization of the circuit using the speed and accuracy of the neural network independently of the Monte Carlo method.
