# Poisson-regression-modelling-in-R
# Simulated data with a count response variable
set.seed(123)
data <- data.frame(
  Count = rpois(100, lambda = 5),  # Simulated Poisson-distributed counts
  X1 = rnorm(100),
  X2 = rnorm(100)
)

# Fit a Poisson regression model
poisson_model <- glm(Count ~ X1 + X2, data = data, family = poisson)

# Display a summary of the Poisson regression model
summary(poisson_model)
