TO-DO
=====

A list of bite-sized tasks that can usefully be done.

Vectorising
-----------
A lot of the solver functions would be sped up by vectorising. 
At the moment, most serially apply zero_finder functions to solve for H.
In [carbon_fns](cbsyst/carbon_fns.py):

- [ ] CO2SYS-style zero finder for HCO3_TA (case 11)
- [ ] CO2SYS-style zero finder for CO3_TA (case 13)
- [ ] Vectorise CO2_HCO3 (case 2)
- [ ] Vectorise CO2_CO3 (case 3)
- [ ] Vectorise CO2_DIC (case 5)
- [ ] Vectorise HCO3_CO3 (case 10)
- [ ] Vectorise HCO3_DIC (case 12)
- [ ] Vectorise CO3_DIC (case 14)

Contition I/O
-------------


Parameter I/O
-------------
At the moment, the Xsys functions can only take single combinations of input parameters.
It might be useful to allow for the calculation of multiple combinations of input combinations at once (a la CO2SYS.m).
However, this would require a major re-tooling of the algorithms, which currently identify parameters to be calculated by whether they are 'None' or not.
I reckon the effort involved here would be much greater than the inconvenience for the user having to run the function twice for different sets of input parameters.
How often do people actually use the ability of CO2SYS.m to take more than one combination of input parameters?

**This is shelved for the moment - revisit later if it becomes an issue**