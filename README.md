# IRT 3-Parameter Model

In this project, we analyzed a group of 536 students' test results to see if IRT's Psychometry models combined with MCMC sampling can help us predict a student's probability of succeeding given their ability, test difficulty, and guessing ability. 


## Exploratory Analysis of Students & Test
- 536 students answered 15 items. A correct answer is indicated by “1” and an incorrect answer by “0.”
Test Performance graph
- Item 03 was the easiest item and item 14 was the most difficult
Student Performance
- The highest density of students had less than 50% correct, this implies a significantly harder assessment than usual

## Convergence 
MCMC Convergence (RHAT) graph
- Based on the NUTS algorithm, the chains for the posterior have converged which means our parameters have largely agreed on a number
## Divergence from Prior
Student Ability Prior vs. Posterior graph
- The posterior Distribution has diverged from the prior reasonably by how the yellow dots stray from the blue ones
Test Question Prior vs. Posterior graph
- Item Parameters 30-45 are the “C” or “pseudo-guess” parameter and belong to all items (questions)
- The 30-45 items cannot be trusted since there’s no clear divergence, the prior and posterior are parallel
## Prediction Performance
Observed vs. Predicted Item Performance graph
- Highlighted portion reveals the least-fitting item, every other item was well predicted
Observed vs. Predicted Item Performance (continuous line) graph
- Highlighted portion contains unexplained discrepancy between the model and distribution
Student Ability vs. Test Difficulty graph
- Location based graph where the plotted students can only answer questions to the left of their point. The graph here suggests that even the highest performing student’s ability is lower than the difficulty
- Here, we can see that a good student performed better than an avg student, so the discriminatory predictability of the posterior did well
## Final Analysis
ICC Graph
- Item 01 was chosen for its high quality estimation, but based off the reverse shape of the ICC, it is NOT recommended for assessment purposes
