# Market-Evaluation-for-Espresso-Machines-using-Conjoint-Analysis

## Background

Acme Espresso Machines is a small, fictitious manufacturer of premium coffee maker machines and is in a market dominated by
several large manufacturers, including Breville, DeLonghi, Gaggia, and Rancilio. To improve Acme’s market share, I plan to analyze the market with several objectives in mind:

- Identify specific market segments within the greater market
- Identify specific features desired by different market segments
- Select marketing messages that will resonate with market segments
- Estimate market share performance for different types of machines

## Data analysis method

I plan to conduct a conjoint analysis to address the objectives. 

Conjoint analysis is a statistical technique used in market research to understand how people make decisions about products or services. It involves presenting participants with a series of product profiles, each of which has a unique combination of features/attributes (known as bundles), and asking them to choose their preferred option. By analyzing the patterns of choices made by participants, researchers can identify the relative importance of different attributes and how they affect overall preferences. It also quantifies the tradeoffs consumers are willing to make between two or more attributes, which can help me advise which bundle of features Acme should include in its new coffee machines.  

The versatile nature of conjoint analysis makes the technique relevant for many situations. Conjoint analysis is well-known with a deep body of research behind it, giving it credibility. The results of conjoint analysis are also applicable to consumer behavior; because the process uses actual product choices instead of surveys, the results can uncover hidden drivers not revealed during discussions with consumers

I use a 10-step procedure to conduct the analysis as follows. 

## 1. Attribute Selection

In attribute selection, I select characteristics (attributes) that consumers find most relevant when evaluating a product or service. I first research secondary information, such as product reviews, industry reports and trade journals, and then conduct primary research through customer surveys, to identify 3 relevant attributes:

- Speed (the length of time in minutes it takes someone to brew a cup of coffee)
- Capacity (the number of cups of espresso the machine can brew at one time) 
- Price (the retail price of the espresso machine).

## 2. Attribute Level Selection

In the next step, I leverage secondary and primary research to identify the levels of the attributes where consumers perceive distinct differences. In Acme’s case, I identify two levels for each attribute: 

- Speed: S1: “Fast” (machine capable of brewing coffee in under one minute)
- Speed: S2: “Slow” (machine requires 1 minute or more to brew coffee)
- Capacity: C1: “Single-Cup” (machine makes 1 cup of espresso at a time)
- Capacity: C2: “Multi-Cup” (machines makes multiple cups at a time)
- Price: P1: “Budget” (machine price under $300)
- Price: P2: “Premium” (machine price $300 or more)

## 3. Product Bundle Formation

I create candidate products by bundling together the three attributes I selected, and varying the levels of the attributes. Some marketer researchers call the bundles “cards” because the attributes are written down on physical cards (like 3” x 5” index cards) to show to respondents. In this case, I have 3 attributes assigned to 2 levels each, so I will need 2^3 cards, or 8 cards. The cards are listed in the table below. Note how every combination of attributes is represented in the table.

<img width="516" alt="image" src="https://user-images.githubusercontent.com/113878059/227751954-183001a5-2235-4d37-bee8-6d2acc807db6.png">

## 4. Data Collection and Results

I gather the preference data indicating how much Acme's target audience likes each of the 8 candidate products. I use the rating scale method, where respondents rate each product bundle on a scale of 1 to 5, similar to the ratings methodology used by Amazon.com. I collect the data, asking respondents to rate each candidate product bundle on a scale from 1 to 5:

