# Data-Science-for-Public-Policy

Can internet voting affect turnout? Evidence from the canton of St. Gallen
Valeria Cerciello (23-746-282) & Tim Schäfer (20-610-937)
Research Question & Motivation
Political participation is declining in most Western Democracies which potentially undermines the le-
gitimacy of democratic decisions. Policy makers aim to address this issue by implementing policies
that reduce voting costs with the expectation of increasing turnout. This paper analyses the effect of
one such policy: internet voting. Specifically, we will analyse the effect of internet voting on turnout
as well as party voter shares by exploring a pilot project in the canton of St. Gallen, where five munic-
ipalities offered internet voting while the majority did not.
Previous studies (see literature) either find no or rather low positive effects on turnout. However, we
will use more recent election data. Since one would assume that voters are becoming more digitally
savvy, this might lead to different estimates compared to previous research.
Dataset
We will obtain most of the data from the official website of the canton of St. Gallen and the Swiss
Federal Statistical Office. This includes PDF and CSV files on voting behaviour at municipality level.
The dataset will allow us to examine changes in voter turnout and party shares before and after the
introduction of internet voting in St. Gallen. By comparing municipalities that adopted internet voting
with those that did not (control group), we can use the DiD approach to isolate the effect of internet
voting on electoral participation and party preferences.
We will have to merge the datasets and organize the data into structured format such as a CSV or SQL
database with columns for each feature (municipality, district,…). Then we will inspect the dataset for
missing values and inconsistencies.
Possible preprocessing steps may include:
• Handle missing or incomplete values
• Normalize data where necessary, for example, converting all dates to a uniform format
• Ensure that all municipal IDs match across different data tables if they come from multiple
sources
Method
The basic diff-in-diff specification is going to be: 𝑌 𝑖𝑡 = 𝛼𝑖 + 𝛾𝑡 + 𝛽𝑋𝑖𝑡 + 𝜖𝑖𝑡
• 𝑌 𝑖𝑡 is the outcome variable (voter turnout or voter share) for municipality i at time t.
• 𝛼𝑖 is a municipality fixed effect and 𝛾𝑡 a time fixed effect that controls for common shocks.
• 𝑋𝑖𝑡is a dummy that is set to one if internet voting is available.
• 𝜖𝑖𝑡 is an idiosyncratic error term.
The key assumption with DiD is that in the absence of the policy change, the differences between the
treatment and control group should remain constant. While this assumption can never be verified,
we will look at the pre-trends to provide evidence in favour or against the assumption.
We will then expand this basic specification with additional control variables to see if the results re-
main robust.
