# Paylocity Deduction Confirmation Pull
Input sheet with Payroll Company ID, Payroll ID, and Deduction Amount, return a .csv of API confirmed deduction amounts for a specific deduction code and check date. 

# Purpose
This is a way to confirm deductions that were requested, were taken accurately and successfully. IF there's a discrepancy, I use this tool to pull the true deduction amounts from paystubs.

# Quick Start
1. Clone main.py to your IDE.
2. Exchange an API secret access_token from Paylocity: https://developer.paylocity.com/integrations/reference/authentication-weblink
3. Add the returned bearer token to the Header in main.py for auth.Authorization.
4. Add an excel sheet to the same folder containing main.py including PCID, TPID, and Deduction Amount columns for the deductions you would like to confirm with the Paylocity.
5. Confirm which deduction code was used to enter the original deduction. Enter that as the ded_amount value.
6. Confirm the exact check date the pay check was issued. Enter that as the check_date value.
7. Run main.py. You should recieve a return file of confirmed deduction in the current directory labeled "Paylocity_confirmations_YYYY-MM-DD".
