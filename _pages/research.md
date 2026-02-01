---
title: "Research Experience"
permalink: /_pages/research/
author_profile: true
---


### Climate Change Prediction with LSTM and Attention Models
Fall 2025

-	Framed long-horizon climate forecasting as a systematic comparison of predictive behavior across spatial aggregation levels, explicitly contrasting global versus continent-level temperature prediction using over 250 years of Berkeley Earth land temperature data (>500k observations).
-	Designed and conducted a controlled empirical comparison of 21 deep learning architectures, systematically varying attention mechanisms and bidirectional temporal modeling to assess predictive accuracy and stability under long-term trends, strong seasonality, and spatial heterogeneity.
-	Built a reproducible time-series preprocessing pipeline to handle non-stationarity and irregular sampling in historical climate records, including country-to-continent harmonization, temporal gap screening, interpolation, and normalization, ensuring fair cross-model comparison.
-	Engineered seasonal encodings, lagged temperature features, and rolling statistics based on the hypothesis that explicit cyclical representations are necessary to stabilize long-horizon forecasts in climate time series.
-	For attention-based architectures, applied attention over fixed 36-month input windows and visualized learned attention weights to examine which historical periods contribute most to predictions, supporting qualitative comparison across models.
-	Evaluated models using RMSE, MAE, and Directional Accuracy to assess both pointwise accuracy and trend alignment across architectures and spatial scales. 
-	Observed that Bi-LSTM models consistently outperform unidirectional LSTMs in regional forecasting tasks, while offering smaller gains under globally aggregated prediction, highlighting scale-dependent differences in predictive behavior.
-	Implemented end-to-end training and inference pipelines in PyTorch and produced spatiotemporal visualizations to support cross-model and cross-region comparison of climate forecasts.
<a href="https://github.com/BopingSong/Climate_Change_Prediction_with_LSTM_Modeling"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>
<hr>

### Measuring the Value of Museum Events
Fall 2025

-	Framed museum event evaluation as a counterfactual impact estimation problem, aiming to quantify the incremental operational and revenue effects of event programming beyond baseline visitation patterns.
-	Analyzed over 10 years of museum-wide operational data from the largest children’s museum in North America, integrating ticketing transactions, retail sales, event calendars, visitor donations, and local weather records.
-	Modeled baseline visitation and revenue dynamics by accounting for seasonality, calendar effects, visitor volume, and weather conditions, mitigating confounding from non-random event scheduling.
-	Designed outcome-specific stacked ensemble baseline models for attendance, ticket revenue, store sales, and donations, combining OLS for interpretability with XGBoost and LightGBM for nonlinear pattern capture, prioritizing the stability of counterfactual estimates and validating robustness across temporal splits (R² = 0.52–0.63).
-	Estimated incremental event effects by comparing observed outcomes to model-predicted baselines, identifying heterogeneous impacts across event formats and revenue channels.
-	Identified heterogeneous treatment effects across event formats and revenue channels, showing that mixed-format events are associated with approximately $4.9K in incremental daily ticket revenue, a ~9% increase in in-store sales, and higher per-visitor donation amounts.
-	Translated statistical estimates into operational insights, enabling comparison of event formats beyond raw attendance and supporting revenue forecasting and strategic programming decisions.

<hr>

### Modeling and Optimization of US Airport Flight Delay Management
Summer 2025

-	Developed airport delay management as a system-level congestion and resource allocation problem, using discrete-event simulation to study how capacity constraints propagate delays through inbound turnaround operations.
-	Developed a DES model of an airport arrival and ground-handling system, explicitly modeling arrival processes, delay identification (≥15-minute rule), gate assignment, ground-crew servicing, and completion or exception handling.
-	Calibrated time-varying arrival rates, delay probabilities, delay causes, and delay durations using U.S. DOT BTS On-Time Performance data (Jan–Apr 2025), modeling arrivals as a non-homogeneous Poisson process with empirically fitted distributions.
-	Explicitly represented gates and ground crews as capacity-constraining queueing resources with seize–hold–release logic, enabling comparison of FIFO and priority queueing rules as well as gate blocking when crews are unavailable.
-	Modeled stochastic ground-handling service times and operational exceptions (cancellations and diversions) while preserving end-to-end KPI accounting for waiting time, utilization, throughput, and queue dynamics.
-	Designed controlled simulation experiments with warm-up periods and 20 independent replications to isolate the marginal impact of capacity changes under baseline and alternative infrastructure and staffing scenarios.
-	Identified gate availability as the dominant system bottleneck, showing that increasing gate capacity from 2 to 3 - 4 gates reduced average post-landing waiting time from 11.56 ± 1.40 minutes to 1.50 ± 0.32 minutes, while increasing ground-crew staffing alone produced minimal congestion relief.
-	Conducted what-if policy comparisons between infrastructure expansion and staffing increases, demonstrating that alleviating upstream capacity constraints dominates downstream staffing interventions in reducing airport congestion.
<a href="https://github.com/BopingSong/Modeling-and-Optimization-of-U.S.-Airport-Flight-Delay-Management-Using-DES-Model"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>
<hr>

