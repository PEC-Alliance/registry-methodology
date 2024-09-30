# Assign EAC and  PEC IDs

## **Objective**

This specification outlines the methodology for assigning EAC IDs and PEC IDs to split meter data. The process ensures that all energy generated, including fractions of a megawatt-hour (MWh), is accurately represented and traceable within the PEC registry.

## **Definitions**

**Energy Attribute Certificate (EAC):**

* Represents 1.0 MWh of renewable energy generated.
* Assigned a unique **EAC ID**.
* Can be composed of whole, remainder, and carryover energy records that sum to 1.0 MWh.

**Power Emissions Certificate (PEC):**

* Represents any fraction of energy (including whole and partial MWh).
* Always associated with a EAC ID.
* Assigned a unique **PEC ID** for every record, down to a single watt-hour (Wh).

## **Assignment of REC IDs and PEC IDs**

### **Assigning REC IDs**

* **Whole Records:**
  * Each **Whole** record is assigned a **unique EAC ID**.
  * Represents a full 1.0 MWh generated within a single hour.
  * EAC IDs follow the format of the issuing EAC registry.
* **Remainder and Carryover Records:**
  * **Remainder** and corresponding **Carryover** records that together sum to 1.0 MWh are assigned the **same EAC ID**.
  * This EAC ID is unique and different from those assigned to Whole records.
  * Ensures that the combined energy totaling 1.0 MWh is tracked under a single EAC.

### **Assigning PEC IDs**

* **All Records:**
  * Every individual record (Whole, Remainder, Carryover) is assigned a **unique PEC ID**.
  * PEC IDs uniquely identify each fraction or whole unit of energy within the registry.
  * PEC IDs are associated with their corresponding EAC IDs for traceability.

## Data Fields and ID Structure

### **PEC ID Structure**

* **Format:**\
  `PEC[Project_ID]-[DateCode]-[EAC_ID]-[SequentialNumber]-[Energy_ID]`
* **Example:**\
  `PEC101-20240928-20003-0001-0750000`

### **Components**

1. **Project\_ID:**
   * Unique identifier for the project, determined during onboarding.
   * **Example:** `101`
2. **EAC\_ID:**
   * Unique identifier from the EAC registry.
   * **Example:** `20003`
3. **DateCode:**
   * Represents the date when the PEC was issued or split, in `YYYYMMDD` format.
   * **Example:** `20240928` (for September 28, 2024)
4. **SequentialNumber:**
   * A sequential number to ensure uniqueness among PECs issued on the same date for the same project and EAC.
   * Starts from `0001` and increments by one for each new PEC.
   * **Example:** `0001`
5. **Energy\_ID:**
   * A seven-digit value representing the energy amount in watt-hours (Wh).
   * Ranges between `0000001` (1 Wh) and `1000000` (1,000,000 Wh = 1 MWh).
   * **Example:** `0750000` represents 750,000 Wh or 0.75 MWh.

## **Example**

<table><thead><tr><th width="92">Hour</th><th width="139">Energy (MWh)</th><th width="94">EAC_ID</th><th>PEC_ID</th></tr></thead><tbody><tr><td>1</td><td>1</td><td>1</td><td>PEC101-20240928-1-1-1000000</td></tr><tr><td>1</td><td>1</td><td>2</td><td>PEC101-20240928-2-2-1000000</td></tr><tr><td>1</td><td>1</td><td>3</td><td>PEC101-20240928-3-3-1000000</td></tr><tr><td>1</td><td>0.5</td><td>4</td><td>PEC101-20240928-4-4-0500000</td></tr><tr><td>2</td><td>0.5</td><td>4</td><td>PEC101-20240928-4-5-0500000</td></tr><tr><td>2</td><td>1</td><td>5</td><td>PEC101-20240928-5-6-1000000</td></tr><tr><td>2</td><td>1</td><td>6</td><td>PEC101-20240928-6-7-1000000</td></tr><tr><td>2</td><td>0.1</td><td>7</td><td>PEC101-20240928-7-8-0100000</td></tr><tr><td>4</td><td>0.1</td><td>7</td><td>PEC101-20240928-7-9-0100000</td></tr><tr><td>5</td><td>0.8</td><td>7</td><td>PEC101-20240928-7-10-0800000</td></tr></tbody></table>

## **Conclusion**

This specification ensures that all generated energy is accurately represented within the PEC registry through systematic assignment of EAC IDs and PEC IDs. By following this methodology, the registry maintains high data integrity, traceability, and compliance with renewable energy accounting standards. All stakeholders are encouraged to adhere strictly to this specification to ensure consistent and transparent operations within the PEC registry.
