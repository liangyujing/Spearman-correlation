# Spearman-correlation
```{r spearman correlation for each condition, include = FALSE}
# 1 Sexy
sexy_data <- Simulated_Data[which(picture =="sexy"),]
res_sexy <-cor.test(sexy_data$Digit, sexy_data$Acceptance,  method = "spearman")
## visualzing
ggscatter(sexy_data, x = 'DigitRatio', y = 'Acceptance', 
          add = "reg.line", conf.int = TRUE, 
          cor.coef = TRUE, cor.method = "spearman",
          ylim = c(0, 4.5),
          xlab = "right-hand 2D : 4D", ylab = "minimum acceptance level", main = "Sexy condition")+
  theme_apa(box = TRUE)

```
