# Tidyverse Create Assignment:
Create an Example Using one or more TidyVerse packages, and any dataset from fivethirtyeight.com or Kaggle, create a programming sample “vignette” that demonstrates how to use one or more of the capabilities of the selected TidyVerse package with your selected dataset.

# Dataset chosen:

Heart Disease dataset from Kaggle

# Data link from Kaggle:

https://www.kaggle.com/ronitf/heart-disease-uci/data#heart.csv

# Data Features:

There are 14 columns in this dataset and 303 obsevations from individuals. 

**age**:age in years.

**sex**:(1 = male; 0 = female)

**cpchest**: pain type. Type of chest-pain experienced by the individual:
1 = typical angina
2 = atypical angina
3 = non-angina pain
4 = asymptomatic angina

**trestbps**: Resting blood pressure (in mm Hg on admission to the hospital).

**chol**:Serum cholestoral in mg/dl.

**fbs**:(fasting blood sugar > 120 mg/dl) (1 = true; 0 = false).

**restecg**: Resting electrocardiographic results:
* 0 = normal
* 1 = ST-T wave abnormality
* 2 = left ventricle hyperthrophy

**thalach**: Maximum heart rate achieved.

**exang**: Exercise induced angina (1 = yes; 0 = no).

**oldpeak**: ST depression induced by exercise relative to rest.

**slope**: the slope of the peak exercise ST segment.

**ca**: number of major vessels (0-3) colored by flourosopy.

**thal**: 
* 3 = normal 
* 6 = fixed defect 
* 7 = reversable defect

**target**: 1 or 0.

# Target:

Heart disease diagnosis

# Tidyverse Capability 1: dplyr (summarise, tibble)

* Usage:

The summarise or summarize function reduces a data frame to a summary of just one vector or value. Usualy, summarise is used with group_by funtion. 

Tibbles or tbl_df is an alias for as_data_frame but it make things easier in R. Tibbles don’t change variable names or types and have a unique print() method which makes them easier to use with large datasets containing complex objects.

* Demo:

summarise (Mean = mean(Resting_Blood_Pressure ), Max = max(Resting_Blood_Pressure), Mean = mean(Resting_Blood_Pressure ), Variance= var(Resting_Blood_Pressure ), SD= sd(Resting_Blood_Pressure))

as_tibble(Heart)

# Tidyverse Capability 2: ggplot

* Usage:

The ggplot2 package, created by Hadley Wickham, offers a powerful graphics language for creating elegant and complex plots. **ggplot2** allows you to create graphs that represent both univariate and multivariate numerical and categorical data in a straightforward manner.

* Demo:

ggplot(Heart,aes(x= Chest_Pain_Type,fill= Diagnosis_Heart_Disease)) +
  theme_bw() +
  geom_bar() +
  facet_wrap(~Gender) +
  labs(y ="count",
       title = "Heart Disease distribution by Gender based on Chest_Pain_Type")


