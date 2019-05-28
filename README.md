# Fingerprint Genetics
## Background Information
Fingerprints are patterns formed on human, monkey, and ape appendages. Every human has a unique fingerprint, including identical twins. In fact, unknown suspects can be identified by the fingerprints they leave behind on a crime scene. There are three main pattern types of fingerprints: arch, whorl, and loop. Even though fingerprints are unique to an individual, scientific research shows that there is some genetic relatedness between the fingerprint patterns of parents and their children. Our own research is to explore to what extent genetic relatedness can be determined by fingerprint similarities.
</br> Volar skin contains no hairs or oil glands and is found on the hands and feet of all primates. The overall pattern of the fingerprint is governed by the shape, size, and placement of volar pads. Higher and symmetric volar pads tend to generate whorls, flatter and symmetric volar pads tend to generate arches, and asymmetric volar pads tend to generate loops. It is generally understood that friction ridge patterns are influenced not just by genetic factors but also by random physical stresses and tensions during fetal development. This leads to fingerprint uniqueness. Though there is some randomness, the purpose of our project is to determine the general extent to which genetics influences fingerprints.
</br> The most precise way to determine fingerprint similarity today is with neural networks. However, since neural networks require thousands of data to train, which we did not have the resources to collect, we decided to use the SURF algorithm on OpenCV.
## Factors 
* Loop vs Whorl vs Arch
  * Subtype: Loose vs. Tight vs. Just Whorl; Concavity of Arch
* Direction of shape
* Centeredness of main pattern
* Opencv analysis to determine percent similarity between two fingerprints
## We have two goals 
1. Determine whether genetic relatedness can be established from fingerprint similarity using OpenCV.
2. Determine a pattern of inheritance for fingerprint patterns on the right thumb.
### Goal 1
**Null Hypothesis:** Siblings and strangers have no significant difference between number of fingerprint pattern matches. </br>
**Alternate Hypothesis:** There is a significant difference in the number of fingerprint pattern matches between siblings and strangers. 
### Goal 2
**Hypothesis:** The pattern of inheritance of fingerprint types is random.
## Classification
{ </br>
    "pattern" : ("loop", "tight whorl", "loose whorl", "whorl", "arch), </br>
    "x alignment" : ("left", "center", "right"), </br>
    "y alignment" : ("low", "center", "up"), </br> 
    (specifically for loop) "direction" : ("pointing right", "pointing left"), </br>
    (specifically for whorl) "top loop direction" : ("right", "left"), </br>
    (specifically for whorl) "bottom loop direction" : ("right", "left"), </br>
    (specifically for arch) "concavity" : ("up", "down") 
</br> }
## Materials
We put together 11 Fingerprinting kits, each containing:
* 1 Tape dispenser
* 1 Pen	
* 1 Stamp pad
* 1 Fingerprint template paper
* 1 set of instructions </br>
</br>

We used the Fingerprint Match program (FingerprintMatcher.ipynb) for achieving Goal #1 of the project.
## Procedure
#### *... for goal #1*
1. Distribute fingerprinting kit to sample families.
2. Scan and upload images of individual fingerprints.
3. Evaluate number of matches and percent match between both siblings and strangers using OpenCV.
 * Control: Compare fingerprint to itself to ensure the program runs as intended.
 * Trial 1: Siblings
 * Trial 2: Compare strangers with the same pattern
 * Trial 3: Compare strangers with different patterns
4. Determine if there is a statistically significant difference between the number of matches in trial 1 compared to trials 2 and 3. 
#### *... for goal #2*
1. Distribute fingerprinting kit to sample families.
2. Scan and upload images of individual fingerprints.
3. Evaluate families’ fingerprints to determine phylogenetic inheritance patterns.
## Conclusion
**Goal 1 Conclusion:** Through our Chi-square calculation, we found that p = 0.0001015531577, which is less than our alpha value of 0.05. So, we can reject the null hypothesis that there is no significant difference between the matches of the fingerprints of siblings and strangers. There is statistically significant evidence that our OpenCV program can distinguish siblings from strangers based on fingerprint similarity. Therefore, we can conclude that it is possible to determine genetic relatedness from fingerprint similarity.
</br>
**Goal 2 Conclusion:** From the fingerprint patterns within a family, we observed that many of the offsprings’ fingerprints showed similar patterns as their parents. When one parent has a whorl and the other has a loop, and both kids have whorls, we deduce that loops are recessive to whorls. Continually, if one parent has an arch and the other has a loop, and the children have a whorl and a loop, the arch allele must be recessive to the loop allele, while being dominant to the whorl allele. We found these patterns to be consistent with all the family data we received. However, our pattern seems convoluted (thus unlikely) because the “loop allele” seems to be dominant to the “arch allele,” seems dominant to the “whorl allele,” but the “whorl allele” seems to be dominant to the “loop allele.” In other words, there does not seem to be a simple inheritance pattern. Rather, it seems more likely that fingerprint pattern inheritance is polygenic. Nevertheless, our data supports the conclusion that fingerprint inheritance is not random, but that genetics has some role in fingerprint pattern.
