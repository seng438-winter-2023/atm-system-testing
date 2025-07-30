> **SENG 438 - Software Testing, Reliability, and Quality**

# Exploratory, Functional, & Regression Testing of an ATM System 🕵️‍♂️

 ## 📚 Project Summary
This project involved testing a simulated **ATM system** as part of a university software testing course. We performed exploratory, manual functional, and regression testing across two versions of the application (``v1.0`` and ``v1.1``) by running the provided JAR files (``ATM System - Lab 1 Version 1.0.jar`` and ``ATM System - Lab 1 Version 1.1.jar``) under the ``seng438-a1-artifacts.zip`` package. Using JIRA as our bug tracking tool, we wrote detailed defect reports, validated bug fixes, and practiced collaborative testing workflows in a team environment.

![Status](https://img.shields.io/badge/grade_achieved-A%2B-success?style=flat-square)

## 🛠️ Tools & Concepts Practiced
- **Exploratory testing** (unscripted, high-level functional checks)
- Manual scripted **functional testing** based on use cases defined in [`seng438-a1.md`](./seng438-a1.md)
- **Regression testing** to verify bug fixes in version `1.1`
- Defect tracking and documentation using **JIRA**
- Writing detailed **bug reports** with reproducible steps, expected vs. actual results
- Pair testing and collaborative QA workflows
- Testing critical banking operations (e.g., withdrawal, deposit, transfer)


**📝 The full defect report can be found in** [`DefectReport-Group30.pdf`](./DefectReport-Group30.pdf)

_Screenshot of one entry from the defect report below:_

<img width="527" height="705" alt="defect-repot-1 1" src="https://github.com/user-attachments/assets/18d4be95-d655-453c-a1fb-25ac70e4d38c" />
<img width="526" height="375" alt="defect-report-1" src="https://github.com/user-attachments/assets/1a680807-0c2e-4bc2-9c07-e187946e953f" />

## 🏧 System Under Test
_Screenshot of the system under test_

![system](https://github.com/user-attachments/assets/16ea4f7b-80b9-415d-a571-32bae8e9aaae)

---


## 📄 Assignment Report Begins Below

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 30      |
|-----------------|
| Student 1: Aayush Dahal                |   
| Student 2: Justin Kuhn              |   
| Student 3: Sheroze Nasir               |   


## 📑  Table of Contents

- [Introduction](#introduction)
- [High-level description of the exploratory testing plan](#high-level-description-of-the-exploratory-testing-plan)
- [Comparison of exploratory and manual functional testing](#comparison-of-exploratory-and-manual-functional-testing)
- [Notes and discussion of the peer reviews of defect reports](#notes-and-discussion-of-the-peer-reviews-of-defect-reports)
- [How the pair testing was managed and team work/effort was divided](#how-the-pair-testing-was-managed-and-team-workeffort-was-divided)
- [Difficulties encountered, challenges overcome, and lessons learned](#difficulties-encountered-challenges-overcomed-and-lessons-learned)
- [Comments/feedback on the lab and lab document itself](#commentsfeedback-on-the-lab-and-lab-document-itself)


# Introduction

In this assignment, our group applied fundamentals of testing we learnt in week 1 & week 2 to test an ATM system(``v1.0`` and ``v1.1``). We applied testing & software engineering knowledge to find faults in the system and reported them in a bug tracking system. The different types of tests performed were Exploratory Testing, Manual Scripted Testing, and Regression Testing. The first step for us was to familiarize ourselves with the system under test (ATM system) as well as the bug tracking system (JIRA).  To familiarize ourselves with the system under test, we read the detailed explanation of the SUT in the lab document and also read the high level requirements of the system under Appendix B. To solidify our understanding, we performed various normal ATM operations on the JAR file of the ATM System. To familiarize ourselves with JIRA, we read an article, “The Ultimate Jira Bug Tracking Tutorial”, and then created an account to familiarize ourselves with the UI and to also try out things we learnt in the article.  Next we performed our first type of test, exploratory tests. Before starting exploratory testing, we decided on a high level plan on how we want to test the system at this stage. We were aware that tests are designed and executed at the same time in exploratory testing without strict plans & constraints, however, we also knew that it was good practice to decide on a high level testing plan before carrying out the testing. Our group had a collective understanding that the point of exploratory testing is for the developer to incrementally create scenarios related to operations of the system to manually test if the software fails or passes the scenario at hand. Next, we performed our second type of test, Manual Scripted Testing. Our group was aware that in scripted testing, a plan with a suite of test cases and steps to execute the test cases are pre written, and the tester is to follow the plan without digressing from it. Lastly, we performed Regression testing. From past courses and experience, our group was familiar with the concept of regression testing. We knew that regression testing is a type of testing mechanism that is used to examine if previously found bugs have been fixed, without creating any new bugs in the existing functionality of the system. During regression testing, our group had an opportunity to test version ``1.1`` of the system. On this step, we re-tested all bugs from version ``1.0`` that we reported in JIRA as well as all the 40 test cases from the scripted testing stage. This gave us an opportunity to check if old bugs were fixed in the new version and also if any new bugs were introduced.

# High-level description of the exploratory testing plan

For exploratory testing, we planned on testing most observable functionality of the system with more emphasis on core functionalities that define the system and are a must for the system to function. For instance, some questions we wanted to answer were, is the correct amount transferred from one account to another?, does it transfer funds to & from the correct account? etc. We also focused on testing the common paths of the system, i.e, combinations and order of inputs that users are most likely to use day-to-day in an ATM system. The most common paths are operations that users will most frequently encounter and are what defines a system. Testing most common paths/core functionality first then focusing on the nice-to-haves goes well with the idea of the popular agile manifesto as this approach allows for delivery of a functional product first. Since, most bugs live on the edge, we also put emphasis on testing edge cases. Working as a team works well with the exploratory testing method. This is because each team member can focus on a different portion of the system under test, and afterwards compare their results to produce bug reports of the whole system in a quick manner. The purpose of exploratory testing is not to debug every possible input in every possible state, but rather to verify that the core functionalities that define the system work as intended.

# Comparison of exploratory and manual functional testing

In general, exploratory testing presents a more broad perspective of software testing. It is not exhaustive, and its primary goal is to test the core functionalities that a system is built off of. It does not follow a script, but rather operates by users testing whatever comes to mind, as long as it is logical to do so. Conversely, manual functional testing is the strict following of a script in order to perform tests. This is where individual functions get tested repeatedly with varying inputs, and system states are explored in much more depth. Relative to the provided test suite, the given test cases were more specific than the exploratory tests, and involved putting oneself in situations that users would rarely encounter during a normal run of the program. For example, one of the test cases was “User enters correct pin on third try”, and another was “A deposit transaction can be canceled by the customer at any time prior to inserting an envelope”. These situations are more obscure, and did not occur to any group member during the exploratory test phase. Comparing these two testing methods, each one has advantages/disadvantages over the other. Exploratory testing is faster and overall less demanding, but manual functional testing is more thorough, complete and will likely find more bugs in the end. Manual functional testing tries to be exhaustive. Even though it can’t test every possible input, it spends a good amount of time on edge cases and values that users wouldn’t normally enter. Deciding which method of testing is better overall is subjective and varies on a case-to-case basis. In an agile team, where working software is demanded at a fast pace, exploratory testing may be sufficient as there is more emphasis on the core functionalities of the system. Additionally, in an environment where developers are receiving constant feedback, there will always be opportunity to fix bugs in the loop of sprint cycles. However, in a waterfall team, where customer feedback is not received until the end of the project, manual functional testing is required as it is essential that the final product is well-tested and as bug-free as it can be. As well, large scale projects that involve sensitive client information, such as a banking system should also be tested with manual functional testing. This is because bugs/exploits that are not patched may have a catastrophic effect, and customers will not feel secure using software that is not thoroughly tested. In our testing, we found that exploratory testing found more bugs, however, performing regression tests was easier on manual scripted tests since they were well-documented. 

# Notes and discussion of the peer reviews of defect reports

- Firstly, the defect reports for the exploratory testing phase between pairs had a consistent format, and this is because the format of the defect report was discussed beforehand as the pair went their way to perform tests.
- Both pairs tested common/core ATM functionalities such as:
    - Turning system on/off
    - Entering a readable/unreadable card
    - Entering an invalid/valid pin
    - Withdraw/Deposit/Transfer/Balance Inquiry
- The reason both pairs tested these functionalities is because our exploratory testing plan was to focus on functionalities that define the system (core functionalities)	
- The defect reports between pairs were as detailed and specific as possible. This was agreed upon beforehand so that the bug reports between pairs maintained a consistent level of quality, as would be expected in an industry.
- In our testing, we found that the update to version ``1.1`` of the system was relatively ineffective, as only 3 existing bugs were fixed in the new release.
- Although both groups mostly ended up testing the same functionalities, both groups missed cases that the other group was able to find, and we were able to discuss this during the peer review stage. 
    - For instance, when both groups tested the Transfer functionality, group 1 found the defect where the wrong amount was transferred between accounts, and group 2 found the defect where the to and from accounts got switched up during the operation.


# How the pair testing was managed and team work/effort was divided 

Since, we had 3 members in our group, we took an adjusted approach for pair testing as well as the whole group assignment. For pair testing, we decided to make one group of 2 testers and then another individual tester to test on their own. Before performing the Exploratory Tests, we collectively came up with a high level testing plan as well as some high level test cases we wanted to ensure were covered. Then, we went off and started testing! When both groups completed performing the exploratory tests and reporting bugs in JIRA, we came together as a group and discussed and ran through all the test cases each group tested and the bug report for each bug found. Through the exploratory testing phase, each team wrote down and kept track of all the test cases they performed and all of those that failed in a Google Doc to keep organized and to help aid our discussions.

For Manual Script Testing, we split into our 2 people and 1 people group as before, and assigned one group scripted test cases 1-20 and the other group scripted test cases 21-40. If a bug was encountered in the system by any group for any test case, a detailed bug report was written in JIRA with “MFT” on the title with the description of the bug, the function being tested, how to reproduce, expected and actual outcome etc. 

During the Regression Testing stage, we again split up into our 2 people and 1 people group. Each group was assigned to perform regression testing on version ``1.1`` of the system with all test cases they tested in stage 1(exploratory testing) and stage 2(manual scripted testing). If a previously failed test case was fixed in version ``1.1``, the bug report in JIRA of the corresponding bug got marked “DONE”. If a previously failed test case was not fixed in version ``1.1``, the bug report in JIRA of the corresponding bug got marked “IN PROGRESS” and a note stating that the bug still exists in version ``1.1`` was added by members performing regression testing,

Note: One principle we tried to follow when dividing work was, to the extent the circumstances allow, give team members the freedom to pick work that they expertise in and they enjoy doing.

# Difficulties encountered, challenges overcomed, and lessons learned

- A major difficulty we encountered was scheduling. Since our group was created at the last possible moment we didn't have as much time to work on it. Since everyone in the group was also busy with other classes we needed to create an efficient schedule with the time that was remaining. We learned to make sure to start assignments earlier so that we would not need to worry about this issue.

- Another difficulty we encountered was that some of our group members were unfamiliar with the bug tracking tool JIRA, thus, there was a little learning curve. To overcome this challenge, team members experienced with JIRA helped other team members get familiar with the tool and they also demonstrated how to create a bug report, and the reasoning behind why JIRA is used. This interaction between members truly demonstrated the importance of working in a team and being open and willing to help each other.

- A major lesson we learnt from this lab is the importance of using a project management/bug tracking tool like JIRA. With a lot of bugs, it is difficult to keep track of them, thus,  JIRA provides an all in one platform where you can report your bugs, format the description, story point it, assign team members to it, track progress etc. This lab taught us and demonstrated the importance of a bug tracking tool, especially while working on a team as it helps keep everything organized and well documented. 

- Another lesson we learnt is the importance of thinking outside the box and coming up with edge test cases. At first, our group neglected edge test cases, however, later when we re-grouped and decided on performing certain edge test cases, we were able to find more bugs in the system. This taught our group that bugs almost certainly live in the edge, and as test engineers we should always prepare well thought out edge test cases.

# Comments/feedback on the lab and lab document itself
- The lab was very good at helping us learn the fundamentals of exploratory, scripted, and regression testing.
- The lab was exceptional in demonstrating how testing is done in a team environment and the lab provided students a basic understanding of how to use a bug reporting tool like JIRA, how to write effective bug reports, as well as how to track progress. 
- The lab also gave students hands on training on how to effectively work and communicate within a software team.
- The assignment description was clear and concise. The testing guide for each testing method was easy to follow.

_This testing project was a joy to work on ❤️_
