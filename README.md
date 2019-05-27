# Code to replicate analyses in Bergen & Trott (submitted)

## About the paper

This paper is an extension to an earlier publication ([Trott & Bergen, 2018](https://www.tandfonline.com/doi/full/10.1080/0163853X.2018.1548219)), which found:  
1. Comprehenders are more likely to interpret a potential indirect request (e.g. "It's cold in here") as a request when the speaker can be inferred to be unaware of an obstacle to fulfilling the request (e.g. a broken heater).  
2. Participants with higher *mentalizing* ability, as measured by the Short Story Task ([Dodell-Feder et al, 2013](https://dash.harvard.edu/bitstream/handle/1/11879039/3820595.pdf?sequence=1)), showed a stronger effect of Speaker Awareness. That is, better mentalizers were more likely to modulate their pragmatic interpretations as a function of what a speaker could be inferred to know.

Previous work left a critical question open: is the effect of mentalizing due primarily to better mentalizers being more likely to **sample** information about a speaker's knowledge states in the first place, or are better mentalizers also more likely to **deploy** this information?

In the current work, we manipulate both the task participants are asked to perform (Experiments 1a-1b), as well as how explicitly a speaker's knowledge states are given in a passage (Experiment 2), and find that mentalizing predicts both *sampling* and *deployment* rate, provided the task explicitly involves knowledge in some way. This suggests that comprehenders might recruit their mentalizing capacity flexibly, in a task-dependent manner.

## Data

The aggregated critical data is found under `Experiment1/data` and `Experiment2/data` respectively.

Note that this data does not include identifying information about a participant's gender or age. Please contact Sean Trott (sttrott at ucsd dot edu) separately for demographic information.

### Primary variables

The following factors are consistent across both experiments:

`Condition`: was the speaker aware or unaware of an obstacle to fulfilling a request?  
Factor levels: `Speaker Unaware`, `Speaker Aware`

`answer`: participant response (`yes` or `no`).  
(Note that for Experiment 1, the meaning of this variable changes depending on experimental group; see notes below.)

`Order`: trial order (continuous, 1-8 or 1-16)


#### Experiment 1

`exp_group`: Participants in Experiment were assigned to one of two experimental groups: **Inference** or **Knowledge**  
Individual difference variables:  
- `exp.inf.mean`: Mean explicit mental state reasoning score (averaged across both coders).  
- `rc.mean`: Mean reading comprehension score (averaged across both coders).  
- `rc.bins`: Binned reading comprehension (created in `experiment1_analysis.Rmd`)  
- `spon.true`: Spontaneous mental state reasoning scores, including tiebreaker codes.  

`numeric_categorization2`: recoded version of `answer`, to align `yes` responses across experimental groups.  
In the Knowledge* group, a "Yes" response would by default be correct in Speaker Aware condition, e.g. "Yes, the speaker is aware of the obstacle"; whereas in the *Inference* group, a "Yes" response would by default be correct in the Speaker Unaware condition, e.g. "Yes, the speaker is making a request". This recoding inverts *Knowledge* answers, such that a "Yes" now corresponds to: "Yes, the speaker is unaware of the obstacle". This allows for direct comparison across experimental groups in which the same expected outcome corresponds to each condition.


#### Experiment 2

Individual difference variables:  
- `exp_inf_mean`: Mean explicit mental state reasoning score (averaged across both coders).  
- `rc_mean`: Mean reading comprehension score (averaged across both coders).  
- `rc_bins_1`: Binned reading comprehension (created in `experiment1_analysis.Rmd`)  
- `spon_true`: Spontaneous mental state reasoning scores, including tiebreaker codes. 


#### Random factors  
- `subject`: subject ID  
- `stimNum`: item number  


## Analyses

The analyses can be found in the `.Rmd` files:
- `Experiment1/experiment1_analysis.Rmd`
- `Experiment2/experiment2_analysis.Rmd`



