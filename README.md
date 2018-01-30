# RplotEBS
Plots the CSV files from the Extended Bayesian Skyline Plot model in BEAST

NOTE: Currently this script only works on Macs, but can be easily tweaked to work on Linux and Windows machines.

## Download the script

    wget https://raw.githubusercontent.com/santiagosnchez/RplotEBS/master/RplotEBS.R

## Run the script

The script runs command-line by using Rscript.
If you run the script directly from the directory where the CSV files are, you only need:

    Rscript RplotESB.R 

To get a help message, type:

    Rscript RplotESB.R help

You will get:

    Error: 
    
    Try:
    Rscript RplotEBS.R path=PATH/TO/CSV/FILES pattern=.csv trim.x=-2.0 trim.y=0.6 y.eq=TRUE
    Defaults: path=. pattern=csv trim.x=NULL trim.y=NULL y.eq=FALSE
    
    Execution halted

If your files are in the desktop, and they are the only CSV files there, run:

    Rscript RplotEBS.R path='~/Desktop/' pattern=.csv

If you want to trim the x-axis on all your plots to, say, 10 Ma, run:

    Rscript RplotEBS.R path='.' pattern=.csv trim.x=-10.0

If you want to have the same y-axis on all your plots, try:

    Rscript RplotEBS.R path='.' pattern=.csv y.eq=TRUE

If you want both the x-axis trimmed and have the same y-axis in all your plots, try with:

    Rscript RplotEBS.R path='.' pattern=.csv trim.x=-10.0 y.eq=TRUE


## Generating the plot

The script will spit out a graphic device (quartz) to your script and hold there indefinitely. You should adjust you plot to the desired size and save the plot using the save menu from the upper bar. Afterwards, use the CTR+C command to terminate the script.







