---
hidden: true
---

# Hourly Timestamp

Meter data collected from the project is used to assign an hourly timestamp to the issued RECs using the following process:

1. For each hour of the generation data,&#x20;
   1. Create records for each whole 1.0 MWh volume of energy.
      1. Assign REC-ID and PEC-ID to these records.
   2. For hours with a partial megawatt-hour
      1. Assign a PEC-ID to this partial record.&#x20;
      2. Carryover the remainder needed to make 1.0 MWh from the partial record to the next hour interval.&#x20;
      3.
