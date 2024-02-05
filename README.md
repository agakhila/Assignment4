# Assignment 4
# Organize the data into vectors
Frequency <- c(0.6, 0.3, 0.4, 0.4, 0.2, 0.6, 0.3, 0.4, 0.9, 0.2)
BP <- c(103, 87, 32, 42, 59, 109, 78, 205, 135, 176)
First <- c(1, 1, 1, 1, 0, 0, 0, 0, NA, 1)  # Assuming NA is encoded as NA
Second <- c(0, 0, 1, 1, 0, 0, 1, 1, 1, 1)
FinalDecision <- c(0, 1, 0, 1, 0, 1, 0, 1, 1, 1)

# Create side-by-side boxplots
par(mfrow = c(1, 2))  # Set up a 1x2 plotting grid
boxplot(BP ~ First, data = data.frame(BP, First), xlab = "First Assessment", ylab = "Blood Pressure", main = "Blood Pressure by First Assessment")
boxplot(BP ~ Second, data = data.frame(BP, Second), xlab = "Second Assessment", ylab = "Blood Pressure", main = "Blood Pressure by Second Assessment")

# Create histograms
par(mfrow = c(1, 2))  # Reset the plotting grid to 1x2
hist(BP, main = "Histogram of Blood Pressure", xlab = "Blood Pressure", col = "lightblue")
hist(First, main = "Histogram of First Assessment", xlab = "First Assessment", col = "lightgreen")