### Can Bitcoin Be Used as an Inflation Hedge Like Gold?
Spring 2025

-	Framed the comparison of Bitcoin and gold as a transferable analytical framework for studying non-stationary financial assets, emphasizing regime-dependent behavior rather than asset-specific investment conclusions.
-	Constructed a unified feature representation of asset dynamics by collecting and preprocessing daily price, trading volume, and market activity data, deriving returns, volatility measures, and volume changes to capture short- and medium-term dynamics.
-	Characterized market environments through both event-driven segmentation (e.g., COVID-19 market stress) and data-driven regime discovery, enabling comparative analysis of asset behavior across heterogeneous market states.
-	Applied unsupervised clustering methods to multivariate asset features to identify latent market regimes, using PCA-based visualization to interpret regime structure and transitions across assets.
-	Employed association rule mining on discretized indicators to uncover regime-specific co-movement and volatility patterns, evaluating structural differences using support, confidence, and lift metrics.
-	Conducted time-series modeling using ARIMA after formal stationarity testing (ADF and KPSS), focusing on differences in dynamic persistence and volatility propagation rather than causal hedging claims.
-	Demonstrated that gold consistently occupies lower-volatility regimes during periods of market stress, while Bitcoin exhibits regime clustering associated with higher volatility and risk-seeking dynamics.
-	Positioned the framework as a generalizable approach for analyzing regime-sensitive behavior in emerging and traditional financial assets, with implications for risk management and portfolio construction under non-stationary market conditions.
<a href="https://github.com/BopingSong/Evaluating-Bitcoin-as-an-Inflation-Hedge-vs-Gold"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>
<hr>


### Managing Large-Scale Financial Data with Hybrid Storage Systems
Spring 2025

-	Designed a hybrid data system that stores large-scale stock price time series separately from flexible company metadata, optimizing each for its own query and access needs.
-	Stored and indexed over 15 million daily stock price records in PostgreSQL using a composite primary key on ticker and date, optimizing for range scans, aggregation queries, and time-series access efficiency.
-	Modeled company fundamentals, business descriptions, and industry metadata in MongoDB to accommodate sparse attributes, long text fields, and schema evolution across firms.
-	Implemented a cross-store linking strategy using a shared ticker identifier, enabling logical joins between relational time-series data and semi-structured company metadata without materialized duplication.
-	Built scalable ETL pipelines with Apache Spark to ingest raw market data, compute derived features such as returns and volatility, and apply columnar compression to reduce storage footprint by approximately 25 percent.
-	Optimized analytical query performance through relational index design and access pattern tuning, achieving roughly 25 percent latency reduction for common cross-temporal queries.
-	Developed a lightweight application interface to abstract storage heterogeneity, supporting unified queries over prices and company context while decoupling computation from storage.
-	Architected the system with separable storage, ETL, and application layers to support horizontal scaling to terabyte-scale data volumes, additional data sources, and distributed computation.
-	Led a three-person team in end-to-end system integration, coordinating data modeling, pipeline design, and interface development decisions.
<a href="https://github.com/BopingSong/Financial-Data-Hybrid-Database-Systems"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>
<hr>


### GameX Option – A Decentralized Game Asset Trading and Options Platform
Spring 2025

