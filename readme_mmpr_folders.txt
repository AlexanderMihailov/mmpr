readme_mmpr_folders.txt

Default path: [F:\archive\comp\ on the external drive used, as noted in the code, but can be anything] mmpr\
First created: 17 August 2012, by Alexander Mihailov
Last modified: 19 August 2019, by Alexander Mihailov
(to be printed out in Landscape orientation, 110-character length of text observed below)

This readme file describes the mmpr folder structure in the zip archive with replication files for McKnight,
Mihailov and Rumler, "Inflation Forecasting Using the New Keynesian Phillips Curve with a Time-Varying Trend",
Economic Modelling (in press).
______________________________________________________________________________________________________________

Main folder: \mmpr - contains two subfolders (as described below)

    \dataset: our dataset in *.xlsx (Excel spreadsheet) format, eausdb15.xlsx; and in *.txt (ASCII) format,
              eausdb15.txt: quarterly time series for the Euro Area and the United States (the sources and
              definitions of the data are described in the Supplementary Online Appendix, section A)

    \eviewsdb - contains two subfolders (as described below)

        \dat: the identical dataset in *.wf1 (EViews workfile) format, eausdb15.wf1, called by the programs
              as input

        \prg: EViews program files, in *.prg format, using the EViews dataset, eausdb15.wf1 (needs to be open),
              as input - contains two subfolders (as described below)
              
              \fig: EViews program graph output files (saved each in *.eps, *.emf and *.bmp formats) - some
                    of these figures are additional, and are not found in the main text or the online appendix

              \out: Eviews program output files, saved with the same name as the program that generated them
                    but with "...out.wf1" at the end; some of these contain "fig[...]" near the end of their
                    filenames, and they are different from the corresponding output files with the same name
                    in that they contain additionally created figures after the program has been run and the
                    respective output file saved

Each of the programs is annotated in much detail so that reading through it explains what it does and how. The
program eausprelim.prg has to be run first, and the resulting data transformations saved as eausprelimout.wf1.
This latter file is then used as input by the eight programs, four for the Euro Area (filenames beginning with
"ea") and four for the United States (filenames beginning with "us"), which are as follows:

eatrinfnkpc3var4mmchp1ar1trgrf_rec00q1to15q4levr.prg - "mmc" denotes the MOE RMC proxy and "rec" recursive window
eatrinfnkpc3var4mmchp1ar1trgrf_roll00q1to15q4levr.prg - "roll" denotes rolling window
eatrinfnkpc3var4rulchp1ar1trgrf_rec00q1to15q4levr.prg - "rulc" denotes the RULC RMC proxy
eatrinfnkpc3var4rulchp1ar1trgrf_roll00q1to15q4levr.prg

ustrinfnkpc3var4mmchp1ar1trgrf_rec00q1to15q4levr.prg
ustrinfnkpc3var4mmchp1ar1trgrf_roll00q1to15q4levr.prg
ustrinfnkpc3var4rulchp1ar1trgrf_rec00q1to15q4levr.prg
ustrinfnkpc3var4rulchp1ar1trgrf_roll00q1to15q4levr.prg

Furthermore, in the filenames above:

"trinfnkpc" denotes the TVT-NKPC
"3var4" denotes the theory-implied 3-variate VAR with 4 lags used in generating the cyclical component forecast
"ar1trgrf" denotes the theory-implied AR with 1 lag used in generating the trend growth component forecast
"hp1" denotes the one-sided Hodrick-Prescott filter used in the forecasting (this add-in needs to be downloaded)
"00q1to15q4" denotes the forecast evaluation period: from Q1 of 2000 to Q4 of 2015
"levr" denotes the cyclical component of the level of the respective RMC proxy in the TVT-NKPC