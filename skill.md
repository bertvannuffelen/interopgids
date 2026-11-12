---
name: interopassessement
description: perform an interop assessment and document it
---

## Objective
Evaluate the information provided by the agent user to perform an interoperability assessment 
based on the background information the agent has.

An interoperability assessment consists of 
  - a scoring against the 6 interop principles (dutch: principes)​‌
  - a scoring against the interoperabilitylayers (dutch: interoparabiliteitslagen)​‌
  - a scoring against the 4 applicationsscenario's (dutch: toepassingsscenarios)
  - a list of 3 to 5 best supported recommendations (ducth: aanbevelingen)
  - a list of 3 to 5 activities that will improve the overall interoperability score (dutch: groeikansen)

## Process

0. at initialisation of the agent: start from a clean context; ensure that previous assessments on the same content do not lead to pointing to the same output document.
1. the agent requests the user to provide all information the user wants to be considered for the assessment
2. the agent performs the assessment by inspecting all provided documents following the rules below
3. the agent stores the assessment in a word document

## Rules

1. use the self-assessment questionnaire to create an initial basis of the assessment
2. use the recommendations to find motivations or indications for support of the principles, interoperabilitylayers and applicationsscenario's.
   
   2.1. first perform the recommendation scoring on all recommendations
   2.2. record for each recommendations the support found
   2.3. perform the application scenario scoring
   2.4. perform the interoperability layer scoring
   2.5. perform the principles scoring
  
4. use the cookbook to identify existing recipes to detect improvement activities

## interoperability scoring

### Recommendation scoring (R scoring)
The scoring for recommendations is

1. The scoring range is between 0 and 5.
2. When there is strong or explicit evidence found in the provided documentation the score is 5
3. When there is moderate evidence in the provided documentation the score is 3
4. When there is an indication of it, the score is 1
5. Otherwise score it 0

### Application scenario scoring (AS scoring)

The scoring range is between 0 and 5.

Step 1: create a generic basic score.
1. Evaluate based on the definition of each application scenario the focus upon the each application scenario.
2. A strong or explicit presence scores is 4
3. A moderate presence scores 3
4. limited or no indication scores 1
5. Compare the assigned scores, and apply the following rule when applicable: For scores higher than 2, when the scoring is equal, compare the support and reduce the one with the least support with 0.5.  
 

Step 2: create an aggregated recommendation support score.

1. Group all recommendations supporting for each application scenario.
2. Calculate the average recommendation score for each application scenario.

Step 3: combined score
The application scenario score is the weighted aggregate =  (0,35 * its generic basic score + 0,65 * its aggregated recommendation score ). 

The combined score is the Application Scenario score.

### Interoperability Layer scoring (IL scoring)

The scoring range is between 0 and 5.

Step 1: create a generic basic score.
1. Evaluate based on the definition of each interoperability layer the focus of the provided information upon the each interoperability layer.
2. A strong or explicit presence scores is 4
3. A moderate presence scores 3
4. limited or no indication scores 1
For scores higher than 2, when the scoring is equal, compare the support and reduce the one with the least support with 0.5.  
 

Step 2: create an aggregated recommendation support score.

1. Group all recommendations supporting for each interoperability layer.
2. Calculate the average recommendation score for each interoperability layer.

Step 3: combined score
The interoperability layer score is the weighted aggregate: (0,35 * its generic basic score + 0,65 * its aggregated recommendation score ). 

The combined score is the Interoperability layer score.

### Principles scoring (IP scoring)

The scoring range is between 0 and 5.

Step 1: create a generic basic score.
1. Evaluate based on the definition of each principle the focus of the provided information upon the each principle.
2. A strong or explicit presence scores is 4
3. A moderate presence scores 3
4. limited or no indication scores 1
For scores higher than 2, when the scoring is equal, compare the support and reduce the one with the least support with 0.5.  
 

Step 2: create an aggregated recommendation support score.

1. Group all recommendations supporting for each principle.
2. Calculate the average recommendation score for each principle.

Step 3: combined score
The principle score is the weighted aggregate: (0,40 * its generic basic score + 0,60 * its aggregated recommendation score ). 

The combined score is the principle score.


## exclude
 - do not include a roadmap or planning. 
 - do not include a visual representation.  
Inform the user if requested that this is a task for a next agent.

## Output 

a word document consisting of 
  - a description of the assessed project and the resources used
  - a scoring against the 6 interop principles (dutch: principes)​‌
  - a scoring against the interoperabilitylayers (dutch: interoparabiliteitslagen)​‌
  - a scoring against the 4 applicationsscenario's (dutch: toepassingsscenarios)
  - a list of 3 to 5 best supported recommendations (dutch: aanbevelingen)
  - a list of 3 to 5 activities based on the recipes in the cookbook that will improve the overall interoperability score (dutch: groeikansen)
  - the full list of all recommendations with their level of support. Include for each recommendation the evidence that supports the level of support.
  - a list of documents that are missing that could improve the scoring.

Filename word document pattern: InteropAssessemnt-{shorthandProject}-{date}-{time}.{extension}



## Notes

