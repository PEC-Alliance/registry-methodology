# Emissions Source Hierarchy

The PEC registry automates the emissions source selection to eliminate complexity and bias for corporate renewable energy buyers. The PEC Alliance has carefully selected each region's most accurate emissions data source. Numerous providers offer varying levels of accuracy, granularity, and methodologies.

Below are key considerations:

* **Model Scope:** Historical short run marginal emissions
* **Model Type:** Statistical, Dispatch, Heat Rate
  * The statistical model regresses changes in generation by fuel type based on changes in load, location marginal price (LMP), and time factors.
  * The dispatch model estimates marginal emissions at nodal resolution derived from standard calculations of LMPs by the grid operator.
  * The heat rate model is produced using LMP, gas prices, and assumptions about the relation between costs and emissions.
* **Time Resolution:** Hourly, Annual
* **Locational Resolution:** Nodal, Zonal, Balance Authority, Country
* **Data Availability:** Near Real-time, Monthly, Quarterly, Annual Release
* **Transparency:** Preference for data published by grid operators and open-source models.

## Emissions Source Selection Guide

<table><thead><tr><th width="105">Rank</th><th width="291">Model Type</th><th>Time Resolution</th><th>Spatial Resolution</th></tr></thead><tbody><tr><td>1</td><td>Marginal (Statistical or Dispatch)</td><td>Hourly</td><td>Nodal</td></tr><tr><td>2</td><td>Marginal (Statistical or Dispatch)</td><td>Hourly</td><td>Zonal</td></tr><tr><td>3</td><td>Marginal (Statistical or Dispatch)</td><td>Hourly</td><td>Balance Authority</td></tr><tr><td>4</td><td>Marginal (Statistical or Dispatch)</td><td>Hourly</td><td>Country</td></tr><tr><td>5</td><td>Marginal (Heat Rate)</td><td>Hourly</td><td>Nodal</td></tr><tr><td>6</td><td>Marginal (Heat Rate)</td><td>Hourly</td><td>Zonal</td></tr><tr><td>7</td><td>Marginal (Heat Rate)</td><td>Hourly</td><td>Balance Authority</td></tr><tr><td>8</td><td>Marginal (Heat Rate)</td><td>Hourly</td><td>Country</td></tr><tr><td>9</td><td>UNFCCC</td><td>Annual</td><td>Country</td></tr></tbody></table>
