# COVIDCAT

The COVIDCAT shiny application produces daily updated COVID-19 data visualization  in  Catalonia available to all public in https://ubidi.shinyapps.io/covidcat/. The R code for reproducing the application is found in this repository.

In the folder 'APP' there is the code for generating the app in 'app.R' along with all the data generated by 'MakingData.R'. In the WWW/ folder there are the logos used and the JavaScript code needed to insert a logo in the navigation bar.

All the files necessary to generate all the data with the results are outside the application folder. The source code found in 'MakingData.R' reads the data and calculates all the parameters for all the periods that can be visualized in the app. For this, some datasets are needed that are already present in this repository in a zip compressed format and can also be downloaded in the sources commented in the code. Two of them, 'dat' and 'dat_edat' are updated day to day. The ones present in this repository were generated at 14/12/2020 so they are not up to date. To access to the updated data from the online portal a SOCRATA API is needed so one has to create first a SOCRATA free acount [https://support.socrata.com/hc/en-us]. Having a SOCRATA's user and a password one can download both up to date data sets using the commented code in 'MakingData.R' with the corresponding username and password created. For the calculation of the bayesian indicators calculated via the functions in 'models.R', the INLA package is needed. To download the package one has to follow the instructions in [https://www.r-inla.org/download-install].
