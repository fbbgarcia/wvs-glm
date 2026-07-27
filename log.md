# Project Log

## Model 1: logit, all predictors
1. Fit Model 1: logit, all predictor main effects.
2. **Deviance GoF test: failed, *p* = 0.002.**
3. Checked expected counts: fine.
4. Checked VIFs: all OK.
5. Checked residual plots: fine.
6. Checked for influential observations:
   a. Outliers: observations 32, 67.
   b. High leverage: observations 68, 91.
   c. High influence: observation 94.
7. Checked for overdispersion: passed (*p* = 0.896).

## Model 2: logit, stepwise selected predictors
8. Fit Model 2: logit, stepwise selected predictors (both directions) to improve Model 1 fit.
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Gender × Degree
   g. Religion × Degree
   h. Religion × Country
   i. Religion × Age
   j. Degree × Country
   k. Country × Age
9. Deviance GoF test: passed (*p* = 0.530).
10. Checked expected counts: fine.
11. Checked VIFs: all OK.
12. Checked residual plots: fine.
13. Checked for influential observations: all OK.
14. Checked for overdispersion: passed (*p* = 0.576).

## Model 3: probit, all predictors
15. Fit Model 3: probit, all predictor main effects.
16. **Deviance GoF test: failed, *p* = 0.002.**
17. Checked expected counts: fine.
18. Checked VIFs: all OK.
19. **Checked residual plots: possible slight curve.**
20. Checked for influential observations:
   a. Outliers: observations 32, 67.
   b. High leverage: observations 68, 91.
   c. High influence: observation 94.
21. Checked for overdispersion: passed (*p* = 0.856).

## Model 4: probit, stepwise selected predictors
22. Fit Model 4: probit, stepwise selected predictors (both directions) to improve Model 3 fit.
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Gender × Degree
   g. Religion × Country
   h. Religion × Age
   i. Degree × Country
   j. Country × Age
23. Deviance GoF test: passed (*p* = 0.538).
24. Checked expected counts: fine.
25. Checked VIFs: all OK.
26. Checked residual plots: fine.
27. Checked for influential observations: all OK.
28. Checked for overdispersion: passed (*p* = 0.584).

## Model 5: cloglog, all predictors
29. Fit Model 5: cloglog, all predictor main effects.
30. **Deviance GoF test: failed, *p* = 0.001.**
31. Checked expected counts: fine.
32. Checked VIFs: all OK.
33. **Checked residual plots: possible slight curve.**
34. Checked for influential observations:
   a. Outliers: observations 31, 32.
   b. High leverage: observations 67, 68.
   c. High influence: observation 91.
35. Checked for overdispersion: passed (*p* = 0.960).

## Model 6: cloglog, stepwise selected predictors
36. Fit Model 6: cloglog, stepwise selected predictors (both directions) to improve Model 5 fit.
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Gender × Degree
   g. Religion × Degree
   h. Religion × Country
   i. Religion × Age
   j. Degree × Country
   k. Country × Age
37. Deviance GoF test: passed (*p* = 0.485).
38. Checked expected counts: fine.
39. Checked VIFs: all OK.
40. Checked residual plots: fine.
41. Checked for influential observations: all OK.
42. Checked for overdispersion: passed (*p* = 0.592).

## Model 7: loglog, all predictors
43. Fit Model 7: loglog, all predictor main effects.
44. **Deviance GoF test: failed, *p* = 0.003.**
45. Checked expected counts: fine.
46. Checked VIFs: all OK.
47. **Checked residual plots: possible slight curve.**
48. Checked for influential observations:
   a. Outliers: observations 32, 67.
   b. High leverage: observations 68, 91.
   c. High influence: observation 94.
49. Checked for overdispersion: passed (*p* = 0.840).

## Model 8: loglog, stepwise selected predictors
50. Fit Model 8: loglog, stepwise selected predictors (both directions) to improve Model 7 fit.
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Gender × Degree
   g. Religion × Degree
   h. Religion × Country
   i. Religion × Age
   j. Degree × Country
   k. Country × Age
51. Deviance GoF test: passed (*p* = 0.585).
52. Checked expected counts: fine.
53. Checked VIFs: all OK.
54. Checked residual plots: fine.
55. Checked for influential observations: all OK.
56. Checked for overdispersion: passed (*p* = 0.864).

57. Compared AIC of Models 2, 4, 6, and 8: all similar; Model 8 only slightly better (551.440, 551.182, 552.935, 549.635).

## Models 9–10: logit, manually reduced variables
58. LRTs on Model 2 with Benjamini–Hochberg adjustments:
   a. Religion (*p* = 0.2566).
   b. Gender × Degree (*p* = 0.116).
   c. Religion × Age (*p* = 0.083).
59. Fit Model 9 (removed Gender × Degree).
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Religion × Degree
   g. Religion × Country
   h. Religion × Age
   i. Degree × Country
   j. Country × Age
