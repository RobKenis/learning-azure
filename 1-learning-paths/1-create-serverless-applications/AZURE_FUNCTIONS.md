# Azure Functions

## Benefits
Basically everthing that AWS Lambda offers.

## Drawbacks
By default, functions have a timeout of **5 minutes**, with a maximum of **10 minutes**.
If the function is initiated through an **HTTP request**, the maximum exection time is **2.5 minutes**.
While scaling, only *1* function app can be created **every 10 seconds**, for up to **200 instances**.

# Create a functions app
Let's do this using *ARM Templates*, like the responsible adults we are.
