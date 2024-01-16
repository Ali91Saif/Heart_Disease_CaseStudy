# Heart_Disease_CaseStudy
The dataset consists of 303 individuals data Instances. There are 14 columns in the dataset, which are described below.

Age: displays the age of the individual.

Sex: displays the gender of the individual using the following format :
1 = male
0 = female

Chest-pain type: displays the type of chest-pain experienced by the individual using the following format :
1 = typical angina
2 = atypical angina
3 = non — anginal pain
4 = asymptotic

Resting Blood Pressure: displays the resting blood pressure value of an individual in mmHg (unit)

Serum Cholestrol: displays the serum cholesterol in mg/dl (unit)

Fasting Blood Sugar: compares the fasting blood sugar value of an individual with 120mg/dl.
If fasting blood sugar > 120mg/dl then : 1 (true)
else : 0 (false)

Resting ECG : displays resting electrocardiographic results
0 = normal
1 = having ST-T wave abnormality
2 = left ventricular hyperthrophy

Max heart rate achieved : displays the max heart rate achieved by an individual.

Exercise induced angina :
1 = yes
0 = no
ST depression induced by exercise relative to rest: displays the value which is an integer or float.

Peak exercise ST segment :
1 = upsloping
2 = flat
3 = downsloping

Number of major vessels (0–3) colored by flourosopy : displays the value as integer or float.

Thal : displays the thalassemia :
1 = normal
2 = fixed defect
3 = reversible defect

Diagnosis of heart disease : Displays whether the individual is suffering from heart disease or not :
1 = No
0 = Yes.


*************************UNIVARIATE ANALYSIS*******************************

1. age
	- data is normally distributed
	- does not have outliers
	- skewness coefficient is around -0.2, no need of transformation
2. sex
	- data contains details of 206 male and 96 female
	

3. ChestPainType
	-143 patients have typical angina
	-86   patients have atypical angina
	-50   patients have non-anginal pain
	-23   patients have asymptomatic pain

4. Blood Pressure
	- data is normally distributed
	- has outliers
	- skewness coefficient is around 0.7, no need of transformation

5. Cholestoral
	- data is normally distributed and skewd rightwards
	- has outliers
	- skewness coefficient is around  1.15,  needs transformation


6. Bloodsugar
	-257 patients have Bloodsugar
	-45   patients do not have Bloodsugar

7. ECG
	-147  patients have Normal ECG
	-151   patients have ST-T wave abnormality in ECG
	- 4  patients have probable or definite left ventricular hypertrophy

8  Max_heartrate
	- data is normally distributed and skewd leftwards
	- has outliers
	- skewness coefficient is around -0.5,  do not need transformation

9 Ex - Pain
	- 99  patients have Exercise induced Angina
	- 203 patients do not have Exercise induced Angina


10 Thalassemia
	-165   patients have normal blood flow
	-117   patients have reversible defect (a blood flow is observed but it is not normal)
	- 18    patients have fixed defect (no blood flow in some part of the heart)
	



12 Target

	- 138  patients are suffering from heart disase
	- 164  patients do not have heart disase


***************************BIVARIATE ANALYSIS*******************

1. Target Vs Age
	- There exists a significant relationship among them
	- ANOVA
		- statistic=10675.801467178899, pvalue=0.0
		* Very high value suggests significant relationship and reject the Null Hypothesis
	- Point Biserial correlation
		- SignificanceResult(statistic=-0.221, pvalue=0.00)
	- Boxplot has shown the variation in mean accross categories

2. Target Vs BloodPressure
	- There does not exist any significant relationship among them
	- Point Biserial correlation
		- SignificanceResult(statistic= -0.14, pvalue=0.00)
	- Boxplot has shown the  no variation in mean accross categories


3. Target Vs Bloodsugar
	- There does not exist any significant relationship among them
	- - ANOVA
		- statistic=124.8, pvalue=1.95
		* Very Low value suggests no  significant relationship and failed to reject the Null Hypothesis
	- Point Biserial correlation
		- SignificanceResult(statistic= -0.02, pvalue=0.64)
	- Boxplot has shown the  no variation in mean accross categories


4. Target Vs Max_heartrate
	- There exists a significant relationship among them
	- ANOVA
		- statistic=12779.77, pvalue=0.0
		* Very high value suggests significant relationship and reject the Null Hypothesis
	- Point Biserial correlation
		- SignificanceResult(statistic= 0.41, pvalue= 0.0)
	- Boxplot has shown the variation in mean accross categories


5. Target Vs Thalassemia
	- There exists a significant relationship among them
	- chi2 = 84.6
	- pvalue = 0.0
	* High chi2 value with pvalue less than significance level indicated association among them

6. Target Vs No_of_vassels
	- There exists a significant relationship among them
	- chi2 = 73.6
	- pvalue = 0.0
	* High chi2 value with pvalue less than significance level indicated association among them


7. Target Vs slope
	- There exists a significant relationship among them
	- chi2 = 46.8
	- pvalue = 0.0
	* High chi2 value with pvalue less than significance level indicated association among them






