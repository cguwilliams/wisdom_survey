#Wisdom and mental/somatic experience

##Define the problem
Is there an association between experience with certain mental and somatic practices and  
wisdom?

##Define the dataset
**Dependent Variables**: Wisdom Total, Cognitive, Affective, and Reflective  
**Primary predictor variables**: Practice type, Years of experience, total hours of experience  
**Mediating variables**: Cognitive and affective empathy, trait anxiety, mindfulness

##Determine what data can be accessed
Data for *meditators* taken from meditation centers across the U.S.  
Data for *ballet dancers* taken from dance centers and listservs across the U.S.  
Data for *Alexander Technique* taken from teachers and students across the U.S. through  
listservs, mailing lists, and advertisements in AT material  
Data for *Feldenkrais Method* taken from website devoted to the practice, as well as email and  
listservs  

##obtain data
Data obtained from SurveyMonkey across 10 collectors  
**Bolded items** are questionnaires used in the final survey analysis to date

###Alexander Technique **(N=113)**  
####ATFullBatt\_Raw.csv (N=24)   
* **Year began** *will need to be transformed to years experience, if still practicing* 
* **Hours experience**  
* **MAAS**   
* **RMET** 
* **QCAE**  
* **Trait anxiety**  
* **3DWS** (*missing two questions. Anchored (1)Strongly Agree to (4) Strongly Disagree*)  
* Subjective Happiness  
* Satisfaction with life  
* Justice  (JUST11-20 not included)
* Emotional contagion  
* Emotional regulation  
* Locus of control (1-30; 3-scales)  
* Complexity of human nature  
* Prosocial personality index    

####ATSurv\_Raw.csv (N=56)  
* **Year began** *will need to be transformed to years experience, if still practicing*
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **RMET**
* **3DWS** *(1)Strongly disagree to (5)Strongly Agree*  
* Locus of Control (1-10)
* CHN  

####ATSurvNews\_Raw.csv (N=33)  
* **Years experience**
* **Hours experience**
* **QCAE**  
* **MAAS**  
* **TA**  
* **RMET**  
* **3DWS** *(1)Strongly disagree to (5)Strongly Agree*  
* Locus of Control (1-10)  
* CHN  
 
###Ballet **(N=122)**  
####Ballet01\_Raw.csv (N=60)  
* Changed ballet styles from numerated (different numbers for each kind of dance style)  
 to 1's
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS**
* **RMET**
* Locus of Control (1-10)
* CHN

####Ballet02\_Raw.csv (N=62) 
* Changed ballet styles from numerated (different numbers for each kind of dance style)  
 to 1's
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS**
* **RMET**
* Locus of Control (1-10)
* CHN 

###Feldenkrais Method **(N=147)**  
####Feld01\_Raw.csv (N=79)  
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS** *missing ReflW11*
* **RMET**
* Locus of Control (1-10)
* CHN 

####Feld02\_Raw.csv (N=68)
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS** *missing ReflW11*
* **RMET**
* Locus of Control (1-10)
* CHN 

###Meditation **(N=123)**  
####MedFullBatt\_Raw.csv (N=28)  
* **Year began** *will need to be transformed to years experience, if still practicing* 
* **Hours experience**    
* **RMET** 
* **QCAE**  
* **Trait anxiety**  
* **3DWS** (*missing two questions. Anchored (1)Strongly Agree to (4) Strongly Disagree*)  
* Subjective Happiness  
* Satisfaction with life  
* Justice 
* Emotional contagion  
* Emotional regulation  
* Locus of control (1-30 3-scales)  
* Complexity of human nature  
* Prosocial personality index   

####MedShort01\_Raw.csv (N=44)  
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS** *missing ReflW11*
* **RMET**
* Locus of Control (1-10)
* CHN 

####MedShort02\_Raw.csv (N=51)  
* **Years experience**
* **Hours experience**
* **QCAE**
* **MAAS**
* **TA**
* **3DWS** *missing ReflW11 and AffW13 missing most data*
* **RMET**
* Locus of Control (1-10)
* CHN 

##clean data
1. *setup consistent labels for every variable across each collector above*
2. *Create separate files for each questionnaire*
3. **Merge files within practice by questionnaire or demographics/experience info**
	* Add ID column for practice type: 1=AT, 2=Ballet, 3=Feldenkrais, 4=Meditation
	* Some scales differ from the initial data collection (full batteries) and shortened later versions
		1. QCAE - Same across all collectors. Reverse-score items 1, 2, and 29. Original key says to reverse score  
		everything!
		2. MAAS - Non-existant in Meditation Full Battery. These meditation data have been excluded from analysis.  
		Ranges from **almost always to almost never** in AT Full Battery, but the opposite in every other  
		survey
			* Do NOT reverse score for AT Full Battery.
			* Reverse score for everything except AT Full Battery.
		3. TA   - Scales are consistent across all collectors. Original reverse-scoring scheme used for the  
		submitted paper was incomplete. In original key: Reverse-score items 10, 13, 14, 16, 19. Actual  
		scheme appears to be: Reverse-score items 1, 3, 6, 7, **10, 13, 14, 16, 19,** 20
		4. 3DWS - For the first two collectors, the anchors were switched, leading to different reverse-scoring schemes
			* Standard reverse scoring scheme - CogW: All; ReflW: 1, 2, 7, 9, 10; AffW: 1, 2, 3, 5, 6, 8, 9, 10, 11, 12
			* Reverse scoring scheme for Full Battery AT and Med - CogW: none; ReflW: 3, 4, 5, 6, 8; AffW: 4, 7, 13
		5. RMET - Consistent across all collectors (not yet used in analysis)
		6. LOC  - Consistent across all collectors (not yet used in analysis)
			* Reverse score 3, 6, 8, 10
		7. CHN  - Consistent across all collectors (not yet used in analysis)
			* Reverse score 8-14
4. Merge  files across practices by questionnaire or demographic/experience info
5. Reverse score where called for
6. ATFullBatt_Raw WIS scores interpolated from 1-4 to 1-5.
	* *1=1;2=2.34;3=3.64;4=5*
7. Compute compound (average) scores for every participant, per dataset (separated as above)
	* Using R-function script
8. Create a tidy data file with only compound scores and demographic/experience info