-	Designed an MVP architecture for a decentralized in-game asset marketplace that supports spot trading of full NFTs and fractionalized game assets (fNFTs), and enables creation/trading of call and put options on both asset types to improve capital efficiency and risk management for players. 
-	Framed the business problem around limitations of existing centralized platforms (limited pricing transparency, fraud risk, lack of financial flexibility, and high entry costs), and positioned the protocol as a DeFi-style layer for game economies and cross-game activity. 
-	Specified a fractionalization module in which a full NFT is locked into a smart contract and a fixed supply of ERC-20 “shares” (fNFT tokens) is minted to represent fractional ownership; shares are freely tradable and can serve as option underlyings. 
-	Designed a redemption workflow where users can regain full NFT ownership by submitting 100% of the fNFT shares, after which the contract validates ownership, burns the ERC-20 shares, and releases the underlying NFT back to the user’s wallet. 
-	Defined an options module supporting call/put options with explicit on-chain metadata fields (underlyingAsset, optionType, strikePrice, premium, expiry, and an isFractional flag), governing option purchase, expiration, and exercise flows for NFTs vs. fNFTs. 
-	Proposed representing options as ERC-1155 tokens to support secondary trading of option positions and standardized display of option status (Active / Exercised / Expired) within a marketplace UI. 
-	Outlined a modular smart-contract system design comprising (1)asset minting and management for in-game items, (2) fractionalization contracts (fNFT), (3) options contracts, (4) a proposed AMM-style cross-game pricing layer, intended to conceptually connect pricing signals across multiple game systems
-	Implemented core contracts in Solidity and tested deployment flows using Remix + MetaMask, leveraging ERC-20 for fractional shares and ERC-1155 for option tokenization to improve composability with wallets and DeFi tooling. 
-	Articulated how blockchain properties (transparent ownership, programmable execution, interoperability, and auditability) address trust, fraud resistance, and ecosystem fragmentation in game asset markets compared with centralized trading venues.
<a href="https://github.com/BopingSong/GameX-Option-A-Decentralized-Game-Asset-Trading-and-Options-Platform"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>

<hr>


### Enhancing Workplace Mental Health: Evaluating Mental Health Support Programs (MHSPs)
Fall 2024

-	Designed a simulation-based research framework to study how intervention effects can be detected and reliably inferredunder realistic assumptions, using workplace mental health programs as an illustrative context.
-	Developed a research plan specifying target populations, conceptual variables, and hypothesized relationships between MHSP participation and employee outcomes.
-	Conducted simulation-based studies in R to generate synthetic outcome data from explicit parametric data-generating processes (e.g., job performance, satisfaction, and retention) under treatment and no-treatment scenarios.
-	Formulated research hypotheses and evaluated the statistical behavior of hypothesis tests, including detection power and misclassification risk, under assumed effect and no-effect conditions using repeated Monte Carlo simulations.
-	Implemented parametric data-generating processes to examine how different effect sizes influence detection power and inference reliability.
-	Visualized simulated outcome distributions and test results using ggplot2 to support interpretation of statistical patterns.
-	Produced a comprehensive research report including literature review, theoretical motivation, hypotheses, methodology, simulation results, limitations, and policy implications for organizational mental health programs.
<a href="https://github.com/BopingSong/Enhancing-Workplace-Mental-Health-Evaluating-Mental-Health-Support-Programs"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>
<hr>


### Customer Churn: Predictive Analytics and Visual Storytelling for Retention
Fall 2024

-	Framed customer churn as a visual analytics and decision-support problem, emphasizing how predictive results can be communicated and compared through effective data visualization to inform retention strategies.
-	Analyzed a telecom churn dataset containing customer demographics, service usage, and billing behavior, conducting exploratory analysis to support meaningful visual comparisons between churned and retained customers.
-	Built an interpretable decision tree model to segment customers into churn-risk groups, using model outputs primarily as inputs for visualization and comparative analysis.
-	Identified key churn-related variables and thresholds to structure visual narratives contrasting high-risk and low-risk customer groups.
-	Designed interactive Tableau dashboards enabling side-by-side comparison of churned vs non-churned customers and high-risk vs low-risk segments across behavioral and usage dimensions.
-	Applied visual encoding and dashboard layout principles to highlight risk concentration, threshold effects, and segment-level differences revealed by the model.
-	Integrated cost–benefit considerations directly into visualizations, illustrating trade-offs between intervention cost and potential revenue savings under targeted retention strategies.
-	Used visual storytelling to convey churn risk and cost–benefit insights in a way accessible to non-technical audiences.
<a href="https://bopingsong.github.io/files/Customer_Churn_Infographic.pdf"
   target="_blank"
   title="View project on GitHub">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
       width="22"
       style="vertical-align:middle; opacity:0.7;"
       alt="GitHub">
</a>

<hr>

