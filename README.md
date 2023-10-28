# State of charge estimation for a unmanned vehicle
__SOC Estimation Methodology__

The estimation of SOC (State of Charge) has been achieved by employing both the Coulomb counting method and the open circuit voltage method. In the initial phase of utilizing Google Colaboratory, the focus was on techniques for preprocessing data. Subsequently, in the second segment, an initial evaluation of the charge capacity of the battery and SOC at various time points was determined using the Coulomb counting method. The third section involved utilizing the previously estimated SOC to create a polynomial that characterizes the correlation between open circuit voltage (OCV) and SOC. Ultimately, the actual SOC value was determined by computing a weighted average of the SOC estimate obtained through Coulomb counting (weighted at 0.8) and the SOC estimate derived from OCV (weighted at 0.2). This weight distribution stems from the superior stability of the Coulomb counting estimate.

__Data Preprocessing in the Initial Phase__

During the initial data preprocessing phase, several operations were performed. These operations encompassed the removal of unwanted columns, deletion of redundant rows, elimination of duplicate entries, and rectification of data concerning the timestamps of measurements.

__Charge Estimation and Polynomial Regression__

In the second part of the process, the operations involved estimating the total charge capacity of the utilized battery (2.5Ah 3s lipo battery) and determining the state of charge using the Coulomb counting method. This SOC estimation was then incorporated in the utilization of the open circuit voltage method.

__Polynomial Regression and Model Training__

The third section focused on operations that entailed the creation of a polynomial using polynomial regression to describe the relationship between open circuit voltage and SOC. Initially, noise in the data was reduced through the application of a moving average. Subsequently, data for the polynomial regression was prepared by exponentiating the OCV data with powers of 0.2, 0.4, 0.6, 0.8, and 2. The data was standardized and employed as input features for the polynomial regression. The resulting model achieved an R2 score of 0.8284. In this phase, efforts were made to overfit the data with the aim of obtaining a polynomial that precisely determined SOC values for given open circuit voltage values. The training of the model involved the use of the Nadam optimizer with an initial learning rate of 0.05, and the model was trained for 500 epochs.
