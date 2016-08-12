# ACP_barplots-fig.8-
#The figure 8 multiple bar plots comparing ACP impact and establishment risk
head(comp_estimp) #a quick view of the data organization
  Count Proportion Percentile       Model
1   901      10.60         90   ENV_EST90
2   911      10.72         90   ENV_EST90
3   912      10.73         90   ENV_EST90
4   965      11.35         90   ENV_EST90
5   886      10.42         90   ENV_EST90
6   584       6.87         90 ENVSP_EST90

bp=ggplot(data = comp_estimp, aes(x = Percentile, y = Count)) + 
+ geom_boxplot(aes(fill = Model), width = 3) + theme_bw()



colours <- c(rep("#9999FF",4), rep("#FF9326",4),rep("#FFFF4D",4),rep("#D92121",4))
bp+scale_fill_manual (values=colours)

xlab("Percentile Threshold")+
ylab("Percent Area Affected")
######################################################################################
