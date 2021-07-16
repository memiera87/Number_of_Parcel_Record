# Number_of_Parcel_Record
Tutorial Github

# Investigating Item-level and Item-parcelling Models in Structural Equation Modelling    # FIRST HEADING
## The R-syntax for the simulation of item-level model                                    ## SECOND HEADING
### _Normal_                                                                              ###THIRD HEADING

    library("lavaan") # Required for SEM analysis                                         Indend to show the coding
    library("matrixcalc") #Required for is.positive.definite function
    library("psych")  #required for reliability function


    data.f=function(n)
  	{
	KSI1=rnorm(n)
	X1Err=rnorm(n)
	X2Err=rnorm(n)
	X3Err=rnorm(n)
	X4Err=rnorm(n)
	X5Err=rnorm(n) 
	X6Err=rnorm(n)
	X7Err=rnorm(n)
	X8Err=rnorm(n)
	X9Err=rnorm(n)
	X10Err=rnorm(n)
	X11Err=rnorm(n)
	X12Err=rnorm(n)
	X1 = round(.70*KSI1 + .714*X1Err + 5.2)
	X2 = round(.80*KSI1 + .060*X2Err + 5.2)
	X3 = round(.90*KSI1 + .436*X3Err + 5.2)
	
	X4 = round(.70*KSI1 + .714*X4Err + 5.2)
	X5 = round(.80*KSI1 + .060*X5Err + 5.2)
	X6 = round(.90*KSI1 + .436*X6Err + 5.2)
	
	X7 = round(.70*KSI1 + .714*X7Err + 5.2)
	X8 = round(.80*KSI1 + .060*X8Err + 5.2)
	X9 = round(.90*KSI1 + .436*X9Err + 5.2)
	
	X10 = round(.70*KSI1 + .714*X10Err + 5.2)
	X11 = round(.80*KSI1 + .060*X11Err + 5.2)
	X12 = round(.90*KSI1 + .436*X12Err + 5.2)

	Eta1Err=rnorm(n)
	Y1Err=rnorm(n)
	Y2Err=rnorm(n)
	Y3Err=rnorm(n)

	ETA1=.585*KSI1 + .811*Eta1Err
	Y1=round(.70*ETA1 + .714*Y1Err + 5.2)
	Y2=round(.80*ETA1 + .060*Y2Err + 5.2)
	Y3=round(.90*ETA1 + .436*Y3Err + 5.2)

	data.norm = data.frame(X1, X2, X3, X4, X5, X6, X7, X8, X9, X10, X11, X12, Y1, Y2, Y3)
	
	return(data.norm)
	}
    
