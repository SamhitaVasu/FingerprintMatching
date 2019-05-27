# FingerprintMatching
## Background Information:
Fingerprints are patterns formed on fingers of human, monkey, or ape appendages. Every human being on this planet has a distinct and unique fingerprint. This means that not one person has the same fingerprint as another, including identical twins. In fact, unknown suspects can be identified by the fingerprints they leave behind on a crime scene. There are three main pattern types of fingerprints: arch, whorl, and loop. Even though fingerprints are specific to an individual, scientific research shows that there is some genetic relatedness between these fingerprint patterns of parents and their children. Our own research is to explore to what extent genetic relatedness can be determined by fingerprint similarities.
## Factors: 
* Loop vs Whorl vs Arch
  * Subtype: Loose vs. Tight vs. Just Whorl; Concavity of Arch
* Direction of shape
* Centeredness of main pattern
* Opencv analysis to determine percent similarity between two fingerprints
## We have two goals: 
#1. Determine whether genetic relatedness can be established from fingerprint similarity using OpenCV. </br>
#2. Determine a pattern of inheritance for fingerprint patterns on the right thumb.
### Goal 1
**Null Hypothesis:** Siblings and strangers have no significant difference between number of fingerprint pattern matches. </br>
**Alternate Hypothesis:** There is a significant difference in the number of fingerprint pattern matches between siblings and strangers. 
## Classification
{ </br>
> "pattern" : ("loop", "tight whorl", "loose whorl", "whorl", "arch), </br>
> "x alignment" : ("left", "center", "right"), </br>
> "y alignment" : ("low", "center", "up"), </br> 
> (specifically for loop) "direction" : ("pointing right", "pointing left"), </br>
> (specifically for whorl) "top loop direction" : ("right", "left"), </br>
> (specifically for whorl) "bottom loop direction" : ("right", "left"), </br>
> (specifically for arch) "concavity" : ("up", "down") </br>
< }
