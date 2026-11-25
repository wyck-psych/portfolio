
The principles for detection include foundational assumptions about how the detector works and normative principles concerning how we want the detector to function and how the results should be used. 

---
### Foundational Assumptions

**First, all detectors utilize some kind of dataset with observed variables as inputs**. Often, detection works with tabular data containing rows of observations and columns of features. Many process data features can be captured as time-stamped event data, which is more difficult to work with as they require more sophisticated models. Detection methods often make specific assumptions about the data, such as whether it is labeled and how much contamination (i.e., the percentage of observations which are anomalies) there is. 

**Second, all detectors utilize some concept of an observation being "genuine" or anomalous**. Some detectors are designed with the intention of making minimal theoretical assumptions (i.e., more data-driven, nonparametric, or exploratory), which leads to broader applicability and the potential to identify previously unknown forms of anomalies. Other detectors are designed with specific forms of anomalies in mind, such as detecting examinees using pre-knowledge cheating in exams and identifying the compromised items. Detection may also involve multiple kinds of genuine or anomalous observations. For instance, a detector for AI-related behavior in online platforms may want to identify multiple forms of AI-assisted, AI-agent, and genuine responding. Researchers at CloudResearch [(Robinson, 2026)](https://www.cloudresearch.com/resources/blog/bot-detection-taxonomy-survey-research/) propose the following working taxonomy (Figure 1) in which AI-related response behaviors vary along a spectrum of participant engagement as well as falling into four categories. The taxonomy suggests four common types of responding, and also suggests that responses vary along two potentially correlated dimensions, which may be called AI tool use and participant engagement. 

![[CloudResearch Taxonomy Photo.png|697]]
Figure 1: Image from https://www.cloudresearch.com/resources/blog/bot-detection-taxonomy-survey-research/

**Third, all detectors utilize some kind of systematic rule/method for assigning anomaly status to observations**. These rules can be based on psychometric or machine learning models. For example, [[Person-Fit Analysis]] in psychometrics utilizes the patterns of item responses to determine the extent to which observations are consistent with a proposed measurement model. Machine learning detection models often produce numerical scores that represent the degree to which the observation is anomalous. A threshold is used on these scores to assign anomaly status to observations, and the performance of the model is evaluated across a range of threshold values (See [[Receiver Operating Characteristic (ROC) Curve and AUROC]]). 

**Fourth, detection can be thought of in terms of joint distributions**. Whichever input variables we choose to use, they will form joint probability distributions in which certain combinations of values are more common than others. Some joint distribution patterns are associated with genuine or anomalous responding. Thus, the task of building a detector can be thought of as choosing/engineering features which will lead to the most distinguishability between genuine and anomalous joint distributions, which then leads to the most accurate and reliable detection. The difficulty is that the joint distributions in observed data contain a significant amount of both construct-relevant variance (i.e., real variation in genuine or anomalous response behaviors) and construct-irrelevant variance (i.e., noise or measurement error). 

**Fifth, detection is inherently adversarial.** As AI tools improve, their ability to avoid detection may also improve, and individuals may become more adept at using AI tools for unauthorized purposes. Over time, it is likely that simpler detection methods will become insufficient for identifying advanced AI workflows. Additionally, there is a tradeoff between the transparency of the detection method and the detector's long run performance, since detectors which are more transparent may be more easily avoided. 

---
### Normative Principles

**First, there should be fairness across relevant subgroups**. Detection performance should not vary meaningfully with group membership in a way that is irrelevant to the construct(s) of interest. This is akin to [[Differential Item Functioning (DIF)|differential item functioning (DIF)]] in psychometrics. Additionally, detection should account for real variation that *is* related to the construct(s) of interest. For instance, students who are not native English speakers may have different typing patterns; a detector should not unfairly punish these students and should treat these typing patterns as a form of genuine responding. 

**Second, there are ethical concerns with collecting some forms of process data**. Many online platforms already collect process data which have a relatively low risk of abuse, such as mouse or keyboard interactions, and participants agree to the collection of this data when it is appropriately handled. However, some forms of process data have a higher risk of abuse, such as capturing video footage of the participant, as in some online proctored exams. These forms of process data are appropriate for applications in which the security and data quality concerns justify their collection and use. In general, most of the process data types that are likely to be useful for detection are not as sensitive and are more easily defensible. In general, data should only be collected and used when there is a sufficient justification, and detectors should involve as few variables as possible to achieve the goals of detection. 

**Third, if the results of a detector are to be used for decision making, then the detector requires evidence and argumentation supporting the reliability, validity, and fairness of the detection method for a specific application.** The evidence and argumentation should align with the Standards for Educational and Psychological Testing (AERA, APA, & NCME, 2014). 

**Fourth, the results of a detector should be treated as one source of evidence among other potential sources, and decision-making should not be based solely on the results of the detector, especially for high-stakes applications.** Ideally, decision-making should utilize multiple sources of evidence, and the results of a detector should be used to identify when further investigation is needed. Furthermore, individuals who are flagged should be permitted to appeal the detection result and request further review. 

---
Next [[(2) Data for Detection]]
Next [[(3) Methods for Detection]]
Next [[(4) Evaluating Detection Performance]]

