# Many Labs 3 (N = 3,433)

Ebersole et al. (2016)

DOI: http://dx.doi.org/10.1016/j.jesp.2015.10.012

Repository: https://osf.io/ct89g/

File: StroopCleanSet.csv

Notes: There is also ML3StroopRaw.csv, which includes the practice trials, but also includes trials with very odd labelling (e.g. 'anagram').

Codebook: There didn’t seem to be one! Here’s what I think:

- Usuable information:
  - _block_number_: Dummy variable, always 1.
  - _block_name_: colour of word presented on this trial, followed by non-informative stuff.
  - _block_pairing_definition_: the correct response for this trial.
  - _study_name_: cebersole.XXX, where XXX is the location this participant was tested.
  - _task_number_: Unsure. Could be order in testing session (many other experments were run), but numbers seem to exceed tasks. 
 
- Other columns
   
  - block_trial_count: 12 = practice block, 21 = main block
