# Rubabimran_assignment3
# Lab 3 work1
df_data<- data.frame(
  name= c("Alice", "Bob", "Hauwa", "Hassan", "Sulaiman"),
  age= c(30, 25, 30, 27 ,28),
  location= c("USA", "UK"," Nigeria","Niger", "Togo")
 )
write.csv(df_data, file = "data.csv")

data <- read.csv("~/data.csv")
View(data)

install.packages("readxl")
library(readxl)

library(readxl)
Score <- read_excel("Score.xlsx")
View(Score)

library(dplyr)
df_data_filtered<- filter(df_data, age>20)
df_data_selected<- select(Score, Score)
print(df_data_selected)
data_selected<- summarise(df_data_selected, mean_score=mean(Score))
data_filtered<- filter(Score, Score > data_selected)
print(data_filtered)  
