# (Titanic Data set)
## by (Hassan Ali)


## Dataset

 the data set we used for this project is titanic data set which provide information about each persons like age,Sex,did he/she survived or not [source](https://www.kaggle.com/c/titanic/data)
<br>
## Feature information
`Survival`:0 = didn't survive, 1 = survived
`pclass`:Ticket class 1 = 1st, 2 = 2nd, 3 = 3rd
`sex`:the gender of the passnger (male or female)
`Age`:Age of each passnger
`sibsp`: number of siblings / spouses aboard the Titanic
`parch`: number of parents / children aboard the Titanic
`ticket`:Ticket number
`fare`:Passenger fare
`cabin`:Cabin number
`embarked`:Port of Embarkation `C = Cherbourg`, `Q = Queenstown`, `S = Southampton`

further information taken from the [source](https://www.kaggle.com/c/titanic/data)
pclass: A proxy for socio-economic status (SES)
1st = Upper
2nd = Middle
3rd = Lower

age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

sibsp: The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

parch: The dataset defines family relations in this way...
Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children traveled only with a nanny, therefore parch=0 for them.

## Data wrangling 
the source of data provided us with three CSV file (`train`,`test`,`gender_submission`)
* we assigned the `gender_submission` to the test data to make the number of the column the same as the train set
* we merged the train set and test set(after adding the new column ) 
* We checked for NaN value in each column and after that, we decided to drop the `cabin` column because it contains the most `NaN` value
* we also dropped the raws with `Age`==NaN and `Embarked`=NaN
### FEATURE ENCODING
the `Survived` column we encoded 
* 0-`didn't survive`
* 1-`did survive`
### FEATURE ENGINEERING 
* we created a new column called the `Family`<br>
* which is the sum of `SibSp` + `Parch` and it will indicate to the family size that was on the ship<br>
* when we create the new column we will add `1` to give indicate to that passenger is only one from his family on this ship <br>
and if it `2` that means he and one of his family members are on the ship and the same goes from 3 or 4,...<br>
<br>
after all of that the data we used for the exploration part contains (1043 row, 12 columns)<br>
we did merge the train and test and used the finale merged data frame as the final data<br>

## Summary of Findings
* we can say that most survived gender is female
* we can say that most most gender that did not survive is male
* Furthermore, half of our data were men and did not survive with percentage =54%
* the most common port for male and female passenger to embark from was  S-Southampton<br>
* the most common port that people emparked from did survive and did not was  S-Southampton<br>
* half of the passenger were men that embarked from the S-Southampton port with `50% percentage from our data` set<br>
* the most gender of the passengers that `didn't survive` and embarked form `S-Southampton port` were `male` with a `43%` percentage form all data set<br>
* the most gender of the passengers that `did survive` and embarked form `S-Southampton` port was `female` with a `20%` percentage form all data set<br>
* the most family size  that survived and didn't survive for both the female and male passenger was = 1 meaning by that the most affected people by survived and didn't survive rate was the solo passenger <br>
## Key Insights for Presentation<br>
we started the presentation with a plot to tell us what is the dominated gender in our data set, after that, we investigate what is the most survived and didn't survive gender in our data set. then we investigated what is the port that most passenger that embarked from it from and after that we investigate what is the common (age, family size, gender) for the passenger that emparked from that port


