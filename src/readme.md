Your source code files will go here.

LWP<- ggplot(LoL_Worlds_Placing, aes(y=Region, fill=Placing)) + scale_fill_manual(values=c("#FFD700", "#C0C0C0", "#CD7F32", "#B87333")) + geom_bar(width = 1, stat = "Count")

blck<- ggplot(lck_lcs, aes(x=lckResult, fill=LCK)) + geom_bar(width = 1, stat = "Count")

blcs<- ggplot(lck_lcs, aes(x=lcsResult, fill=LCS)) + geom_bar(width = 1, stat = "Count")

ggplot(data = lMod, aes(x = Year, y = viewers)) +
     geom_point() +
     stat_smooth(method = "lm", col = "dodgerblue3") +
     theme(panel.background = element_rect(fill = "white"),
           axis.line.x=element_line(),
           axis.line.y=element_line()) +
     ggtitle("Linear Model Fitted to Viewership in League of Legends World Championship")

ggplot(data = sports_viewership, mapping = aes(x = Year, y = viewers, color = type)) + geom_point() + labs(y = "Total Viewers") + geom_smooth(se = FALSE, method = loess)

ggplot(data = tier, mapping = aes(x = Tier, y = amount, fill = Region)) + geom_bar(stat = "identity", position = "dodge") + scale_x_discrete(breaks = c("Iron IV", "Iron III", "Iron II", "Iron I", "Bronze IV", "Bronze III", "Bronze II", "Bronze I", "Silver IV", "Silver III", "Silver II", "Silver I", "Gold IV", "Gold III", "Gold II", "Gold I", "Platinum IV", "Platinum III", "Platinum II", "Platinum I", "Diamond IV", "Diamond III", "Diamond II", "Diamond I", "Master I", "Grandmaster I", "Challenger I"), labels = c("I4", "I3", "I2", "I1", "B4", "B3", "B2", "B1", "S4", "S3", "S2", "S1","G4", "G3", "G2", "G1", "P4", "P3", "P2", "P1", "D4", "D3", "D2", "D1", "M", "GM", "C"))
