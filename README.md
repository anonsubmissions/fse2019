# fse2019 online appendix
# Benchmarks
## rq1: 
This folder contains the benchmark and labels used to answer RQ1.

## BenchmarkRQ2. 
The benchmark we used to answer RQ2.

## BenchmarkRQ3
The benchmark we used to answer RQ3

# Empirical Results Reported in Section V
## SnippetAssignedToFimAndClones.pkl
This python pickle file contains the empirical evidence of code clones we found in our Java+JSON dataset, that we discussed in Section VI. You can open it as follows:

```
with open('SnippetAssignedToFimAndClones.pkl', 'rb') as f:
  data = pickle.load(f)
```

After that, use `data.keys()` to explore the keys inside.

## ValidSnippetsWithErrorInfo.pkl
This python pickle file contains all the valid and invalid code snippets with error information as logged by our Hybird Code Parser (described in Section III-B)

## OfficialDocumentationUsage.xlsx
The spreadsheet shows the code examples and API types found in two official documentation most discussed APIs in our dataset. This information is used in Section VI, such as to understand how many of the mined scenarios are actually covered in the official documentation.

# The User Study
We answered the following research question:
How useful is the tool with the mined API usage scenarios to support development tasks?

The goal of this study was to analyze the effectiveness of our tool to assist in coding tasks. The objects were the APIs and their
usage summaries in our tool Uminer, Stack Overflow, Official documentation, and via Search Engines. The subjects were the participants who each completed four coding tasks.

## Raw Data of Responses
A total of 31 developers (18 professional) participated in the study. Each developer completed four coding tasks. The 31 participants are divided into four groups (G1-G4). Each of three groups (G2, G3, G4) had eight participants. The other group (G1) had eight participant, but one developer could not participate at the end. The responses of each group can be found in the online appendix folder [User Study Responses](https://github.com/anonsubmissions/icse2019/tree/master/User%20Study%20Responses).   


## Four Coding Tasks 
Each task was required to be completed using a pre-selected API. Thus for the four tasks, each participant needed to use four different APIs: Task1 using Jackson, Task 2 using Gson, Task 3 using Xstream, and Task 4 Spring framework. Jackson and Gson are two of the most popular Java APIs for JSON parsing. Spring is one of the most popular web framework in Java and XStream is well-regarded for its efficient adherence to the JAXB principles, i.e., XML to JSON conversion and vice versa.

## Online Google Doc Forms to Conduct the Study
The anonymized Google doc forms are available here:
1. https://goo.gl/forms/13vuqcQGAgpQV8gr2
2. https://goo.gl/forms/QK3qS5laeAz2c1Ny1
3. https://goo.gl/forms/CAh2HrIgeOPorN8D2
4. https://goo.gl/forms/TNFSVXqBqX7vQusY2

For each group, a seven page instruction guide is produced and shared with each participant to ensure they understood the task requirements. Once a participant completed the coding tasks, he was invited to share his/her experience of using our tool and the API resources they used in their coding task in a separate Google doc form. Each participant was asked to share his/her unbiased opinion.

## Design of the study 
Our design was a between-subject design, where each participant in a group completed four tasks in a setting different from the other groups.For example, group 1 completed Task 1 using Stack Overflow, Task 2 using API official documentation, Task 3 using our tool, Task 4 using everything including search engines (e.g., Google). Group 2 completed Task 1 using our tool (Uminer), Task 2 using Stack Overflow, etc. 

## Evaluation Criteria
We assessed the effectiveness of each resource to assist in the coding tasks along three dimensions: 

1. Correctness of the provided coding solution: We considered a solution as correct if it adhered to the pro-
vided specification and strived for functional correctness.

2. Time taken to complete a coding task: We defined the time spent to complete a coding task using
a given development resource as the total time took for a participant (1) to read the task description, (2) to consult the
given development resolution for a solution and (3) to write the solution in the provided text box of the solution.

3. Effort spent to complete a coding task: We defined the effort spent to complete a coding task using a given development resource as how hard the participant had to work to complete the task. We analyzed the effort using the NASA TLX index which uses six measures to determine the effort spent to complete a task. TLX computes the workload of a given task by averaging the ratings provided for
six dimensions: mental demands, physical demands, temporal demands, own performance, effort, and frustration.

## Summary of Results 
A total of 124 coding solutions were provided by the 31 participants. From there, we discarded 14 as invalid solutions (i.e.,
link/wrong API). Out of the 124 reported time, we discarded 23 as being spurious. 24 participants completed the TLX metrics
(providing 96 entries in total), with each setting having six participants each. 

We share some key results below from the study. More results can be shared.

While using our tool, the participants on average coded with more correctness (62.3%), spent less time (18.6 minutes per coding task) and less effort (45.8). The pair-wise comparison between the resources show that the difference is statistically significant between our tool and API official documentation based on the effort spent. The correctness of the provided solutions
were the lowest when participants used only Stack Overflow, showing that the increasing size of Stack Overflow is becoming a problem for developers to get quick and correct solutions. Participants on average spent the highest amount of time and effort per coding solution when using only the formal documentation. 

More than 85% of the respondents agreed that our mined usage screnarios offer improvements over formal API
documentation to assist in their development activities. The participants considered learning an API could be quicker while using our tool  than while using Stack Overflow, because our tool synthesizes the information from Stack Overflow by APIs using both sentiment and source code analyses. According to one participant 
> It is quicker to find solution in Uminer(our tool) since the subject is well covered and useful information is collected.

14 participants (45.2%) decided that they would use Uminer online tool in their daily development tasks because of
analytics based on sentiment analysis and machine learning, usability, and richness of contents. The developers praised the
usability, search, and analytics-driven approach in Uminer. The gain in productivity via analytics was highlighted by the
participants as a motivation to use Uminer. According to one participant: 
> In depth knowledge plus the filtered result from Uminer can easily increase the productivity of daily development tasks, as it recommends most recently asked questions from Stack Overflow with the quick glimpse of the positive and negative feedbacks.



