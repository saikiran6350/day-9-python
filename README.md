# day-9-python
import numpy as np
import pandas as pd
df = pd.read_csv('D:\exams.csv')
df
gender	race/ethnicity	parental level of education	lunch	test preparation course	math score	reading score	writing score
0	female	group D	some college	standard	completed	59	70	78
1	male	group D	associate's degree	standard	none	96	93	87
2	female	group D	some college	free/reduced	none	57	76	77
3	male	group B	some college	free/reduced	none	70	70	63
4	female	group D	associate's degree	standard	none	83	85	86
...	...	...	...	...	...	...	...	...
995	male	group C	some college	standard	none	77	77	71
996	male	group C	some college	standard	none	80	66	66
997	female	group A	high school	standard	completed	67	86	86
998	male	group E	high school	standard	none	80	72	62
999	male	group D	high school	standard	none	58	47	45
1000 rows × 8 columns

 
import seaborn as sns
import matplotlib.pyplot as plt
#import seaborn as sns
#import matplotlib.pyplot as plt
sns.stripplot(x = 'reading score',y = 'writing score',data = df)
plt.title("ratio")
plt.show()

#HISTOPLOT
sns.histplot(df['math score'])
plt.title('Distribution of math score')
plt.show()

# STRIP PLOT
sns.stripplot(x = 'gender',y = 'math score',data = df)
plt.show()

 
#JOINT PLOT
sns.jointplot(x='math score',y='writing score',data=df,color='orange')
plt.show()

#VIOLIN PLOT
sns.violinplot(x = 'reading score',y = 'writing score',data = df)
plt.show()

 
