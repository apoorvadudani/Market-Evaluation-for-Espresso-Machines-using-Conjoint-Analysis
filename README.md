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

## Data Preparation

I prepare the data for use with R, as well as preparing R to solve the problem by loading the _conjoint_ package.

## Importance Weights Calculation



## Part-Worth Calculation

## Market Share Estimation

## Data Interpretation and Recommendations

## References
