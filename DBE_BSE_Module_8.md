# 8.1 Introduction to MLR with Categorical Variables

-   **MLR Review**: A model predicting a dependent variable y using
    multiple independent variables
    ![](media/media/image22.png){width="0.9873184601924759in"
    height="0.20833333333333334in"}

-   **Extension**: In this module, categorical (qualitative) variables
    are introduced as independent variables alongside quantitative
    variables.

    -   **Example**: Flat prices might depend not only on area
        (quantitative) but also on whether the location is premium or
        not (categorical).

#### **Why Include Categorical Variables?**

-   **Improved Predictions**: Categorical variables often provide
    crucial context not captured by quantitative data.

    -   **Example**: In Mysuru flat price data:

        -   Quantitative variables: Area, bathrooms, bedrooms.

        -   Missing categorical variables: Amenities, apartment type,
            premium location.

#### **Handling Categorical Variables**

-   **Key Concept**: Categorical variables need to be converted into
    numerical form (dummy variables) for regression.

    -   **Dummy Variables**: Binary variables (0 or 1) representing
        categories.

        -   Example: Brand variable in Basavaraja\'s dataset:

            -   ![](media/media/image10.png){width="1.5520833333333333in"
                height="0.22916666666666666in"}

            -   ![](media/media/image25.png){width="1.25in"
                height="0.21875in"}

#### **Steps in MLR with Categorical Variables**

1.  **Model Formulation**:

    -   Basic regression equation:
        ![](media/media/image15.png){width="1.8201771653543306in"
        height="0.21221784776902888in"}

    -   x~1~​: Price (quantitative).

    -   x~2~​: Brand (categorical, represented as dummy variable).

2.  **Data Analysis**:

    -   Include both x~1~​ and x~2~​ in the regression model.

    -   Use tools like Excel\'s Analysis ToolPak to calculate
        coefficients, R^2^, standard error, and ANOVA table.

3.  **Example Calculation**:

    -   Basavaraja\'s dataset: Satisfaction score depends on:

        -   Price (x~1~): Quantitative.

        -   Brand (x~2~​): Lenovo (1) or Dell (0).

    -   **Regression Equation**:
        ![](media/media/image4.png){width="2.9479166666666665in"
        height="0.21875in"}

#### **Results and Interpretations**

-   **Performance Improvement**:

    -   R^2^ improved from 0.31 (price only) to 0.45 (price + brand).

    -   Standard error reduced from 5.19 to 4.85.

-   **Significance Tests**:

    -   **F-test** (overall significance):

        -   Null hypothesis: No linear relationship.

        -   F-statistic: 13.75 (p-value close to 0). Reject null
            hypothesis, indicating the model is significant.

    -   **T-tests** (individual significance):

        -   ![](media/media/image11.png){width="0.7729166666666667in"
            height="0.18130139982502189in"}

            -   ![](media/media/image14.png){width="2.9166666666666665in"
                height="0.2708333333333333in"}

            -   Price significantly influences satisfaction score.

        -   ![](media/media/image34.png){width="0.7145833333333333in"
            height="0.17654418197725286in"}

            -   ![](media/media/image5.png){width="2.8125in"
                height="0.3020833333333333in"}

            -   Brand also significantly impacts satisfaction.

#### 

-   Adding categorical variables (e.g., brand) enhances the model\'s
    explanatory power and predictive accuracy.

-   Interpretation of coefficients:

    -   β~1~​: Satisfaction score increases by 1.29 units for every
        1-lakh increase in price.

    -   β~2~​: Lenovo users score 3.93 units higher than Dell users, on
        average.

### **Simplified Explanation**

1.  **What is Multiple Linear Regression (MLR)?**

    -   It\'s like finding a formula to predict something (e.g.,
        satisfaction score) using several factors (e.g., price, brand).

2.  **What's New?**

    -   Previously, we only used numbers (e.g., price).

    -   Now, we also include labels like brand (Lenovo, Dell) by turning
        them into numbers (dummy variables: 1 or 0).

3.  **Why Do This?**

    -   Labels (categories) can also influence predictions. Including
        them improves accuracy.

4.  **How Do We Use It?**

    -   Example:

        -   Satisfaction = 46.83 + (1.29 × price) + (3.93 × brand).

        -   If it's Lenovo, brand = 1. If Dell, brand = 0.

# 8.2 Understanding the Interpretation of Coefficients

