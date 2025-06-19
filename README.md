# Election_Result2024_Analysis
Excel+SQL-based insights on the 2024 Indian General Elections - party, state &amp; alliance analysis
#  India General Elections 2024 - SQL Analysis

This repository contains SQL queries for analyzing the **India General Elections 2024**. It explores party performance, alliance-wise results, constituency details, and voter behavior using structured datasets.

---

##  Project Structure

The project uses the following main tables:

- `constituencywise_results` — Final results by constituency.
- `partywise_results` — Total seats and details by party.
- `statewise_results` — Mapping of constituencies to states.
- `states` — State metadata.
- `constituencywise_details` — Vote-level detail for each candidate.

---

##  Key SQL Queries

###  General Overview
- Total number of seats in India
- Number of seats available in each state

###  Alliance-Wise Performance
- Total seats won by:
  - **NDA**
  - **I.N.D.I.A**
  - **Other**
- Seat-wise breakdown per alliance
- State-wise alliance seat distribution

###  Party-Level Insights
- Total seats won per party within alliances
- Top performing parties in a specific state

###  Constituency-Level Details
- Winning candidate, their party, total votes & margin (e.g., *Amethi, Uttar Pradesh*)
- EVM vs Postal votes breakdown for a constituency (e.g., *Mathura*)
- Top 10 candidates by EVM votes across constituencies
- Winner & runner-up per constituency (e.g., *Maharashtra*)

###  State Summary Example (e.g., Maharashtra)
- Total seats
- Total candidates
- Total parties
- Total votes (EVM + Postal)
- EVM vote count
- Postal vote count

---

##  Data Modeling Addition

Added a new column to `partywise_results` to group parties by alliance:

```sql
ALTER TABLE partywise_results ADD party_alliance VARCHAR(50);
