#microarray_heatmap_R20160630
library(gplots)
genes <- read.csv("data")
row.names <- genes$name
x <- genes[, 2:4]
y <- as.matrix(x)
x_heatmap <- heatmap.2(y, Rowv = TRUE, col = greenred(75), labRow = row.names, key = TRUE, keysize = 1, cexRow = 0.7, cexCol = 1, density.info = c("none"),trace = "none")
