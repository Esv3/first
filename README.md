#dissertation
library(haven)

#loading files

#2005

hse2005ai<-read_dta("hse05ai.dta")

#selecting variables needed

yr2005<-hse2005ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","ethinda","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","expsm","smoke4","kcigregg","chpace")]

#renaming the variables to be consistent with other years and creating a separate column called 'year'

yr2005$Year<-"2005"
names(yr2005)[3]<-"tenure"
names(yr2005)[9]<-"ethnic"
names(yr2005)[13]<-"bprespb2"
names(yr2005)[16]<-"firstsys"
names(yr2005)[17]<-"secsys"
names(yr2005)[18]<-"thirdsys"
names(yr2005)[19]<-"firstdia"
names(yr2005)[20]<-"secdia"
names(yr2005)[21]<-"thirddia"

#2006

hse2006ai<-read_dta("hse06ai.dta")

yr2006<-hse2006ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","ethinda","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","expsm","smoke4","kcigregg","chpace")]

yr2006$Year<-"2006"

names(yr2006)[3]<-"tenure"
names(yr2006)[9]<-"ethnic"
names(yr2006)[13]<-"bprespb2"
names(yr2006)[16]<-"firstsys"
names(yr2006)[17]<-"secsys"
names(yr2006)[18]<-"thirdsys"
names(yr2006)[19]<-"firstdia"
names(yr2006)[20]<-"secdia"
names(yr2006)[21]<-"thirddia"

#merging the 2005 and 2006 dataframe together

yrs0506<-merge(yr2005,yr2006,all=TRUE,sort=FALSE)
View(yrs0506)


#2007

hse2007ai<-read_dta("hse07ai.dta")

yr2007<-hse2007ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","ethinda","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","expsm","smoke4","kcigregg","chpace")]

yr2007$Year<-"2007"
names(yr2007)[3]<-"tenure"
names(yr2007)[9]<-"ethnic"
names(yr2007)[13]<-"bprespb2"
names(yr2007)[16]<-"firstsys"
names(yr2007)[17]<-"secsys"
names(yr2007)[18]<-"thirdsys"
names(yr2007)[19]<-"firstdia"
names(yr2007)[20]<-"secdia"
names(yr2007)[21]<-"thirddia"

yrs050607<-merge(yrs0506,yr2007,all=TRUE,sort=FALSE)
View(yrs050607)

#2008

hse2008ai<-read_dta("hse08ai.dta")

yr2008<-hse2008ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","origin","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","expsmok","smoke4","kcigregg")]

yr2008$Year<-"2008"
names(yr2008)[3]<-"tenure"
names(yr2008)[9]<-"ethnic"
names(yr2008)[13]<-"bprespb2"
names(yr2008)[16]<-"firstsys"
names(yr2008)[17]<-"secsys"
names(yr2008)[18]<-"thirdsys"
names(yr2008)[19]<-"firstdia"
names(yr2008)[20]<-"secdia"
names(yr2008)[21]<-"thirddia"
names(yr2008)[33]<-"expsm"

yrs5to8<-merge(yrs050607,yr2008,all=TRUE,sort=FALSE)
View(yrs5to8)

#2009

hse2009ai<-read_dta("hse09ai.dta")

yr2009<-hse2009ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","origin","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bp1","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","expsmok","smoke4","kcigregg")]

yr2009$Year<-"2009"
names(yr2009)[3]<-"tenure"
names(yr2009)[9]<-"ethnic"
names(yr2009)[13]<-"bprespb2"
names(yr2009)[16]<-"firstsys"
names(yr2009)[17]<-"secsys"
names(yr2009)[18]<-"thirdsys"
names(yr2009)[19]<-"firstdia"
names(yr2009)[20]<-"secdia"
names(yr2009)[21]<-"thirddia"
names(yr2009)[34]<-"expsm"

yrs5to9<-merge(yrs5to8,yr2009,all=TRUE,sort=FALSE)
View(yrs5to9)


#2010
hse2010ai<-read_dta("hse10ai.dta")

yr2010<-hse2010ai[c("pserial","sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","origin","frtpor","vegpor","birthwt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om","hibp2om","bp1","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","everbp","expsmok","smoke4","kcigregg")]

yr2010$Year<-"2010"
names(yr2010)[3]<-"tenure"
names(yr2010)[9]<-"ethnic"
names(yr2010)[13]<-"bprespb2"
names(yr2010)[16]<-"firstsys"
names(yr2010)[17]<-"secsys"
names(yr2010)[18]<-"thirdsys"
names(yr2010)[19]<-"firstdia"
names(yr2010)[20]<-"secdia"
names(yr2010)[21]<-"thirddia"
names(yr2010)[35]<-"expsm"

