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
The user study actual data are available in the files:
Solutions to Coding Tasks: G1-JGXS.csv, G2-GXSJ.csv, G3-SJGX.csv, G4-XSJG.csv, 
Survey: SurveyResponsesAnon.xlsx

The goal of this study was to analyze the effectiveness of our tool to assist in coding tasks. The objects were the APIs and their
usage summaries in our tool Uminer, Stack Overflow, Official documentation, and via Search Engines. The subjects were the participants who each completed four coding tasks.

## Four Coding Tasks 
Our design was a between-subject
design, with four different groups of participants (G1, G2, G3, G4), each
participant completing four tasks in four different settings.

Each task was required to be completed using a pre-selected API. Thus for the four tasks, each participant needed to use four different APIs: Task1 using Jackson, Task 2 using Gson, Task 3 using Xstream, and Task 4 Spring framework. Jackson and Gson are two of the most popular Java APIs for JSON parsing. Spring is one of the most popular web framework in Java and XStream is well-regarded for its efficient adherence to the JAXB principles, i.e., XML to JSON conversion and vice versa.

### Task Description
TJ using Jackson: Write a method that takes as input a Java Object
and serializes it to Json, using the Jackson annotation
features that can handle custom names in Java object
during deserialization.

TG using GSON: Write a method that takes as input a JSON string and
converts it into a Java Object. The conversion should
be flexible enough to handle unknown types in the
JSON fields using generics.

TX using Xstream: Write a method that takes as input a XML string and
converts it into a JSON object. The solution should
support aliasing of the different fields in the XML
string to ensure readability

TS using Spring: Write a method that takes as input a JSON response
and converts it into a Java object. The response
should adhere to strict JSON character encoding
(e.g., UTF-8).

All of the four APIs can be found in the list of top 10 most discussed APIs in our evaluation corpus. The APIs are mature and are
fairly large and thus can be hard to learn. The largest API is the Spring framework 5.0.5 with a total of 3687 types (Class, Annotation,
Exception, and Annotation), followed by Jackson 2.2 (467 types), XStream 1.4.10 (340 types), and Gson 2.8.4 (34 types). For Jackson
API, we counted the code types that are shipped with the core modules (jackson-core, databind, and annotations). The Jackson API has
been growing with the addition of more modules (e.g., jackson-datatype). The four APIs have a total of 4528 types. In comparison, the
entire Java SE 7 SDK has a total of 4024 code types, and the entire Java SE 8 SDK has a total of 4240 code types


###  Distribution of coding tasks per group per setting. 
SO = Stack Overflow, DO = Javadoc, TOOL = Our Tool, EV = Everything. TJ,
TG, TX, TS = Task Using Jackson, GSON, XStream, Spring, resp.
↓ Group | Setting → SO DO TOOL EV
G1 TJ TG TX TS
G2 TS TJ TG TX
G3 TX TS TJ TG
G4 TG TX TS TJ

## Online Google Doc Forms to Conduct the Study
The anonymized Google doc forms are available here:
1. https://goo.gl/forms/13vuqcQGAgpQV8gr2
2. https://goo.gl/forms/QK3qS5laeAz2c1Ny1
3. https://goo.gl/forms/CAh2HrIgeOPorN8D2
4. https://goo.gl/forms/TNFSVXqBqX7vQusY2

For each group, a seven page instruction guide is produced and shared with each participant to ensure they understood the task requirements. Once a participant completed the coding tasks, he was invited to share his/her experience of using our tool and the API resources they used in their coding task in a separate Google doc form. Each participant was asked to share his/her unbiased opinion.

## Study Design
### Task Selection Rationale. 
The four tasks were picked randomly from our evaluation corpus of 22.7K Stack Overflow posts. Each
task was observed in Stack Overflow posts more than once and was asked by more than one developer. Each task was related to the
manipulation of JSON inputs using Java APIs for JSON parsing. The manipulation of JSON-based inputs is prevalent in disk-based,
networked as well as HTTP-based message, file, and object processing. Therefore, the Java APIs for JSON parsing offer many complex
features to support the diverse development needs. The solution to each task spanned over two posts. The two posts are from two
different threads in Stack Overflow. Thus the developers could search in Stack Overflow to find the solutions. However, that would
require those searching posts from multiple threads in Stack Overflow. All of those tasks are common using the four APIs. Each post
related to the tasks was viewed and upvoted more than hundred times in Stack Overflow. To ensure that each development resource
was treated with equal fairness during the completion of the development tasks, we also made sure that each task could be completed
using any of the development resources, i.e., the solution to each task could be found in any of the resources at a given time, without
the need to rely on the other resources.

