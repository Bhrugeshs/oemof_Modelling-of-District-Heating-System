# oemof_Modelling-of-District-Heating-System

## About the Project:

This project focuses on designing a cross-sectoral energy system to provide district heating in a city quarter in southern Germany (Amberg, Bayern). The system integrates multiple energy components, ensuring cost-efficiency, sustainability, and CO2 reduction. The key components of the system include:

- Heat pump
- Ground-mounted large-scale solar energy systems (e.g., photovoltaic and/or solar thermal collectors)
- Backup or peak load systems
- Large-scale sensible thermal storage (seasonal storage)
- Connection to public grids (electricity, gas)

## Objective

The primary objective of this project is to:
1. Size the system components and develop a cost-optimized schedule with the help of the *oemof toolbox*.
2. Calculate the yearly CAPEX (Capital Expenditure), OPEX (Operating Expenditure), and LCOE (Levelized Cost of Energy) for the delivered thermal energy.
3. Develop two configurations:
    - A **CO2-optimized configuration**
    - A **Cost-optimized configuration**

## System Components

- **Heat Pumps**: Can use ambient air or river water as a low-temperature heat source. The temperature profile is crucial to calculate the Coefficient of Performance (COP). Data was sourced from online resources.
- **Solar Renewable Energy Systems**: Includes ground-mounted PV systems, with hourly normalized production profiles.
- **Backup and Peak Load Systems**: Used to balance fluctuations in renewable energy generation.
- **Thermal Storage**: A large-scale seasonal thermal storage system, with options for conventional TTES (high-temperature heat)
- **Grid Connections**: Integration with public electricity and gas grids to support energy supply.

## Design Considerations

- **Feasibility**: The components selected are commercially available, with a technically feasible operation schedule (min/max up- and downtimes for critical components like heat pumps is taken into consideration).
- **Energy Tariffs**: Different prices for energy consumption, including electricity tariffs for private consumers and large-scale consumers like heat pumps.
- **CO2 Emission Limit**: The share of heat derived from fossil fuels is capped at a maximum of 35%.

## Boundary Conditions

- **Thermal Peak Load**: 2500 kW
- **Electric Peak Load**: 850 kW (excluding heat pumps)
  
### Energy prices
- Natural gas: 8 Ct/kWh
- Biomethane: 15 Ct/kWh
- Hydrogen: 25 Ct/kWh
- Biomass (wood chips): 30 Ct/kWh
- Electricity (including grid fees) private consumers 32 Ct/kWh
- Electricity (including grid fees) large consumers, e.g., large scale heat pumps 25 Ct/kWh

### Revenues for selling electricity to the grid (e.g., by PPA):
- PV system: 10 Ct/kWh
- Fossil CHP systems:5 Ct/kWh
- Renewable CHP systems: 10 Ct/kWh

### Investment Costs
- Gas boiler: 150 €/kWth
- Gas fired CHP unit: 750 €/kWel
- Biomass boiler (wood chips): 500 €/kWth
- Heat pump (large): 1500 €/kWel
- Ground mounted PV system (large): 750 €/kWp
- Balance of system (BoS): 30 % of the total investment cost

## CO2 and Energy Emission Factors

- **Primary Energy**: Various energy carriers like natural gas, biogas, wood, and electricity are considered with specific CO2 emission factors.
- **Electricity**: Grid supply: 560 g/kWh, PV/renewable electricity: 0 g/kWh