yrs5to10<-merge(yrs5to9,yr2010,all=TRUE,sort=FALSE)
View(yrs5to10)


#2011
hse2011ai<-read_dta("hse2011ai.dta")

yr2011<-hse2011ai[c("pserial","Sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","Origin","frtpor","vegpor","BirthWt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc","bpmedd","hibp1om2","hibp2om2","bp1","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","everbp","expsmok","Smoke4","kcigregg")]
yr2011$Year<-"2011"

names(yr2011)[2]<-"sex"
names(yr2011)[3]<-"tenure"
names(yr2011)[12]<-"birthwt"
names(yr2011)[9]<-"ethnic"
names(yr2011)[13]<-"bprespb2"
names(yr2011)[16]<-"firstsys"
names(yr2011)[17]<-"secsys"
names(yr2011)[18]<-"thirdsys"
names(yr2011)[19]<-"firstdia"
names(yr2011)[20]<-"secdia"
names(yr2011)[21]<-"thirddia"
names(yr2011)[24]<-"hibp1om"
names(yr2011)[25]<-"hibp2om"
names(yr2011)[35]<-"expsm"
names(yr2011)[36]<-"smoke4"

yrs5to11<-merge(yrs5to10,yr2011,all=TRUE,sort=FALSE)
View(yrs5to11)

#2012

hse2012ai<-read_dta("hse2012ai.dta")

yr2012<-hse2012ai[c("pserial","Sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","Origin","BirthWt","bprespc","omdiaval","omsysval","sys1om","sys2om","sys3om","dias1om","dias2om","dias3om","bpmedc2","bpmedd2","hibp1om2","hibp2om2","bp1","bmival","bmiok","htok","htval","bmicat1","bmicat2","bmicat3","EverBP","expsmok","Smoke4","kcigregg")]
yr2012$Year<-"2012"

names(yr2012)[2]<-"sex"
names(yr2012)[3]<-"tenure"
names(yr2012)[10]<-"birthwt"
names(yr2012)[9]<-"ethnic"
names(yr2012)[11]<-"bprespb2"
names(yr2012)[14]<-"firstsys"
names(yr2012)[15]<-"secsys"
names(yr2012)[16]<-"thirdsys"
names(yr2012)[17]<-"firstdia"
names(yr2012)[18]<-"secdia"
names(yr2012)[19]<-"thirddia"
names(yr2012)[20]<-"bpmedc"
names(yr2012)[21]<-"bpmedd"
names(yr2012)[22]<-"hibp1om"
names(yr2012)[23]<-"hibp2om"
names(yr2012)[33]<-"expsm"
names(yr2012)[34]<-"smoke4"
names(yr2012)[32]<-"everbp"

yrs5to12<-merge(yrs5to11,yr2012,all=TRUE,sort=FALSE)
View(yrs5to12)


#2013
hse2013ai<-read_dta("hse2013ai.dta")

yr2013<-hse2013ai[c("pserial","Sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","Origin","frtpor","vegpor","BirthWt","bprespc","omdiaval","omsysval","SYS1OM","SYS2OM","SYS3OM","DIAS1OM","DIAS2OM","DIAS3OM","bpmedc2","bpmedd2","hibp1om2","hibp2om2","BMIval","BMIok","Htok","Htval","BMIcat1","BMIcat2","BMIcat3","EverBP","ExpSmok2","Smoke415","kcigregg")]
yr2013$Year<-"2013"

names(yr2013)[2]<-"sex"
names(yr2013)[3]<-"tenure"
names(yr2013)[12]<-"birthwt"
names(yr2013)[9]<-"ethnic"
names(yr2013)[13]<-"bprespb2"
names(yr2013)[16]<-"firstsys"
names(yr2013)[17]<-"secsys"
names(yr2013)[18]<-"thirdsys"
names(yr2013)[19]<-"firstdia"
names(yr2013)[20]<-"secdia"
names(yr2013)[21]<-"thirddia"
names(yr2013)[22]<-"bpmedc"
names(yr2013)[23]<-"bpmedd"
names(yr2013)[24]<-"hibp1om"
names(yr2013)[25]<-"hibp2om"
names(yr2013)[26]<-"bmival"
names(yr2013)[27]<-"bmiok"
names(yr2013)[28]<-"htok"
names(yr2013)[29]<-"htval"
names(yr2013)[30]<-"bmicat1"
names(yr2013)[31]<-"bmicat2"
names(yr2013)[32]<-"bmicat3"
names(yr2013)[34]<-"expsm"
names(yr2013)[35]<-"smoke4"
names(yr2013)[33]<-"everbp"