![image](https://user-images.githubusercontent.com/113878059/227753897-04d6a695-48ba-4cd1-ac78-268ec4f65bd6.png)

The table below shows the resulting preference data for each card, or bundle:

<img width="678" alt="image" src="https://user-images.githubusercontent.com/113878059/227753711-7db8003b-67a1-4fdc-8aed-1418f15bc3bc.png">

## Coding and Preparing Data for Analysis

To make our analysis run smoothly in Microsoft Excel, I prepare the data for analysis by coding it into a special form. The coding includes two steps--converting the data into binary form, and removing redundant data.

I start by coding the data into binary form, which only allows only zeros (0) and ones (1). I use two columns to represent attributes with two levels. I assign two levels to the attribute Speed. I designate Speed 1 as the first level and Speed 2 as the second level. Then, I assign a "1" to each "True" entry, and a "0" to each "False" entry. I repeat the process with capacity and price. See results as below:

![image](https://user-images.githubusercontent.com/113878059/228728726-35609b91-6b1f-4b6a-8066-d4acde0c18a9.png)

For example, an espresso machine which completes the preparation of its drinks in under 60 seconds would be coded as Speed 1 = 1 because I have defined Speed 1 to indicate fast speeds. If Speed1 = 1, then Speed 2 must equal 0.

Similarly, the figure shows coded values for capacity (Cap. 1 and Cap. 2) and price (Price 1 and Price 2). I do not code preference because it represents a ratio (in this case, a rating based on a scale of 1 to 5).

To resolve the problem of linear dependency that might result from this coding, I omit one of the columns for each attribute. We only need (n-1) columns to express all the possible levels of the attribute, where n is the number of levels. Because the redundant column for each attribute is completely dependent on the remaining columns, we do not lose any information when we remove one column.

This is what the table looks like without redundancies:

![image](https://user-images.githubusercontent.com/113878059/228738238-6747e07c-7366-4d8b-99ae-7087d40f6038.png)

## Part-Worth Calculation

I now calculate the preference consumers have for each attribute (called a part-worth) using multiple regression analysis. The multiple regression
process fits a function that approximates the data for multiple variables (in our case, speed, capacity, and price). The process fits a function by minimizing the sum of the squares of the errors. The errors are the discrepancies between the fitted curve and the given data. Our example uses speed, capacity, and price as the evaluation attributes. Therefore, we use the following mathematical equation to predict preference levels:

*Preference = (Constant) + A1 * (Speed 1) + A2 * (Capacity 1) + A3 * (Price 1)*

In the equation, A1, A2, and A3 are coefficients expressing the contribution for the three attributes Speed 1, Capacity 1, and Price 1. Because part-worths express the importance of each attribute toward preference, we estimate the part-worths by calculating the coefficients for each variable in the describing equation. During the process, we also solve for the Constant, which represents the y-intercept of the equation.

I execute regression analysis using the regression function provided in Microsoft Excel's set of data analysis functions (ToolPak add-in).

## Analysis Execution and Findings

Microsoft Excel produces the following summary output after I input preferences data (our dependent variable) in the Input Y Range and speed, capacity and price data (our independent variables) in the Input X Range:

![image](https://user-images.githubusercontent.com/113878059/228973657-d66f647a-b9de-44eb-8b85-fac37ab422e4.png)

## Celculating Preference 

I plug in the values for the constant and the A1, A2, and A3 coefficients to arrive at the following preference equation:

Preference = Constant + A1 * Speed 1 + A2 * Capacity 1 + A3 * Price 1

*Preference = 3.75 + 1.75 Speed 1-0.75 * Capacity 1 + 1.25 * Price 1*

The coefficients represent the utility the respondent places on the attributes. Because A1, the coefficient for Speed 1, is relatively large, we assert that the respondent places a high value on speed when selecting an espresso machine. The positive sign (+1.75) indicates that the respondent prefers Speed 1 (the fast machine) over the alternative speed, Speed 2.
The negative sign in front of the coefficient for Capacity 1, A2, shows that the respondent holds a preference against the smaller machine (Capacity 1), preferring the larger machine instead (Capacity 2). The positive coefficient for A3 indicates a respondent preference for the lower priced machine (Price 1) over the higher price unit (Price 2).
Apply Conjoint Results: In the final step, we interpret the results of the conjoint analysis, applying it for marketing purposes. For example, we might use the results to investigate possible market segmentation or to estimate market share using market simulation. Figure 7.22 provides an overview.

## Market Share Estimation



## Data Interpretation and Recommendations

## References
