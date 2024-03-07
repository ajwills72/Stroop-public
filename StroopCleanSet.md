# Many Labs 3 (N = 3,433)

_File_: ml3.rda

- Ebersole et al. (2016)
  - DOI: http://dx.doi.org/10.1016/j.jesp.2015.10.012
  - Repository: https://osf.io/ct89g/
    - Original Data File: StroopCleanSet.csv
    - Documentation: Many Labs 3 Supplementary Materials.pdf
    - Note: There is also ML3StroopRaw.csv, which includes the practice trials, but also includes trials with very odd labelling (e.g. 'anagram').

## Summary

Stroop as part of 10 experiments, random order within that sequence. It’s a forced choice between three display colours (red, blue, green). The words are also red, blue, green, and all combinations are present, so two-thirds of trials are incongruent and one-third are congruent. There are no neutral trials. 

## Codebook

None provided. Here's my interpetation:

- _block_number_: Always 1.
- _block_name_: screen colour of word presented on this trial, followed by non-informative stuff.
- block_trial_count: Always 21
- _block_pairing_definition_: the correct response for this trial.
- _study_name_: cebersole.XXX, where XXX is the location this participant was tested.
- _task_number_: Unsure. Could be order in testing session (many other experments were run), but numbers seem to exceed tasks.
- _task_name_: Always 'stroop'
- _trial_number_: Trial number (0-62)
- _trial_name_: the written word presented on this trial, followed by non-informative stuff. 
- _trial_response_: The response of the participant on this trial, indicating screen colour of word presented on this trial.
- _trial_latency_: Response time in milliseconds
- _trial_error_: 1 = Correct, 0 = Error.
- _session_id_: Unique participant ID, potentially links to other files in repo.
- _trial_word_: The response key pressed by the participant.
- _congruent_: Is this a Congruent, or Incongruent, trial?

## Procedure

Participants will complete a variation of the Stroop task in which they are presented with the words “red”, “blue”, and “green” written in either red, blue, or green.  Within participants, in one third of trials the word will match the color of the text and in two thirds of the trials the word will not match the color of the text.  Participants will read a description of the task and complete a 12-trial practice block before the critical trials.  The description of the task is as follows:

“On the following page, you will complete a color recognition task. Several words will be presented. For each word, indicate the color of the font by pressing the appropriate key.

Specifically, if the word is presented in red, press the 1 key. If the word is presented in blue, press the 2 key. If the word is presented in green, press the 3 key.

So for instance, if you saw the word red, you would press the 1 key.

If you saw the word blue, you would also press the 1 key because although the meaning of the word is a different color, the color of the font is still red.

Complete this task as quickly as possible while minimizing errors.

Once you have understood these instructions, place your fingers on the 1, 2, and 3 keys and press 'continue' to begin the task. You will first do a practice block before continuing to the test block.”

When participants begin, items appear one at a time in the middle of the screen and labels at the top of the screen remind participants of which key is associated with which color response. If participants make a categorization error, a red X will appear on the screen to note the error, and the task will advance to the next trial.  Upon completion of the practice block, participants will be presented with the description of the task again and then complete a 63-trial test block so that each color word appears 21 items, 7 times in each of the three font colors.

## Analysis plan (pre-registered)

The Stroop task is a within-person experiment with two response conditions - font color congruent with color word and font color incongruent with color word -and response latency as a dependent variable.  The analysis strategy uses the D scoring algorithm for analysis of such data (Greenwald, Nosek, & Banaji, 2003; Nosek & Sriram, 2007).  First, all trials with latencies above 10,000ms will be removed.  Then, we will calculate an average response time for all correct responses separately for congruent and incongruent trials.  Response latencies for trials with errors will be replaced by the mean of correct responses in that condition plus 600 milliseconds.  Then, the means for congruent and incongruent trials will be recomputed with all trials.  D is the difference between these two means divided by the standard deviation of all trials regardless of condition.  Positive scores will indicate slower response times on average for incongruent compared to congruent trials.
