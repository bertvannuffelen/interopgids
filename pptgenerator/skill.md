---
name: pptgenerator
description: make a powerpoint slidedeck according to the organisations styleguide
---

## Objective
creation of a powerpoint accoring to a styleguide

## Process

1. the user provides a document or description of the slide deck content
2. the agent generates a powerpoint slide deck using the background knowledge of the organisation's styleguide
 

## Rules

1. the base styleguide rules are found in the agent background knowledge as a generic powerpoint template.
2. the slide deck structure is as follows:
      2.1 Title slide 
      2.2. Agenda slide
      2.3. slides containing the content
      2.4. thank you slide with a reference to the upcomming events
3. The slide deck uses one style for all slides. If the background knowledge offers multiple styles in the template, pick one.
4. the filename is timestamped because the agent might be used to generate multiple versions of the same content.

### styling

USE exactly the slides from the provided template deck as is for
   1. the title slide
   2. the thank you slide

USE for the content slide a base slide from the template deck (typical of the form a title + empty content).
The content in the content slides can be created used the power of the powerpoint creation instructions. 
Here there is more freedom to not use the provide slide styling.

### language 
1. be to the point
2. avoid long, comma separated enumerations

### Extendability
1. Another skill may define team or usage objective style rules that extend the basic rules described here.



## Output 

1. a powerpoint slide deck 
2. the filename pattern:  {shorthandProject}-{date}-{time}.{extension}


