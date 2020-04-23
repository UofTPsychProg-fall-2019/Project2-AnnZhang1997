## Project2-AnnZhang1997

# About the Files
MTMMice.csv is the original data.
MTM.Rmd is the R markdown file containing the data processing pipeline.
MTM.pdf is the result file you get after running the pipeline.

# About my project
My experiment seeks to demonstrate multiple time of day memory in mice through behaviour testing.
48 subject mice are divided into 4 experiment groups, differing in the type of stimulus and the time of day that they are tested for. Data are collected from two experiment sessions for each mice:

1. The habituation session before any stimulus has been given
2. The testing session after the mice had received training of the stimulus

Each session lasts for ten minutes, during each the subject mouse will have free access to two chambers, the paired chamber in which the mouse receives training of the stimulus during the training, and the unpaired chamber in which the mouse does not receive any stimulus. The time each subject mouse choose to spend within each chamber is recorded in seconds.

# About the Data
The original data in MTMMice.csv includes:
The slot position (slot) and the subject number (subjectnum) of each mice; the time and the pattern of chamber in which the mice received preference (CPP) or avoidance (CPA) stimulus training, the stimulus (Teststim) the mice was tested for during the testing session; whether the testing time matches the training time (TestON); how many seconds did each mouse spent in the chamber paired with the stimulus and the chamber not paired with the stimulus during the habituation session (hab-paired and hab-unpaired) and the testing session (test-paired and test-unpaired).

# About the Data Processing Pipeline

Once the rmd file is run, it generates a pdf file that includes four sections.
1. Summary of the Results
In this section, a table is generated that summarises the average and standard deviation of the time each group of mice spent within the paired chamber and the unpaired chamber during the testing session and the habituation session.

2. Effect of Chamber Patterns on Chamber Preference
In this section, the mean and standard deviation of the time mice spent within each pattern-type chamber. One-way ANOVA is then performed on the results and a bar graph is generated. As all the chambers used in the experiment are identical except for the pattern on their walls, the aim of this section is to prove that there is no inherent preference or avoidance for the patterns.

3. Effect of Conditioning on Chamber Preference
In this section, the average and standard deviation of time that each group of mice spent within the paired and unpaired chamber during the habituation and testing session  is calculated.Two-way ANOVA is then performed and a bar graph is generated.By comparing whether there is a significant difference in dwell time between testing and habituation, it could be shown whether training would have an effect on the preference of the chambers. By comparing whether the results for the testing session is significantly different for the cpp group and the cpa group, it could be shown whether the type of stimulus would have an effect on the preference of the chambers.

4. Effect of the Time of Day on Chamber Preference
In this section, the data of the testing session are grouped into four groups depending the stimulus the subjects are tested for and whether the testing time matches the training time. Within each group, the difference between the dwell time in the paired chamber and the unpaired chamber is calculated. This average dwell-time-difference for the subjects that were tested at Circadian Time 4 and Circadian Time 11 was calculated within each group and  compared using t-test.Box graphs are plotted to visualize the data.