1.  **Regression Equation**:\
    ![](media/media/image31.png){width="1.9791666666666667in"
    height="0.2790015310586177in"}​,\
    where:

    -   β~0~​: Intercept.

    -   β~1~: Coefficient for x~1~​ (quantitative variable).

    -   β~2~​: Coefficient for x~2~​ (categorical dummy variable).

2.  **Interpreting Coefficients with a Dummy Variable**:

    -   ![](media/media/image30.png){width="1.9097222222222223in"
        height="0.391583552055993in"}

    -   ![](media/media/image21.png){width="2.076388888888889in"
        height="0.39968066491688536in"}

    -   **Impact of β~2~​**:

        -   ![](media/media/image33.png){width="2.8680555555555554in"
            height="0.717014435695538in"}

3.  **Example with Basavaraja\'s Dataset**:

    -   Regression Equation:
        ![](media/media/image17.png){width="2.219673009623797in"
        height="0.16997484689413822in"}

        -   x~1~​: Price of the computer.

        -   X~2~ = 0 (Dell), x2=1x_2 = 1x2​=1 (Lenovo).

    -   **Predictions**:

> ![](media/media/image26.png){width="1.9930555555555556in"
> height="0.45386373578302713in"}

-   Interpretation: Lenovo scores 3.93 points higher on average than
    Dell.

#### **Residual Analysis**

-   **Residuals vs. x~1~​** (price): Appear evenly distributed around the
    x-axis.

-   **Residuals vs. x~2~** (dummy variable): Clustered at the two dummy
    values (0 or 1).

-   **No major outliers**: A few residuals above or below ±2.

#### **When There are More Categories**

-   **Scenario**: Three brands (Lenovo, Dell, Asus).

-   Use **k - 1 dummy variables** for kkk categories:

![](media/media/image23.png){width="1.9861111111111112in"
height="0.6978226159230096in"}

**Regression Equation**:\
![](media/media/image18.png){width="1.875in"
height="0.2233759842519685in"}

-   **Interpretation of Coefficients**:

    -   β~0~​: Average satisfaction score for Asus.

    -   β~1~​: Difference between Lenovo and Asus.

    -   β~2~: Difference between Dell and Asus.

-   **Alternative Baseline**: Change the reference category.

    -   Example: Use Lenovo as the baseline.

        -   β~0~: Average score for Lenovo.

        -   β~1~​: Difference between Asus and Lenovo.

        -   β~2~​: Difference between Dell and Lenovo.

### **Simplified Explanation**

#### **What is Happening?**

1.  **Why Use Dummy Variables?**

    -   Categorical data (e.g., brands) must be converted into numbers
        (0s and 1s) to fit into the regression model.

2.  **How Do We Interpret Results?**

    -   Each category (e.g., Dell or Lenovo) changes the regression
        equation slightly.

    -   Example: Lenovo gives an average satisfaction score 3.93 points
        higher than Dell.

3.  **What Happens with 3+ Categories?**

    -   Use multiple dummy variables. For 3 brands:

        -   Assign 1s and 0s to represent two of the brands, while the
            third acts as a baseline for comparison.

#### **Key Takeaways**

-   Dummy variables allow you to analyze categorical factors like
    brands.

-   The choice of baseline category (e.g., Asus or Lenovo) affects how
    results are interpreted but not the overall conclusion.

# 8.3 Examples

#### **Baseline Model: Manjula Nayak\'s Household Survey**

-   ![](media/media/image19.png){width="5.222222222222222in"
    height="0.4435542432195976in"}

-   **Regression Results**:

    -   β~0~=−140,378

    -   ![](media/media/image28.png){width="2.4895833333333335in"
        height="0.19791666666666666in"}

    -   ![](media/media/image1.png){width="3.2291666666666665in"
        height="0.19111439195100613in"}

#### **Adding Ownership as a Categorical Variable**

![](media/media/image8.png){width="6.5in" height="4.625in"}

#### **Adding Location as a Categorical Variable**

![](media/media/image13.png){width="6.5in" height="4.236111111111111in"}

![](media/media/image9.png){width="6.5in" height="1.9861111111111112in"}

#### **Baseline Model**

1.  **Initial Model**:

    -   Dependent variable (y): Selling price (in lakhs).

    -   Independent variable (x~1~​): Area (in square feet).

