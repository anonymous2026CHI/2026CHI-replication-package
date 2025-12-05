# 2026CHI-replication-package

#for code
- panel_regression_for_RQ1.R executes panel regression for new bugs.
- panel_regression_for_RQ2.R executes panel regression for new commits.
- panel_regression_for_RQ3.R executes panel regression for bug fix time.

#for data
- data/event_type.xlsx holds the event types, access, and their profiles.
- data/panel_data_for_RQ1.xlsx holds the data of panel regression for new bugs.
- data/panel_data_for_RQ2.xlsx holds the data of panel regression for new commits.
- data/panel_data_for_RQ3.xlsx holds the data of panel regression for bug fix time.

#for additional validation

We provide the monthly counts of created and merged pull requests for each project as an indicator of active and sustained maintenance. Our dataset covers the complete lifecycle of vuejs/vue, which announced its development move to a new repository on December 31, 2023. Please note that data outside its lifecycle period was excluded from our panel regression models. All other projects in our sample remained actively developed and regularly maintained through May 2025. 


#ask for questions from reviewer1 

**1. When selecting the 8 projects to be included, beyond ensuring they had at least 3,000 commits in the main branch historically in total, was any further checking done to ensure that the projects studied had regular recent maintenance activity?**

We fully understand your concern: a project in decline or no longer actively maintained likely exhibits fundamentally different fork purposes, frequencies, and integration patterns (i.e., the "fork behavior patterns" you referred to) compared to an active project. If such changes in behavior patterns due to different project stages are not properly controlled, they could indeed confound the interpretation of the relationship between convergence entropy and productivity.

Our analytical design is precisely aimed at capturing and addressing these "time-varying patterns." The monthly variations in our control variables—such as NumCores, NumPrs, and NumForks—not only reflect project activity levels but also, to some extent, mirror the underlying fork behavior patterns. For example, an increase in NumForks coupled with a decrease in NumPrs may signal project decline, where new forks are created more for archival purposes or independent development rather than for contributing back to the mainline. The high R² values of our models (e.g., 0.742 for Model B1) indirectly suggest that our set of explanatory variables has captured a substantial portion of the variance related to these evolving fork behavior patterns.

Furthermore, we have visualized the monthly counts of created and merged pull requests for each project as an indicator of active and sustained maintenance. Our dataset covers the complete lifecycle of vuejs/vue, which announced its development move to a new repository on December 31, 2023. Please note that data outside its lifecycle period was excluded from our panel regression models. All other projects in our sample remained actively developed and regularly maintained through May 2025.

**2. Can you provide a direct comparison between Convergence Entropy and established fork and convergence measures to show uniqueness and incremental value?**

Thanks for your suggestion. We already provide direct comparison table in Section Related work, including equations and interpretive scope. And we explicitly identify the research gap and explain how Convergence Entropy adds theoretical or practical value beyond existing measures.
