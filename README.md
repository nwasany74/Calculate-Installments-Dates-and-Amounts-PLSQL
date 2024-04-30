# Calculate-Installments-Dates-and-Amounts-PLSQL
## Project Description

This PLSQL project calculates the installment dates and amounts for contracts. It also handles the first installment and adds all new data to a new table in the database schema.

## Project Details

The PLSQL script creates three tables:

1. **CONTRACTS** with columns: 
   - Contract_ID
   - Contract_STARTDATE
   - Contract_ENDDATE
   - Contract_Total_Fees
   - Contract_Deposit_Fees
   - Client_ID
   - Contract_Payment_Type
   - Notes

2. **CLIENTS** with columns:
   - Client_ID
   - Client_Name
   - Mobile
   - Address
   - NID

3. **INSTALLMENTS_PAID** with columns:
   - Installment_ID
   - Contract_ID
   - Installment_Date
   - Installment_Amount
   - Paid

Two primary keys using the PRIMARY KEY constraint are defined:

- The first one is on the Contract_ID column of the CONTRACTS table.
- The second one is on the Client_ID column of the CLIENTS table.

Two foreign key constraints are used:

- The first one is between the CONTRACTS and CLIENTS tables, where the client_ID column in the CONTRACTS table references the client_ID column in the CLIENTS table.
- The second one is in the INSTALLMENTS_PAID table with the CONTRACTS table in the contract_ID column.

## Tools and Technologies

- SQL and PLSQL
- Triggers
- TOAD