yrs5to13<-merge(yrs5to12,yr2013,all=TRUE,sort=FALSE)
View(yrs5to13)


#2014
hse2014ai<-read_dta("hse2014ai.dta"

yr2014<-hse2014ai[c("pserial","Sex","tenureb","ag215g2","wt_int","wt_nurse","nssec5","hpnssec5","origin2","frtpor","vegpor","BirthWt","bprespc","omdiaval","omsysval","SYS1OM","SYS2OM","SYS3OM","DIAS1OM","DIAS2OM","DIAS3OM","bpmedc2","bpmedd2","hibp1om2","hibp2om2","bp1","BMIval","BMIok","Htok","Htval","BMIcat1","BMIcat2","BMIcat3","EverBP","ExpSmok2","Smoke415","kcigregg")]
yr2014$Year<-"2014"


names(yr2014)[2]<-"sex"
names(yr2014)[3]<-"tenure"
names(yr2014)[12]<-"birthwt"
names(yr2014)[9]<-"ethnic"
names(yr2014)[13]<-"bprespb2"
names(yr2014)[16]<-"firstsys"
names(yr2014)[17]<-"secsys"
names(yr2014)[18]<-"thirdsys"
names(yr2014)[19]<-"firstdia"
names(yr2014)[20]<-"secdia"
names(yr2014)[21]<-"thirddia"
names(yr2014)[22]<-"bpmedc"
names(yr2014)[23]<-"bpmedd"
names(yr2014)[24]<-"hibp1om"
names(yr2014)[25]<-"hibp2om"
names(yr2014)[27]<-"bmival"
names(yr2014)[28]<-"bmiok"
names(yr2014)[29]<-"htok"
names(yr2014)[30]<-"htval"
names(yr2014)[31]<-"bmicat1"
names(yr2014)[32]<-"bmicat2"
names(yr2014)[33]<-"bmicat3"
names(yr2014)[35]<-"expsm"
names(yr2014)[36]<-"smoke4"
names(yr2014)[34]<-"everbp"

yrs5to14<-merge(yrs5to13,yr2014,all=TRUE,sort=FALSE)
View(yrs5to14)


#2015
hse2015ai <- read_dta("hse2015ai.dta")

yr2015<-hse2015ai[c("SerialA","Sex","tenureb","Ag015g4","wt_int","wt_nurse","nssec5","hpnssec5","origin2","frtpor15","vegpor","BirthWt","bprespc","omdiaval","omsysval","SYS1OM","SYS2OM","SYS3OM","DIAS1OM","DIAS2OM","DIAS3OM","bpmedc2","bpmedd2","hibp1om2","hibp2om2","bp1","BMIval","BMIok","Htok","Htval","BMIcat1","BMIcat2","BMIcat3","EverBP","ExpSmok2","Smoke415","kcigregg")]
yr2015$Year<-"2015"

names(yr2015)[1]<-"pserial"
names(yr2015)[2]<-"sex"
names(yr2015)[3]<-"tenure"
names(yr2015)[12]<-"birthwt"
names(yr2015)[9]<-"ethnic"
names(yr2015)[10]<-"frtpor"
names(yr2015)[13]<-"bprespb2"
names(yr2015)[16]<-"firstsys"
names(yr2015)[17]<-"secsys"
names(yr2015)[18]<-"thirdsys"
names(yr2015)[19]<-"firstdia"
names(yr2015)[20]<-"secdia"
names(yr2015)[21]<-"thirddia"
names(yr2015)[22]<-"bpmedc"
names(yr2015)[23]<-"bpmedd"
names(yr2015)[24]<-"hibp1om"
names(yr2015)[25]<-"hibp2om"
names(yr2015)[27]<-"bmival"
names(yr2015)[28]<-"bmiok"
names(yr2015)[29]<-"htok"
names(yr2015)[30]<-"htval"
names(yr2015)[31]<-"bmicat1"
names(yr2015)[32]<-"bmicat2"
names(yr2015)[33]<-"bmicat3"
names(yr2015)[35]<-"expsm"
names(yr2015)[36]<-"smoke4"
names(yr2015)[34]<-"everbp"

yrs5to15<-merge(yrs5to14,yr2015,all=TRUE,sort=FALSE)
View(yrs5to15)


