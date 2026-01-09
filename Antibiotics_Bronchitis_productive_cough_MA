# Replicating Analysis 3.1 Comparison 3 
# Productive cough at follow-up visit
# Outcome 1 Number of participants with productive cough 

# Smith SM, Fahey T, Smucny J, Becker LA. 
# Antibiotics for acute bronchitis. 
# Cochrane Database of Systematic Reviews 2017, Issue 6. Art. No.: CD000245. 
# DOI: 10.1002/14651858.CD000245.pub4

if (!requireNamespace("meta", quietly = TRUE)) {
  install.packages("meta")
}

library(meta)

event.e <- c(13,9,28,30,13,2)
n.e <- c(23,11,41,104,69,37)
event.c <- c(14,6,27,32,14,3)
n.c <- c(22,9,31,103,67,32)

studlab <- c("Dunlay 1987","Hueston 1994","King 1996",
"Stott 1976","Verhaj 1994","Williamson 1984")

# Meta analysis - RR is the default for metabin
ma <- metabin(event.e,n.e,event.c,n.c,studlab,method = "MH")

# Forest plot (common effect only)
#png(filename = "~/../Desktop/Comparison 3 Productive cough at follow-up.png", 
#width = 2400*1.3, height = 2400, res = 300)
forest(ma,
       random=F,
       plotwidth = "8cm",
       fontsize = 10,
       col.square = "black",
       col.diamond = "black",
       test.overall = TRUE,
       studlab = studlab)
#dev.off()
