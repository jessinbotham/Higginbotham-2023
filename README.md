Codes used to process photometry data for Higginbotham et al., 2023.

Start by downloading matlab and install pMAT.

Installation and user guide can be found here: https://github.com/djamesbarker/pMAT 

To detect peaks for specific trials use the pMAT software first to generate Trial Trace Data set and trim the timepoints for your timepoints of interest. Open the EventData_ExampleDataFile.mat and the EventDataAnalysis.m to analyze trial data for example data binned at 0.5 s intervals with the relevant area determined as -1 to 5s seconds relative to the response.



To analyze tonic activity across the session save a .csv file with the timestamp in column A and signal data in column B. See ExampleID_SessionDay_ExampleSignalFile.csv and save the file to your directory. Run the TonicSummaryTable.m to create a summary table in the directory to store sumarry data for each session. 


Use the TonicPeakAnalysis.m to start analyzing a series of data. The user will be promted for a signal file. Use example file, ExampleID_SessionDay_ExampleSignalFile.csv. The program will generate a double exponential curve and fit the data to the curve before detecting peaks. The final output will display a figure containing the curve fit, the fit data, peaks detected across the trace, and a histogram plot of the peaks detected. Each File processed will generate a unique figure and spreadsheet containing individual event measurements. The summary data for each file processed will be added to the summary table. 