### Coding Guide. 
A seven-page coding guide was produced to explain the study requirements. Before each participant was invited to
complete the study, he had to read the entire coding guide. Each participant was encouraged to ask questions to clarify the study details
before and during the study. To respond to the questions the participants communicated with the first author over Skype. Each participant
was already familiar with formal and informal documentation resources. To ensure a fair comparison of the different resources used
to complete the tasks, each participant was given a brief demo of [TOOL] before the beginning of the study. This was done by giving
them an access to the [TOOL] web site.

### Data Collection Process. 
The study was performed in a Google Form, where participation was by invitation only. Four versions of
the form were generated, each corresponding to one group. Each group was given access to one version of the form representing the
group. The developers were asked to write the solution to each coding task in a text box reserved for the task. The developers were
encouraged to use any IDE that they are familiar with, to code the solution to the tasks. 

Before starting each task, a participant was asked to mark down the beginning time. After completing a solution the participant was
again asked to mark the time of completion of the task. The participant was encouraged to not take any break during the completion of
the task (after he marked the starting time of the task). To avoid fatigue, each participant was encouraged to take a short break between
two tasks. Besides completing each coding task, each participant was also asked to assess the complexity and effort required for each
task, using the NASA Task Load Index (TLX)

### Participants
Each of the studies was conducted separately. The survey was conducted after the participants completed their coding tasks. The 31
participants in the coding tasks are divided into four groups (G1-G4). Each of three groups (G1, G3, G4) had eight participants. Among
the 31 participants, 18 were recruited through the online professional social network site, Freelancer.com. The rest of the participants
were recruited from four universities. Each participant had a background
in computer science and software engineering. The number of years of experience of the participants in software development ranged between less than one year to more than 10
years: three (all of them being students) with less than one year of experience, nine between one and two, 12 between three and six,
four between seven and 10 and the rest (nine) had more than 10 years of experience. Among the four participants that were not actively
involved in daily development activities, one was a business analyst (a freelancer) and three were students (university participants). The business data analyst had between three and six years of development experience in Java. The diversity in the participant occupation
offered us insights into whether and how [TOOL] was useful to all participants in general.

### Study Data Analysis

We analyzed each solution to a coding task using three metrics:
1) Correctness. How accurate is the provided solution to support the coding task?
2) Time. How much time was spent to code the solution?
3) Effort. How much effort was required to code the solution?

## Coding Task Summary Results

Participants showed better performance when using [TOOL] only, than when using every available resources
(which included [TOOL], formal documentation, Stack Overflow, and Search Engines) during the coding tasks. The participants
reported that they were familiar with Stack Overflow and the official documentations, but that they needed time to learn [TOOL]. Thus,
they may have started exploring those resources before resorting to [TOOL] for their coding solution when they were allowed to use
all the resources. Several participants mentioned that they found the coding tasks to be difficult. This difficulty contributed to the lower number of participants providing completely accurate solution.

The correctness of the provided solutions were the lowest when participants used only Stack Overflow.
Participants on average spent the highest amount of time and effort per coding solution when using only the formal
documentation. The lowest correctness while using Stack Overflow shows the difficulties that the participants faced to piece together
a solution from multiple forum threads that may not be discoverable (e.g., they are not connected together). Since the formal
documentation did have all the solutions, it was a matter of finding and piecing those solutions together.

The participants spent less time while using [TOOL], than the other resources for the two tasks (TG, TS). For
the task TX, participants spent on average 19.4 minutes using [TOOL] was the second best behind (17.3 minuties) only Stack
Overflow (the lowest completion time). 

## Survey Summary Analysis
The survey was conducted in a Google doc form. We invited
the participants who completed the coding tasks to participate
in the survey. We asked them the following three questions
to capture their opinion based on their experience.
Our focus was to understand whether and how [TOOL] could
be adopted into their daily development tasks.

 The analytics-based documentation approaches in [TOOL] moti-
vated the respondents to decide to use Opiner. According to
one participant “[TOOL] is a splendid tool to use. It provides
great features and functionalities to solve different tasks so that
i will use it”. The unfamiliarity to [TOOL] (because it’s a new
tool) motivated the other participants to be hesitant about using
Opiner on a daily basis. According to a participant: “I am a
new user of [TOOL]. So, at this moment I am not so sure about
using it for my daily development tasks.” Four participants
(i.e., 12.9%) did not want to use [TOOL], because to them
it was redundant or Opiner does not simply have as large
user base as Stack Overflow has. According to one such
participant, “I already have everything available from google
search..."

 The participants considered that [TOOL]
summaries present the huge volume of data from Stack
Overflow in a usable format. According to one participant:
“it provides huge data in a presentable format”. According
to another participant, the advantage of [TOOL] is that it can
provide a single platform for the diverse information API
resources found in Internet: “[TOOL] is useful in the sense
it is providing information about API’s at a single platform.
One don’t have to search over the internet and compare by
themselves. [TOOL] does that task” The combination of big
data prsentation with a search interface was important for
another participant: “Helps in finding answers easily and in
presentable format,more options”
