# State-of-charge-estimation-for-a-unmanned-vehicle

The SOC estimation has been accomplished through the utilization of both the Coulomb counting method and the open circuit voltage method. The initial phase of the Google Colaboratory entails the techniques employed for data preprocessing. Subsequently, in the second part, an initial assessment of the charge quantity attainable from the battery and the SOC at various time points has been established using the Coulomb counting method. In the third section, the preceding SOC estimation has been employed to formulate a polynomial that depicts the relationship between the open circuit voltage (OCV) and the SOC. Ultimately, the actual SOC value has been ascertained by computing a weighted average of the SOC estimate obtained through Coulomb counting, weighted at 0.8, and the SOC estimate derived from OCV, weighted at 0.2. This weight distribution is attributed to the superior stability of the Coulomb counting estimate

__text__
