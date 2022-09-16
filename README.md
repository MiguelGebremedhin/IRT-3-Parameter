# IRT 3-Parameter Model

In this project, we analyzed a group of 536 students' test results to see if IRT's Psychometry models combined with MCMC sampling can help us predict a student's probability of succeeding given their ability, test difficulty, and guessing ability.
<img width="820" alt="IRT model" src="https://user-images.githubusercontent.com/112588590/190560752-1719eaf2-d478-4d98-a382-abf604ad02e0.PNG">


## Exploratory Analysis of Students & Test
- 536 students answered 15 items. A correct answer is indicated by “1” and an incorrect answer by “0.”
<img width="417" alt="dimension of students" src="https://user-images.githubusercontent.com/112588590/190559274-cd8a3b2d-76ee-461a-8dca-fbfa9ec79ced.PNG">

Test Performance graph
- Item 03 was the easiest item and item 14 was the most difficult
<img width="475" alt="item performance" src="https://user-images.githubusercontent.com/112588590/190559948-1ae244ff-0eb8-49b7-addf-f83748057b78.PNG">
Student Performance
- The highest density of students had less than 50% correct, this implies a significantly harder assessment than usual
<img width="546" alt="student population performance" src="https://user-images.githubusercontent.com/112588590/190560045-00625890-b209-4410-aec8-1f378f2adbed.PNG">

## Convergence 
MCMC Convergence (RHAT) graph
- Based on the NUTS algorithm, the chains for the posterior have converged which means our parameters have largely agreed on a number
<img width="650" alt="MCMC convergence" src="https://user-images.githubusercontent.com/112588590/190560103-c4dc4134-6163-4f9d-8d1a-6cef84cf2078.PNG">

## Divergence from Prior

Student Ability Prior vs. Posterior graph

- The posterior Distribution has diverged from the prior reasonably by how the yellow dots stray from the blue ones
<img width="609" alt="student ability prior vs  posterior" src="https://user-images.githubusercontent.com/112588590/190560178-381527b7-e0ba-40c6-aac7-a3e4d007df5e.PNG">

Test Question Prior vs. Posterior graph

- Item Parameters 30-45 are the “C” or “pseudo-guess” parameter and belong to all items (questions)
- The 30-45 items cannot be trusted since there’s no clear divergence, the prior and posterior are parallel
<img width="547" alt="item prior and posterior estimates" src="https://user-images.githubusercontent.com/112588590/190560302-c18053c4-e262-4d95-be59-e4436309f66f.PNG">

## Prediction Performance

Observed vs. Predicted Item Performance graph

- Highlighted portion reveals the least-fitting item, every other item was well predicted
<img width="546" alt="observed vs  predicted performance" src="https://user-images.githubusercontent.com/112588590/190560351-9791f719-ed6a-4790-96fa-99ac111f300c.PNG">

Observed vs. Predicted Item Performance (continuous line) graph

- Highlighted portion contains unexplained discrepancy between the model and distribution
<img width="548" alt="observed vs  predicted (continuous)" src="https://user-images.githubusercontent.com/112588590/190560405-15fedefb-95ce-41fb-ab5c-28edcb5ca5c2.PNG">

Student Ability vs. Test Difficulty graph

- Location based graph where the plotted students can only answer questions to the left of their point. The graph here suggests that even the highest performing student’s ability is lower than the difficulty
- Here, we can see that a good student performed better than an avg student, so the discriminatory predictability of the posterior did well
<img width="572" alt="ability vs  difficulty" src="https://user-images.githubusercontent.com/112588590/190560457-eae9bfc8-6892-4350-b5b0-3bff5420b8b8.PNG">

## Final Analysis

ICC Graph
- Item 01 was chosen for its high quality estimation, but based off the reverse shape of the ICC, it is NOT recommended for assessment purposes
<img width="398" alt="icc" src="https://user-images.githubusercontent.com/112588590/190560516-3701acb1-4b8e-4331-81a3-148545e960c4.PNG">