![](media/media/image2.png){width="6.5in" height="0.7777777777777778in"}

2.  **Limitations**:

    -   Adding quantitative variables (e.g., bedrooms, bathrooms) led to
        **multicollinearity issues**, as these variables were highly
        correlated with area.

#### **Step 1: Adding a Categorical Variable (Premium Location)**

1.  **New Model**:

    -   Dependent variable (y): Selling price.

    -   Independent variables:

        -   x~1~​: Area (quantitative).

        -   x~2~​: Premium location (categorical; x~2~​=1 for premium,
            x~2~​=0 otherwise).

    -   Regression equation:\
        ![](media/media/image7.png){width="1.9652777777777777in"
        height="0.2143941382327209in"}

2.  **Results**:

> ![](media/media/image32.png){width="5.861111111111111in"
> height="2.371035651793526in"}

#### **Step 2: Adding Multiple Categorical Variables**

1.  **Additional Variables**:

    -   x~3~: Amenities (1 if present, 0 otherwise).

    -   x~4~​: Gated community (1 if gated, 0 otherwise).

2.  **New Model**:

    -   Regression equation:\
        ![](media/media/image12.png){width="3.0972222222222223in"
        height="0.18472550306211724in"}

3.  **Results**:

> ![](media/media/image16.png){width="4.958333333333333in"
> height="2.4898523622047244in"}

4.  **Significance Tests**:

    -   ![](media/media/image3.png){width="4.923611111111111in"
        height="0.18463582677165355in"}

#### **Residual Analysis**

1.  **Standardized Residuals**:

    -   No values exceeding ±3.

    -   Adding categorical variables improved the fit.

2.  **Plots of Residuals**:

    -   Residuals vs. independent variables
        ![](media/media/image27.png){width="0.9780293088363955in"
        height="0.158413167104112in"} Random distribution, no patterns,
        indicating no bias.

    -   Residuals vs. predicted values
        ![](media/media/image20.png){width="0.23524715660542433in"
        height="0.20910870516185476in"} Equally distributed above and
        below the x-axis.

# 8.4 Interactive Variables

#### **What are Interaction Variables?**

1.  **Definition**:

    -   Interaction variables are the product of two independent
        variables (e.g., continuous and categorical variables).

    -   They capture the conditional relationship between a dependent
        variable (y) and one independent variable (x~2~​), moderated by
        another variable (x~1~​).

2.  **Purpose**:

    -   To model situations where the effect of one independent variable
        on the dependent variable depends on the level of another
        independent variable.

#### **Example: Salary Analysis**

> ![](media/media/image24.png){width="5.060634295713036in"
> height="3.441231408573928in"}

#### **Analysis and Results**

![](media/media/image29.png){width="5.222222222222222in"
height="3.2806266404199476in"}

![](media/media/image6.png){width="5.854166666666667in"
height="0.7974420384951881in"}

#### **Interpretation of Interaction Effects**

1.  **Insights**:

    -   The rate of salary increase (effect of x~2~​) is significantly
        moderated by gender (x~1~).

    -   Men experience a much higher salary increase with work
        experience compared to women.

2.  **Implications**:

    -   Highlights the importance of considering interaction effects in
        salary studies.

    -   Reflects systemic gender-based salary disparities when work
        experience is accounted for.

### **Simplified Explanation**

#### **What Are Interaction Variables?**

-   Interaction happens when one factor (e.g., work experience) affects
    outcomes differently depending on another factor (e.g., gender).

#### **How Does It Work?**

-   Multiply two variables (e.g., gender × experience) to create an
    interaction term.

-   This term helps identify if the relationship changes depending on
    conditions (e.g., different effects for men vs. women).

#### **Example Insights**

-   Men's salaries increase faster than women's as work experience
    grows.

    -   Women: Salary increases by \$52.2 per month of experience.

    -   Men: Salary increases by \$293.8 per month of experience.

#### **Why Use Interaction Variables?**

-   To capture complex relationships and uncover hidden patterns in
    data.

-   Helps ensure models reflect real-world dynamics.

#### **Key Takeaways**

1.  **Power of Interaction Variables**:

    -   They provide tailored insights for different groups (e.g., men
        vs. women).

    -   Make regression models more versatile and insightful.

2.  **Practical Use**:

    -   Applicable in salary analysis, customer segmentation, and more.

    -   Ensures better, data-driven decisions.
