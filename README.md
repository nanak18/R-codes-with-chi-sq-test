Project work I did with a few mates with the topic effects of social media on students mental health using R programming for the data analysis
# R-codes-with-chi-sq-test
##import dataset 
library(readxl)
grp8 <- read_excel("C:/Users/Lord Benyah/Desktop/social media.xlsx")
View(grp8)
###converting cartegorical data to factors
grp8$`1. What is your age?`=as.factor(grp8$`1. What is your age?`)
A=table(grp8$`1. What is your age?`)
percentages=round(A/sum(A)*100)
percentages
grp8$`2. Gender`=as.factor(grp8$`2. Gender`)
B=table(grp8$`2. Gender`)
B
percentages=round(B/sum(B)*100)
percentages
names=c("Female","Male")
C=paste(names,"",percentages,"%",sep="")
View(C)
pie(B,labels =C,main = "Piechat To Show Gender Distribution",col=c("blue","red"))
grp8$`3. What is your level of study?`=as.factor(grp8$`3. What is your level of study?`)
D=table(grp8$`3. What is your level of study?`)
D
V=round(D/sum(D)*100)
name=c("1st year","2nd year","3rd year","4th year","5th year","6th year")
E=paste(names,"",V,"%",sep="")
barplot(D,main="The Level of Education",legend.text =c("5th Year","1st Year","4th Year","2nd Year","6th 
Year","3rd Year"),col =c("red","blue","black","yellow","purple","green"))
grp8$`4. How often do you use social media?`=as.factor(grp8$`4. How often do you use social media?`)
table(grp8$`4. How often do you use social media?`)
percentages=round(F/sum(F)*100)
percentages
pie(F,main ="Graphical Representation of How often do you use social media?" )
grp8$`5. Do you feel anxious or stressed when you don't have access to social media?`=as.factor
G=table(grp8$`5. Do you feel anxious or stressed when you don't have access to social media?`)
View(G)
percentages=round(G/sum(G)*100)
percentages
names=c("Yes","No","Sometimes")
new_labels=paste(names,"",percentages,"%",sep="")
View(new_labels)
pie(G,labels =new_labels,main ="Do you feel anxious or stressed when you don't have access to social 
media?")
grp8$`6. Do you compare yourself to others on social media?`=as.factor(grp8$`6. Do you compare yourself to 
others on social media?`)
H=table(grp8$`6. Do you compare yourself to others on social media?`)
H
names=c("No,never","Yes,frequently","Yes,sometimes")
percentages=round(H/sum(H)*100)
percentages
new_labels=paste(names,"",percentages,"%",sep ="")
pie(H,labels=new_labels,main =" Do you compare yourself to others on social media?",col 
=c("red","blue","white") )
sum(123,17,81)
grp8$`7. Which social media platforms do you use regularly?`=as.factor(grp8$`7. Which social media platforms 
do you use regularly?`)
table(grp8$`7. Which social media platforms do you use regularly?`)
p=round(L/sum(L)*100)
name=c("Facebook","Telegram","Instagram","TicTok","youtube","Twitter","Snapchat","Whatsapp")
La=paste(names,"",percentages,"%",sep="")
pie(L,labels=La,main ="Which social media platforms do you use regularly")
#####Chi Square Test to show Association between How often do you use social media and which social media 
platforms do you use regularly++-
Table=table(grp8$`4. How often do you use social media?`,grp8$`7. Which social media platforms do you use 
regularly?`)
View(Table)
chisq.test(Table)
barplot(Table,legend.text =c("1-2 hours per day","2-3 hours per day","3-4 hours per day","Less than an hour 
per day","More than 4 hours"),col = c("black","orange","purple","blue","red"))
#### chi square to test the association between gender and preffered platform
Male=table(grp8$`2. Gender`,grp8$`7. Which social media platforms do you use regularly?`)
View(Male)
chisq.test(Male)
barplot(Male,main ="Diagram to show the association between Gender and Preferred Platform ",col = 
c("red","blue"),legend.text =c("Female","Male") )
###Chi Square To Show the association between level of Studies and Interference With Studies
As=table(grp8$`3. What is your level of study?`,grp8$`11. Do you have difficulty focusing on tasks due to social 
media distractions?`,)
chisq.test(As)
barplot(As,main ="Association between level of Studies and Interference With Studies",col = 
c("black","orange","purple","blue","red","green"),legend.text =c("5th Year","1st Year","4th Year","2nd 
Year","6th Year","3rd Year"))
###chi square to test the association between Mental well being and addiction
Ad=table(grp8$`17. Have you ever taken a break from social media to improve your mental wellbeing?`,grp8$`10. Do you feel addicted to social media?`)
Ad
chisq.test(Ad)
barplot(Ad,main = "association between Mental well being and addiction",col = 
c("black","orange","blue"),legend.text = c("No","Planning to"
