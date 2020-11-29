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

# Interventions

For the 4th review, we ask you to make a recommendation for the population to follow in order to control the epidemic. The recommendation you make should be motivated from scenarios you run and simulate.

The possible interventions are given below. Some interventions come with parameters and you must provide values for them, should you recommend these interventions. Multiple interventions can be applied at the same time.

- Wearing a mask: Reduce the infection rate by 20%. No parameters are associated with this intervention.
- Case isolation: When an individual becomes symptomatic, it isolates itself. The infection rate associated to isolated individuals is reduced by 25% at home, 90% in communities and 100% at work or school (no infection at work or school). It has as parameter the duration of the isolation.
- Home quarantine: When an individual becomes symptomatic, all the individuals of its home isolate them-selves. The infection rate associated to isolated individuals is reduced by 25% at home, 90% in communities and 100% at work or school (no infection at work or school). It has as parameter the duration of the isolation.
- Lock-down: The infection rate associated to every individual is reduced by 75% in communities, by 75% at work and by 100% at school. There is no reduction at home. No parameters are associated with this intervention.
- Social distancing: Each individual above a given age applies social distancing. It reduces the infection rate at work and in communities by 75%. It has as parameter the age above which people should apply social distancing.

When combining interventions, the strongest reduction is applied. The only exception is the intervention of wearing a mask, that has a multiplicative effect on the others. Case isolation and home quarantine cannot be combined.

You may assume that around 90% of the citizens will follow the recommendation, others act as if no intervention were made.

Your recommendation will become effective by December 18 and will be run until the end of January.
