# PROJ0016 Big data project 2020 — COVID-20

## Data 

- `num_positive`: number of individuals tested positive during the last day. 
- `num_tested`: number of tests performed during the last day. 
- `num_hospitalized`: number of individuals currently at the hospital.
- `num_critical`: number of individuals currently in an ICU (criticals are not counted as part of `num_hospitalized`).
- `num_cumulative_hospitalizations`: cumulative number of individuals who were or are being hospitalized.
- `num_fatalities`: cumulative number of deaths.

# Extra information

October 26:
- Testing policy:
  - We estimate that at least 50% of the symptomatics are being tested. 
  - Hospitalizations necessarily imply a positive test: either a (previously) positively tested symptomatic becomes hospitalized, or a non-tested/false negative symptomatic becomes critically sick and gets hospitalized, upon which a positive test is accounted for.
  - The test sensitivity is around 70-85% and its specificity is 100%.
- The incubation period is estimated between 1 and 5 days.
- The symptomatic period (before hospitalization) is estimated between 4 and 10 days.

October 5:
- The population of the city is 1000000.
- It is reported individuals may be infected and infectious without developing symptoms.
- For now, tests are targeted at individuals with symptoms that are highly suspicious. A good fraction of the individuals developing symptoms are being tested.
- The sensitivity of the test is estimated to be 70-90%.
