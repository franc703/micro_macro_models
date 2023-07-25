# README

## Economic Modeling with CES Production and Utility Functions

This model aims to demonstrate the effect of a wage increase on a firm's and consumer's decisions under a CES (Constant Elasticity of Substitution) utility and production function framework. The model takes into account both a production function for the firm and a utility function for the consumer, and it solves for the optimal decisions using optimization techniques under certain constraints.

### Components and Equations

1. **CES Production Function**: The Constant Elasticity of Substitution (CES) production function is a mathematical relationship between the inputs and output of a production process. The functional form used in this model is `(labor**rho + capital**rho)**(1/rho)`. The CES function assumes that labor and capital are substitutable at a constant elasticity, rho. Rho is the substitution parameter and controls the ease of substitution between labor and capital. A higher rho means that labor and capital are easily substitutable, while a lower rho means they are not.

2. **Budget Constraint for the Firm**: This constraint reflects that the total cost of labor and capital cannot exceed the firm's budget. The constraint is expressed as `budget - (wages*labor + interest_rate*capital)`. The firm is assumed to take wages (cost of labor) and the interest rate (cost of capital) as given when making its decision.

3. **CES Utility Function**: The utility function describes the preferences of the consumer. It is assumed to have a CES form: `(x**sigma + m**sigma)**(1/sigma)`. The sigma parameter controls the ease of substitution between the consumption good and imports. A higher sigma means the goods are easily substitutable, while a lower sigma indicates they are not.

4. **Budget Constraint for the Consumer**: The consumer is limited by their income. They cannot spend more than their income on the consumption good and imports. This constraint is given by `income - price*x - price_m*m`.

### Model Equilibrium

The equilibrium in this model is found by solving the firm's and the consumer's optimization problems. These problems are solved using the `scipy.optimize.minimize` function with Sequential Least Squares Programming (SLSQP) method.

1. **Firm's Problem**: The firm seeks to maximize its production subject to its budget constraint. This is done by adjusting the levels of labor and capital.

2. **Consumer's Problem**: The consumer aims to maximize their utility subject to their budget constraint. This is achieved by adjusting their consumption of the firm's good and imports.

The equilibrium is attained when the firm's choice of labor and capital and the consumer's choice of goods consumption and imports no longer change, given the prices and income levels.

### Results

The model outputs the optimal levels of labor, capital, consumption, and imports before and after the wage increase. It also calculates the resulting output, price, and utility in both situations, as well as the welfare loss due to the wage increase.

### Graphs

Six bar charts are created to illustrate the changes in the optimal decisions, output, price, and utility following the wage increase:

1. **Optimal Labor and Capital Before and After Wage Increase**
2. **Optimal Consumption and Imports Before and After Wage Increase**
3. **Output Before and After Wage Increase**
4. **Price Before and After Wage Increase**
5. **Utility Before and After Wage Increase**

### Concluding Remarks

By running the code, you'll be able to observe the impacts of a wage increase on economic decisions and outcomes under the assumptions of this model. The resulting graphs will visually demonstrate these changes, offering a clear understanding of how economic agents might respond to changes in the wage rate under CES utility and production functions.
