# JC-School_District_Analysis
Module 4, intro to Pandas!

 # Project Overview

 ### This challenge reviewed a set of School Distrcit data compiled in csv, to evaluate students and High Schools performance and therefore allocate budget accordingly. Furthermore, the analysis was done a second time with the purpose of removing potential fraudulent results from a particular High School.

 # Resources:
 **Data source** All data used in this analysis is in the [Resources](https://github.com/juanitacosmica/JC-School_District_Analysis/tree/main/Resources) folder.
 **Software** Python 3.7, Anaconda 4.11.0, Jupyter Notebook and Pandas.
  
# Results: 

After all the anaylsis was finalized, it was brought to the analyst attention that the 9th grade students from Thomas High School had misbehaved and therefore their results were fraudulent; with this, the analysis had to be ran a second time to remove their grades from the calculations and results. Note: The full 9th grade score turned to "NaN".

The Analysis without removing Thomas High School were as follows:

![Old Districts Summary](/Resources/old_district_summary.png)

The 9th grade grades were replaced with 'NaN" using the loc method:

![Removing the 9th grades from Thomas High School](/Resources/replace_loc.png)

And with this removal and following the calculations as done during the initial analysis, the new district summary ended up as:

![New Districts Summary](/Resources/new_district_summary.png)

- Thomas High School scores were removed from the calculations, this translated in changes to the results for the District and Thomas High School:
    - The overall passing percentage was 65%, it decreased by 0.1% to 64.9%
    - The reading passing percentage was 86%, it decreased by 0.3% to 85.7%
    - The math passing percentage was 75%, it decreased by 0.2% to 74.8%
    - The spending ranges had a slight 0.1% decrease in the % Overall Passing budget between $630 and $644, from 62.9% to 62.8%
        ![Old spending ranges](/Resources/new_spending_ranges.png)
        ![New spending ranges](/Resources/new_spending_ranges.png)
    - The scores by school size and type remained unchanged
        ![No changes in scores by schoool size](/Resources/scores_school_size.png)
        ![No changes in scores by schoool type](/Resources/scores_school_type.png)


# Summary:

The wholesome and integrity of the data allows to conclude with 100% accuracy, instead of having removed the 9th grade scores and students, it would have been ideal to identify which students were faulty and assign scores (perhaps 0) accordingly, this way the results are more transparent. When the 9th grade scores were replaced with NaN at Thomas High School, the students without scores were also removed, and therefore, the overall results decreased by 0.1% to 0.3%, which is not as significant (once again, another method would have resulted in more accurate numbers but the methodology was suggested so the average and final results did not have a huge impact caused by dishonesty).

The code can be found in the [PyCitySchools_Challenge.ipynb](https://github.com/juanitacosmica/JC-School_District_Analysis) file.