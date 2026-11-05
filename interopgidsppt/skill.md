---
name: interopassessmentpptx
description: make a powerpoint slidedeck documenting an interopassessment 
---

# Configuration parameters
The following parameters should be filled in by the agent before performing its objective.

TEMPLATEFILE
INTEROPGIDS

## Objective
creation of a slidedeck describing the interopassessement 

## Process

1. the user provides a document or description of the slide deck content
2. the agent generates a powerpoint slide deck according to the rules described below
3. the agent requests a feedback from the user about the generated content
 

## Rules

### Explicit reuse of the slides 1, 2 en 4 from the TEMPLATEFILE

use slides 1, 2 and 4 of the TEMPLATEFILE directly and completely within the new slidedeck.

"directly and completely" means:
1. copy the original slides, not just there appearrance. 
2. Maintain for each slide the original slide-layout, slide-master and other visual elements.
3. Do not rebuild these copied slides again with new textboxes, shapes or images.
4. Do not create a visual lookalike or derivative
5. Do not change positioning, size or style
6. Only replace the placeholdertexts with the appropriate content from the interopassessment.
7. If the content does not fit the provided placeholder:
    - reduce or reformulate first the content
    - never change the template layout to make the content fitting
    - the only approapiate action is to apply a font resizing (smaller)   

Use the slide 3 from the TEMPLATEFILE as basis for the content slides.

### the expected structure of the slide deck

- Slide 1: titlepage on the basis of slide 1 in TEMPLATEFILE 
- Slide 2: agenda on the basis of side 2 in TEMPLATEFILE
- Slide 3 and following: content slides on the basis of slide 3 in TEMPLATEFILE
- final slide: A thank you slide with a reference to a next event on the basis of slide 4 in TEMPLATEFILE

### The content slides

The following content slides are minimally to be created
1. an overview slide indicating in 3 figures the assessment on the principles, interoperability layers and application scenarios.
2. an slide indicating the best supported recommendations
3. an slide indicating the recommended advices for improvement
4. an slide to discuss one or more of the recommended advices whether or not the project responsible agrees with it and whether this is an investment worth

additional optional slides
- motivation why this assessment was performed
- slide with references to the information used


## Style guide 
1. use the icons from the INTEROPGIDS to support the principles, layers and application scenario's.
2. use color the layers according to the color scheme in the INTEROPGIDS
3. use stable colors throughout the slides for indicating the level of support found (from purple red to grass green)

## events
1. use https://www.vlaanderen.be/digitaal-vlaanderen/agenda/evenementen/interoperabiliteit?order_startdate=asc to find the key events that can be used to be placed on the last slide
2. ask the user to select one
3. create a QR code for that selected event


## MANDATORY conformancecheck for the styling

Apply a technical and visual check on the style of the generated slides. In particular the slides 1, 2 and the last one. 

### Technische check 

Compare each generated slide with the original corresponding source slide in the TEMPLATEFILE.

Check at least:
- used slide-layout;
- linked slide-master;
- images

A slide is only conform when the template structure has been maintained and only the placeholder content has been adapted.


The following cases are considered not conform:

- use the same colors but different layout;
- a rebuild slide
- removal of template elements
- the use of layout that only visually is comparable.
  
### Visual check

- Render the full deck to images
- compare the slides 1, 2 and the last slide with the corresponding template slides
- Check for shifts of objects, different sizes, missing elements and unwanted whitespace.

### Decision

When at least one of the slides 1, 2 and the last is technical or visually non conformant,
inform the user about this.


## Output 




## Notes
