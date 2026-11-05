---
name: dataConformsStandard
description: make an conformity check of data
---

# Objective
Assess the conformance of a representative data sample with the expected data layer of GovOS 

# Procedure

1. the user provides the data that needs to be assessed.
2. The agent will perform the representative check
3. the agent performs a conformance check of the provided data following the phases in the order: 
   2.1. It performs the detailed assessment phase
   2.2. It will perform the feedback phase
   2.3. It will perform the aggregation phase
4. the agent will create a report documenting its findings


# representativeness check
Prior performing the conformance check the agent will asked the user about the representativeness of the provided data.

It will check 
1. The completeness of the data. Is this a full data dump, or a representative sample, or a view (single API request), etc ?
2. The presence of exceptional cases if the data is not complete
3. The presence of additional data exchange mechanisms of the data.

The agent only starts the conformance check when the user explicitly has conformed to have provided all information about the representativeness of the provided data.

# Conformance check rules

## detailed assessment phase
The agent assess each question in the provided Excel file and 
1. records the amount of support for it.
2. record a counter example when found

## feedback phase 
Based on the detailed assessment the agent identifies potential missing evidences.
The agent will ask the user to provide additional evidence, or to conform that evidence does not exist.
A maximum of 3 missing evidences are to be requested to the user.  

## aggregation phase
The agent will aggregate the support for the questions according to the dimensions and the conformance principles.

It calculates a score for the conformance to the principles:
- a question for which the amount of support could not be determined due to lack of evidence, is labeled ignored.
- a question for which little support and the presence of counter examples is scored 0
- a question for which in some cases there is support but in others not is scored 1
- a question for which in all cases there is support is scored 3

The scoring for a principle is calculated as SUM/TOTAL where 
   SUM = the sum of all score for questions supporting the principle, and 
   TOTAL = 3 * the amount of questions that support the principle.
In this score are the questions which are labeled ignored, excluded.

For each principle a summary of the good support and missing support is created based on the information found by the questions.

## report generation phase
The report form is a word document containing the following sections

1. the assessment metadata: Who performed the assessment, when it happened, with with version of the conformance check , etc.
2. the assessed data: it describes the provided data and it representativeness
3. the detailed assessment per question: a table containing for each question the level of support, motivation, score and eventually counter examples
4. the aggregated scoring: for each dimension the aggregated score and the summary on the good support and missing support 
5. a visual radar diagram presenting the aggregated score
6. a conclusion with 3 to 5 advices to improve the conformity





