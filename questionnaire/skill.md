---
name: questionnaire
description: enable a interaction mode for background knowlegde to perform an interactive survey about the background knowledge
---

# Objective
Perform an interview with a person on a topic. 

# Parameters
NUMBEROFQUESTIONS = 10
INTERACTIONDURATION = 5min

# Timer

1. start a timer at the beginning of the chat session
2. Check every interaction if the duration is already longer than the configured INTERACTIONDURATION
3. If the duration is not yet passed, continue as usual.
4. If the duration is beyond the limit, then notify the user with a thank you about its feedback and a question if the user wants to continue the survey.
5. If the user indicates that the survey can be continued, follow the instructions of the user about its motivation to continue.

# Survey preparation 

1. read the provided background knowledge
2. If the background knowledge has a survey mode available follow this, otherwise construct a survey with at maximum NUMBEROFQUESTIONS questions.
3. This list is called the reference survey mode.

# next question

To determine the next question the following strategy should be followed. It is composed of 3 aspects.

 - deeping: perform followup questions to get to know more details. To get more information and context of the provided answer
 - continuation: select a next question of the survey list in order to cover the full survey
 - randomisation: as timing may lead to not asking all questions to all respondents, randomisation of the question selection is needed to ensure a broader coverage

The rule for determining the next question is as follows:

1. process the answer and then identify the need for deeping. If possible try deepning
2. if sufficient time is still available continue with the next question in the survey.
3. When the timelimit is nearby perform randomisation to select the following question.


# Interaction


1. Introduce the objective of the survey to the user
2. Initiate the reporting
3. Mention the time limit and initiate the timer
4. Start with the opening question.
5. Process the feedback of the user and determine the next question
6. Stop when all questions are asked, or that timer resulted in a stop

# reporting

1. initiate the reporting by creating a word document containing the initial metadata of the survey taken
2. at each interaction dump the question and respons to the word document

At the end of the survey a word document is presented to the user with the answers and questions the user has provided.
The user is requested to submit this to the reporting email address.


   
