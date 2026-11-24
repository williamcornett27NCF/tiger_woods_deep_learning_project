# tiger_woods_deep_learning_project

Dataset: The data comes from the paper “Dataset of Two Decades of Tiger Woods Press Conferences and Tournament Performance” (Pastoriza & Warin, 2022) and was downloaded from the authors’ GitHub repository. It has 1,284 rows covering Tiger Woods’ PGA Tour events from 1996 to 2020. Each row is one round of one tournament and includes:
1.	Text: the transcript of Tiger’s press conference after the round.
2.	Performance: his round score, leaderboard position, birdies and other stats.
3.	Context: whether the event was a major, his world ranking, injury and personal-issue flags, and sentiment scores calculated by the authors.
The newer files in the repository have an empty transcript column, so this project uses the older file (tiger_woods_sentiment.RDS), which is the only one with the interview text.
Domain: Sports analytics and natural language processing (NLP). Sports analytics usually relies only on numbers; this project tests whether an athlete’s words add useful information.
Problem: Can what Tiger says after a round predict how he plays in the next round? His answers may show confidence, frustration or physical problems that the stats do not capture. This could help coaches, sports psychologists, analysts and sports forecasters.
Prediction task: Binary classification. The input is the interview text after round n. The label is 1 if Tiger shoots 69 or lower in round n + 1 of the same tournament, and 0 if he shoots 70 or higher.
We predict the next round on purpose. The interview talks about the round Tiger just played (for example, “Shot 69 with three 3-putts”), so predicting that round would be too easy and would leak the answer. The cut-off of 69 was chosen because the median next-round score is 70, which splits the data into two equal groups
