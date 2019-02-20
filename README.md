# fse2019 online appendix
# Benchmarks

* RQ1_associatedWithoutInvalidWithToolOutputs: for the valid code snippets used in RQ1
* RQ1_discardedWithInvalidFromAssociated: for the invalid code snippets used in RQ1
* RQ2_BenchamrkWithAllToolOutputs: the benchamrk for RQ2 with outputs from each algorithm and baseline
* RQ3_BenchmarkWithToolOutputs: the benchamrk for RQ3 with outputs from the proposed algorithm
  


# Empirical Results Reported in RQ4 
## OfficialDocumentationUsage.xlsx
The spreadsheet shows the code examples and API types found in two official documentation most discussed APIs in our dataset. This information is used in RQ4, such as to understand how many of the mined scenarios are actually covered in the official documentation.

## The User Study
The user study technical report is provide in userstudy_technical_report.pdf

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
