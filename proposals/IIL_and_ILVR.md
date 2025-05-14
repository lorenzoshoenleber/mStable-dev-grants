# General Grant Proposal

* **Project:** The Implied Impermanent Loss and Implied LVR

## Project Overview

### Overview

We propose developing a forward-looking, option-implied measure of risk for liquidity providers (LPs) on decentralized exchanges (DEXs), focusing on impermanent loss and loss-versus-rebalancing (LVR). Using traded option prices, our metric captures real-time market expectations and volatility. This "VIX for DeFi" would enable professionalized market-making, risk-based dynamic fees, and hedging strategies. We aim to collaborate on real-time integration into the mStable platform, enhancing liquidity efficiency, stability, and user education.

### Project Details
  
The core functionality of our project relies on integrating real-time data through APIs in order to compute forward-looking risk metrics for liquidity providers. To achieve this, we leverage the Amberdata API to retrieve cryptocurrency derivative market data, which is essential for calculating option-implied impermanent loss and loss-versus-rebalancing (LVR). In parallel, we use The Graph to access up-to-date liquidity pool information, enabling us to track token balances and pool states with precision.

These two data sources feed into a unified, risk-neutral pricing framework designed to produce real-time measures of LP risk. Architecturally, the system consists of a backend service responsible for collecting and processing both spot and option market data. This service is coupled with a statistical engine that runs the optimization and valuation models to derive the implied IL and LVR metrics. To ensure accessibility, the results are exposed through a lightweight API interface, allowing for seamless integration into frontends such as dashboards or DEX user interfaces.

By combining live market expectations with the mechanics of automated market makers, this architecture enables a dynamic and transparent assessment of liquidity provision risk in decentralized finance.

Our current working papers, on which this proposal is built, 
- Yield Farming for Liquidity Provision (https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4422213)
- Implied Impermanent Loss: A Cross-Sectional Analysis of Decentralized Liquidity Pools (https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4811111)
- Decentralized and Centralized Options Trading: A Risk Premia Perspective (https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4822783)
got presented at various conferences. 

## Team

### Team members
* Lorenzo Schoenleber
* Andrew Papanicolaou

### Team Website
* https://sites.google.com/view/lorenzo-schoenleber/menu
* https://math.sciences.ncsu.edu/people/apapani/

### Legal Structure
N/A

### Team's experience
- Prof. Dr. Lorenzo Schoenleber is an Assistant Professor in Finance at the Collegio Carlo Alberto and the University of Turin. He obtained his PhD at the Frankfurt School of Finance. He is also associated with the Fintech & Digital Finance Chair at Paris Dauphine University. His area of specialization is empirical asset pricing (option-implied information) and DeFi (Yield Farming). 
- Prof. Dr. Andrew Papanicolaou is an associate professor in the Department of Mathematics at North Carolina State University (NCSU). His PhD is in applied mathematics from Brown University. His research interests are computational finance and stochastic systems for control and optimization. The applications of this work include financial data analysis and the challenges associated with these highly complex data sets. My background is in probability theory and nonlinear filtering. 


### Team Code Repos
* https://github.com/your-repo-1
* https://github.com/your-repo-2

## Development Roadmap

Dates - Project stage 
- 06-08/2025 – Accessing, preparing, and processing spot and option data via the Amberdata API 
- 08-09/2025 – Accessing liquidity pool data using The Graph
- 09-12/2025 – Developing the mathematical optimization framework to replicate V3 type of pools and LVR 
- 01-02/2026 – Programming and numerically solving the optimization framework  
- 02-06/2026 – Live implementation of the code to calculate the measure in real time
- 07-08/2026 – First White paper draft

### Overview
* **Total Estimated Duration:** 14 months
* **Total Costs:** 10,000 USD

We want to emphasize that any amount of sponsorship or donation would be beneficial for us since we are trying to request funding from different funding sources to realize this project.


### Milestone 1 

* **Estimated duration:** 2 months
* **Costs:** 6.000 USD

### Milestone 2 

* **Estimated duration:** 1 month
* **Costs:** 1,000 USD

### Milestone 3

* **Estimated duration:** 3 months
* **Costs:** 0 USD

### Milestone 4

* **Estimated duration:** 2 months
* **Costs:** 0 USD

### Milestone 5

* **Estimated duration:** 4 months
* **Costs:** 2,000 USD

### Milestone 6

* **Estimated duration:** 2 months
* **Costs:** 1,000 USD

### Community engagement

As part of our commitment to openness and transparency, we intend to engage the broader DeFi and liquidity provider community through an accessible and educational article published on Medium or a similar platform. This article will explain the methodology behind our option-implied measures of impermanent loss and loss-versus-rebalancing, detail the benefits for liquidity providers, and show how the metrics can be used for risk management and strategic decision-making.

We will include visual examples, case studies, and simulation results to make the content accessible to both technical and non-technical audiences. This will be an opportunity to educate LPs on how to interpret risk metrics and even hedge their positions using derivative products.

Depending on the evolution of the project, we may also publish interim posts after key milestones, such as the integration of the backend risk engine or the live deployment of the API. Our goal is to provide a bridge between academic research and practical tools for the DeFi ecosystem, helping users understand and adopt risk-aware liquidity strategies.
## Future Plans
After the grant, the project will continue through academic collaboration between the proposing researchers and their institutions. Development will be maintained through open-source contributions and ongoing research in the areas of decentralized finance and liquidity provision. One of the key goals is to publish the methodology and results in a peer-reviewed academic journal, thereby strengthening the project’s scientific credibility and visibility within both academic and DeFi communities.

In the short term, the primary focus will be on implementing and deploying the real-time risk measure based on option-implied data, making it readily available for integration into decentralized platforms. The team is open to displaying the results on the front ends of DEX protocols and firmly believes that a forward-looking risk metric can enhance liquidity provision strategies and enable more informed, professionalized market-making.

To ensure long-term sustainability, the team plans to seek additional funding from a variety of sources, including academic grants, sponsorships, and strategic partnerships with DeFi protocols interested in integrating the proposed risk metrics. The team emphasizes that even partial sponsorship would be highly valuable, highlighting a flexible and collaborative approach to funding the project's continued development and deployment.

## Additional Information
We would like to emphasize that our proposal not only aims to produce technical results, but also to generate academic visibility. The project will result in a high-level academic research paper in the DeFi space, offering credibility and dissemination within the scientific and institutional community.

Moreover, one important implementation path we foresee is the possibility to develop dynamic fee mechanisms (hooks) based on the real-time risk levels inferred from our metrics. This could directly impact the design of more efficient and adaptive AMM protocols.

Another valuable application is the use of our metrics to partially hedge liquidity positions through derivatives markets (e.g., buying options to cover LP exposure), contributing to a deeper integration between DeFi and traditional derivatives logic.

Lastly, our framework allows for the generation of simulation-based “corridors” of expected impermanent loss, which can serve both educational and practical purposes for LPs.