60. LRT between Models 2 and 9: passed (*p* = 0.105).
61. LRTs on Model 9 with Benjamini–Hochberg adjustments:
   a. Religion (*p* = 0.261).
   b. Religion × Age (*p* = 0.066).
62. Fit Model 10 (removed Religion × Age).
   a. Gender
   b. Religion
   c. Degree
   d. Country
   e. Age
   f. Religion × Degree
   g. Religion × Country
   h. Degree × Country
   i. Country × Age
63. LRT between Models 9 and 10: passed (*p* = 0.0598).
64. LRTs on Model 10: only Religion main effect not significant, but retained due to significant interactions.
65. Deviance GoF test: passed (*p* = 0.357).
66. Checked expected counts: fine.
67. Checked VIFs: all OK.
68. Checked residual plots: fine.
69. Checked for influential observations: all OK.
70. Checked for overdispersion: passed (*p* = 0.656).

## Models 11–12: probit, manually reduced variables
71. LRTs on Model 4 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.254).
    b. Gender × Degree (*p* = 0.117).
    c. Religion × Age (*p* = 0.083).
72. Fit Model 11 (removed Gender × Degree).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Religion × Age
    i. Degree × Country
    j. Country × Age
73. LRT between Models 4 and 11: passed (*p* = 0.106).
74. LRTs on Model 11 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.250).
    b. Religion × Age (*p* = 0.067).
75. Fit Model 12 (removed Religion × Age).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Degree × Country
    i. Country × Age
76. LRT between Models 11 and 12: passed (*p* = 0.0598).
77. LRTs on Model 12: only Religion main effect not significant, but retained due to significant interactions.
78. Deviance GoF test: passed (*p* = 0.364).
79. Checked expected counts: fine.
80. Checked VIFs: all OK.
81. Checked residual plots: fine.
82. Checked for influential observations: all OK.
83. Checked for overdispersion: passed (*p* = 0.600).

## Models 13–14: cloglog, manually reduced variables

84. LRTs on Model 6 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.370).
    b. Gender × Degree (*p* = 0.101).
    c. Religion × Age (*p* = 0.088).
85. Fit Model 13 (removed Gender × Degree).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Religion × Age
    i. Degree × Country
    j. Country × Age
86. LRT between Models 6 and 13: passed (*p* = 0.091).
87. LRTs on Model 13 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.371).
    b. Religion × Age (*p* = 0.069).
88. Fit Model 14 (removed Religion × Age).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Degree × Country
    i. Country × Age
89. LRT between Models 13 and 14: passed (*p* = 0.062).
90. LRTs on Model 14: only Religion main effect not significant, but retained due to significant interactions.
91. Deviance GoF test: passed (*p* = 0.315).
92. Checked expected counts: fine.
93. Checked VIFs: all OK.
94. Checked residual plots: fine.
95. Checked for influential observations: all OK.
96. Checked for overdispersion: passed (*p* = 0.680).

## Models 15–16: loglog, manually reduced variables

97. LRTs on Model 8 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.162).
    b. Gender × Degree (*p* = 0.141).
    c. Religion × Age (*p* = 0.077).
98. Fit Model 15 (removed Gender × Degree).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Religion × Age
    i. Degree × Country
    j. Country × Age
99. LRT between Models 8 and 15: passed (*p* = 0.129).
100. LRTs on Model 15 with Benjamini–Hochberg adjustments:
    a. Religion (*p* = 0.157).
    b. Religion × Age (*p* = 0.063).
101. Fit Model 16 (removed Religion × Age).
    a. Gender
    b. Religion
    c. Degree
    d. Country
    e. Age
    f. Religion × Degree
    g. Religion × Country
    h. Degree × Country
    i. Country × Age
102. LRT between Models 15 and 16: passed (*p* = 0.057).
103. LRTs on Model 16: only Religion main effect not significant, but retained due to significant interactions.
104. Deviance GoF test: passed (*p* = 0.412).
105. Checked expected counts: fine.
106. Checked VIFs: all OK.
107. Checked residual plots: fine.
108. Checked for influential observations: all OK.
109. Checked for overdispersion: passed (*p* = 0.968).

110. Compared AIC of Models 10, 12, 14, and 16: all similar; Model 16 only slightly better (553.481, 553.201, 555.109, 551.465).

## Final Model: Model 10

111. LRT between Model 10 and the full logit model: passed (*p* = 0.3733).
112. Produced final model output.
113. Produced final model predictions.
114. **Computed ROC–AUC: 0.6105 (low).**
115. **Computed confusion matrix, sensitivity, specificity, and accuracy at a 0.5 cutoff, indicating poor predictive performance (Sensitivity = 0.6075, Specificity = 0.542, Accuracy = 0.575).**
