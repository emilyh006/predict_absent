## **Dataset Dictionary**

This dataset dictionary has been customized specifically for the purposes of this project. For the official data dictionary, please refer to [the original source.](https://www.cdc.gov/yrbs/media/pdf/2023/2023_National_YRBS_Data_Users_Guide508.pdf)

#### 

Mental Health: Questions: 26-30, 84, 106  
Home Context: Questions: 89-91, 99-102, 104  
Social Context: Questions: 14, 16, 19, 20-25, 88, 103, 105  
Health: Questions: 76-78, 85

##### **Modular Clustering:**

Clean Dataset (no missingness): dat\_cleaned  
Final Recoded Dataset: dat\_final

###### **Scaled Subsetted Datasets:**

Mental Health \+ Home Context: X\_home  
Mental Health \+ Social Context: X\_social  
Mental Health \+ Health: X\_health

##### **Exploratory Clustering:**

Full Dataset: dat  
Cleaned and Trimmed (no missingness, dropped QN\# and QNword cols): dat2\_cleaned  
Final Recoded Dataset: dat2\_final

## **Recoding Dictionary**

#### **Mental Health**

Directionality: Negative. As you go up the scale, it indicates poor mental health.

| Question/ Data type  | Original Values | Recode Values |
| :---- | :---- | :---- |
| 26-28, 106 \[Binary\] | 1.0 \= Yes  2.0 \= No | 1 \= Yes  0 \= No  |
| 29, 84  \[Ordinal\]  | Suicide Attempt (1-5) Poor Mental Health (1-5) | NO CHANGE  |
| 30  \[Categorical but not Ordinal\] | 1.0 \=  I did not attempt suicide during the past 12 months 2.0 \=  Yes \[attempted and need treatment\] 3.0 \=  No \[attempted but no treatment\]  | For consistent directionality  0 \=  I did not attempt suicide during the past 12 months 1 \= \[attempted but no treatment\] 2 \= \[attempted and need treatment\] |

#### **Home Context**

Directionality: Negative. As you go up the scale, it indicates a poor home environment.

| Question/ Data type  | Original Values | Recode Values |
| :---- | :---- | :---- |
| 89-91 \[Ordinal\] | Violence (physical/environment) (1-5) | NO CHANGE  |
|  99, 104  \[Ordinal\] |  Basic Needs Met, Parental Attention (1-5) (Never → Always)  | Reverse Scale   (1-5) (Always → Never) 1: 5 2: 4 3: 3 4: 2 5: 1 |
| 100-102  \[Binary\] | Parents with Issue/ Absent  1.0 \= Yes  2.0 \= No |  1 \= Yes  0 \= No  |

### 

#### **Social Context**

Directionality: Negative. As you go up the scale, it indicates a poor social environment.

| Question/ Data type  | Original Values | Recode Values |
| :---- | :---- | :---- |
| 14, 16 \[Ordinal\] | Safety in school (1-5) Physical fight (1-8) | NO CHANGE |
| 19 \[Binary\] | Sexual coercion 1.0 \= Yes  2.0 \= No | 1 \= Yes  0 \= No  |
| 20, 23, 103 \[Ordinal\] | Sexual coercion, anyone (1-5), Sexual coercion, romantic (1-6), Physical violence, romantic (1-6), Bullying, race/ethnicity (1-5) Closeness to schoolmates (1-5)  | NO CHANGE |
| 24, 25, 88, 105 \[Binary\] | Bullying, Cyberbullying, Sexual assault 1.0 \= Yes  2.0 \= No | 1 \= Yes  0 \= No  |

### 

#### **Health**

Directionality: Negative. As you go up the scale, it indicates low physical activity. 

| Question/ Data type  | Original Values | Recode Values |
| :---- | :---- | :---- |
| 76 \[Ordinal\] | 1hr Physical Activity (1-8) (0 days → 7 days)  | Reverse Scale (1-8) (7 days → 0 days) 1: 8 2: 7 3: 6 4: 5 5: 4 6: 3 7: 2 8: 1 |
| 77 \[Ordinal\] | Days of PE (1-6) (0 days → 5 days)  | Reverse Scale (1-6) (5 days → 0 days) 1: 5 2: 4 3: 3 4: 2 5: 1 |
| 78 \[Ordinal\] | Sports teams (1-4) (0 teams → 3+ teams)  | Reverse Scale (1-4) (3+ teams → 0 teams) 1: 4 2: 3 3: 2 4: 1  |
| 85 \[Ordinal\] | Hours of sleep (1-7) (4 or less hrs → 10 or more hrs) | Risk Score (distance from optimal sleep) (1-7) (4 or less hrs ← 7, 8, 9 hrs → 10 or more hrs) 1: 3 2: 2 3: 1 4: 0 5: 0 6: 0 7: 1 |

#### **Full Dataset**

Previously recoded variables included in dataset and shown *again* in table.  
Excluded from exploratory cluster analysis. Questions: 6, 7, 37, 45\. RACEETH \<= look into

| Question/ Data type  | Original Values | Recode Values |
| :---- | :---- | :---- |
| 18, 19, 24, 25, 26, 27, 28, 31, 35, 88, 100, 101, 102, 105, 106,  \[Directional Binary\] Yes \= potentially more risk/harm | Violence in neighborhood, Rape, Bullying, Cyberbullying, Hopelessness, Suicidal thoughts, Suicide plan, Cigarette, Vape, Parent Alcoholic, Parent Mental Illness, Parent Imprisioned, Unfairly disciplined, Executive functioning 1.0 \= Yes  2.0 \= No | 1 \= Yes  0 \= No  |
| 56 \[Neutral Binary\] Just an interpretative distinction tbh ◡̈ | Had sex 1.0 \= Yes  2.0 \= No  | 1 \= Yes  0 \= No ({1: 1, 2: 0}) |
| 9, 10, 11, 12, 13, 14, 15, 16, 17, 20, 21, 22, 23, 29, 33, 34, 36, 38, 39, 40, 42, 43, 44, 46, 48, 49, 50, 51, 52, 53, 54, 55, 58, 59, 61, 68, 69, 70, 71, 72, 73, 74, 75, 79, 80, 84, 89, 90, 91, 92, 93, 95, 98, 103, 107 \[Directional — Ordinal\] As you go up the scale, it indicates poor mental health / risk behavior  | Car alcohol, Driving alcohol, Text drive, Carry weapon in school, Carry gun, Safety school, Threatened with weapon, Physical fight, Physical fight at school, Sexual assault, Sexual assault romantic, Physical violence romantic, Bullying Race/Ethnicity, Suicide attempt, Days smoked cigarette, Amount smoked cigarette, Days vaped, Tobacco, Days smoked cigar, Alcohol/Month, Drunk/Month, Total \# drinks, Weed, Weed/Month, Pain medicine, Cocaine, Inhalants, Heroin, Methamphetamines, Ecstasy, Needle drugs, Lifetime sexual partners, 3mo sexual partners, Condom, Juice, Fruit, Salad, Potatoes, Carrots, Vegetables, Soda, Breakfast, Concussion, Social Media, Poor mental health, Family insult, Family physical violence, Home physical violence, Unprescribed medicine, Hallucinogenic, Sports drink, Sunburn, Closeness at school, English ability | NO CHANGE |
| 8, 76, 77, 78, 96, 97, 99, 104,  \[Directional Reverse-Score — Ordinal\] As you go up the scale, it indicates poor mental health.   | Seat belt, Physically active, PE, Sports teams, Water, Strength training, Basic Needs, Parental monitoring,  | Reverse Score |
| 1, 3,  \[Ordinal/Categorical — Neutral Numeric\] Data is ordered but not directional. | Age, Grade, |  |
| 2, 4, 5, 63, 64, 67,  \[One-hot\] Unordered, non-directional data, we use dummies. | Sex, Hispanic/Latino, Race, Sexual Id history, Sexual orientation, Weight action,   |  |
| 30, 60, 94 \[Special Case\] | 1.0 \=  I did not attempt suicide during the past 12 months 2.0 \=  Yes \[attempted and need treatment\] 3.0 \=  No \[attempted but no treatment\]  1 \= I have never had sexual intercourse 2 \= Yes \[used substances before sex\] 3 \= No \[did not use substances before sex\] 1 \= I have never had sexual contact 2 \= Yes 3 \= No | For consistent directionality (As you go up the scale, it indicates poor mental health): 0 \=  I did not attempt suicide during the past 12 months 1 \= No \[attempted but no treatment\] 2 \= Yes \[attempted and need treatment\] 0 \= I have never had sexual intercourse 1 \= No \[didn't use substances\] 2 \= Yes \[used substances before sex\] 0 \= I have never had sexual contact 1 \= No 2 \= Yes ({1: 0, 3: 1, 2: 2}) |
| 32, 41, 47, 57,  \[Special Case\] | Age cigarette, Age alcohol, Age marijuana, Age sex,  1 \= I have never smoked a cigarette, not even one or two puffs / I have never had a drink of alcohol other than a few sips / I have never tried marijuana / I have never had sexual intercourse 2 \=  8 years old or younger 3 \= 9 or 10 years old 4 \= 11 or 12 years old 5 \= 13 or 14 years old 6 \= 15 or 16 years old 7 \= 17 years old or older | For consistent directionality (As you go up the scale, it indicates poor mental health) and considering 0=haven’t tried before: ({1: 0, 2: 6, 3: 5, 4: 4, 5: 3, 6: 2, 7: 1}) 0 \= I have never smoked a cigarette, not even one or two puffs / I have never had a drink of alcohol other than a few sips / I have never tried marijuana / I have never had sexual intercourse 1 \= 17 years old or older 2 \= 15 or 16 years old 3 \= 13 or 14 years old 4 \= 11 or 12 years old 5 \= 9 or 10 years old 6 \=  8 years old or younger |
| 62 \[Special Case\]  | 1 \= I have never had sexual intercourse with an opposite-sex partner 2 \= No BC method 3 \= BC pills 4 \= Condoms 5 \= IUD 6 \= Shot / Injection 7 \= Withdrawal 8 \= Unsure | 0 \- 2 Custom Risk Scale ({1: 0, 3: 1, 4: 1, 5: 1, 6: 1, 2: 2, 7: 2, 8: 2}) 0 \= I have never had sexual intercourse with an opposite-sex partner 2 \= No BC method 1 \= BC pills 1 \= Condoms 1 \= IUD 1 \= Shot / Injection 2 \= Withdrawal 2 \= Unsure   |
| 65 \[Special Case\]  | 1 \= No, I am not trans 2 \= Yes I’m trans 3 \= I’m not sure 4 \= Idk what you’re asking | Special Binary Recoding 0 \= No, I am not trans 1 \= Yes I’m trans 0 \= I’m not sure 0 \= Idk what you’re asking ({2: 1, 1: 0, 3: 0, 4: 0})  |
| 66 \[Special Case\] df\['Q66\_recode'\] \= df\['Q66'\].map({ 	1: 2,  \# Very underweight \= high risk 	2: 1, 	3: 0,  \# About right \= baseline 	4: 1, 	5: 2   \# Very overweight \= high risk }) | 1 \= Very underweight 2 \= Slightly underweight 3 \= About the right weight 4 \= Slightly overweight 5 \= Very overweight | Custom U-Shaped Risk Scale ({1: 2, 2: 1, 3: 0, 4: 1, 5: 2}) 2 \= Very underweight 1 \= Slightly underweight 0 \= About the right weight 1 \= Slightly overweight 2 \= Very overweight |
| 81, 82 \[Special Case\]  | Have you been tested for HIV?, Have you been tested for any sexually transmitted diseases? 1 \= Yes 2 \= No 3 \= Not sure | Special Binary Recoding (similar to Q65) 1 \= Yes 0 \= No 0 \= Not sure  |
| 83 \[Directional with tweak\] | When was the last time you saw a dentist for a check-up, exam, teeth cleaning, or other dental work? 1 \= During the past 12 months 2 \= 12-24 mo ago 3 \= 24+ mo 4 \= Never 5 \= Not sure | 1: 0, 2: 1, 3: 2, 4: 3, 5: 3  |
| 85 \[Special Case\] | Hours of sleep (1-7) (4 or less hrs → 10 or more hrs) | Risk Score (distance from optimal sleep) (1-7) (4 or less hrs ← 7, 8, 9 hrs → 10 or more hrs) 1: 3 2: 2 3: 1 4: 0 5: 0 6: 0 7: 1 |
| 86 \[Special Case\]  | 1 \= In my parent's or guardian's home 2 \= In the home of a friend, family member, or other person because I had to leave my home or my parent or guardian cannot afford housing 3 \= In a shelter or emergency housing 4 \= In a motel or hotel 5 \= In a car, park, campground, or other public place 6 \= I do not have a usual place to sleep 7 \= Somewhere else | Custom Risk Scale 1: 0, 2: 1, 3: 2, 4: 3,  5: 4, 6: 5, 7: 3 |
| 87 \[Special Case\] grades\_map \= { 	1: 0,  \# Mostly A's 	2: 1, 	3: 2, 	4: 3, 	5: 4,  \# Mostly F's 	6: 4,  \# None of these → conservatively scored high risk 	7: 4   \# Not sure → conservative estimate of disengagement/risk } | 1 Mostly A's 2 Mostly B's  3 Mostly C's  4 Mostly D's  5 Mostly F's  6 None of these grades  7 Not sure | ​​Directional: Lower grades \= higher risk for 0 Mostly A's 1 Mostly B's  2 Mostly C's  3 Mostly D's  4 Mostly F's  4 None of these grades  4 Not sure |

