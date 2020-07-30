**October, 2019**

TechRate
https://techrate.org

## Disclaimer

This is a limited report on our findings based on our analysis, in accordance with good industry practice as at the date of this report, in relation to cybersecurity vulnerabilities and issues in the framework and algorithms based on smart contracts, the details of which are set out in this report. In order to get a full view of our analysis, it is crucial for you to read the full report. While we have done our best in conducting our analysis and producing this report, it is important to note that you should not rely on this report and cannot claim against us on the basis of what it says or doesn’t say, or how we produced it, and it is important for you to conduct your own independent investigations before making any decisions. We go into more detail on this in the below disclaimer below – please make sure to read it in full.
					
DISCLAIMER: By reading this report or any part of it, you agree to the terms of this disclaimer. If you do not agree to the terms, then please immediately cease reading this report, and delete and destroy any and all copies of this report downloaded and/or printed by you. This report is provided for information purposes only and on a non-reliance basis, and does not constitute investment advice. No one shall have any right to rely on the report or its contents, and TechRate and its affiliates (including holding companies, shareholders, subsidiaries, employees, directors, officers and other representatives) (TechRate) owe no duty of care towards you or any other person, nor does TechRate make any warranty or representation to any person on the accuracy or completeness of the report. The report is provided "as is", without any conditions, warranties or other terms of any kind except as set out in this disclaimer, and TechRate hereby excludes all representations, warranties, conditions and other terms (including, without limitation, the warranties implied by law of satisfactory quality, fitness for purpose and the use of reasonable care and skill) which, but for this clause, might have effect in relation to the report. Except and only to the extent that it is prohibited by law, TechRate hereby excludes all liability and responsibility, and neither you nor any other person shall have any claim against TechRate, for any amount or kind of loss or damage that may result to you or any other person (including without limitation, any direct, indirect, special, punitive, consequential or pure economic loss or damages, or any loss of income, profits, goodwill, data, contracts, use of money, or business interruption, and whether in delict, tort (including without limitation negligence), contract, breach of statutory duty, misrepresentation (whether innocent or negligent) or otherwise under any claim of any nature whatsoever in any jurisdiction) in any way arising from or connected with this report and the use, inability to use or the results of use of this report, and any reliance on this report.
					
The analysis of the security is purely based on the smart contracts alone. No applications or operations were reviewed for security. No product code has been reviewed.






### Background 
TechRate was commissioned to perform an audit of smart contracts: 
Pixby.sol

The purpose of the audit was to achieve the following:

Ensure that the smart contract functions as intended.
Identify potential security issues with the smart contract.

The information in this report should be used to understand the risk exposure of the smart contract, and as a guide to improve the security posture of the smart contract by remediating the issues that were identified.
High Severity Issues
Extra passive income

**Issue:** 
If the user performs passive income investment for n days, he gets the passive income for an extra one day (n+1). For example:
The User made the investment for 2 days. 
On the third day he will call the release function and get passive income for 2 days, but he will not get his investments back and will be able to call this function one more time in the future. 
For example, next day he will call this function and will get his investments back and passive income for one extra day, however he invested only for 2 days.

### Recommendation: 
In line 302 change ckecing to ‘>=’, like this:
if(numberOfDaysHeld >= passiveInvestors[_passiveIncomeID].Days){

**Fixed:** 
Issue fixed at 26.10.2019
Medium Severity Issues
No medium severity issues.
Low Severity Issues

## Known vulnerabilities of ERC-20 token

**Issue:**
1. It is possible to double withdrawal attack. More details here.
2. Lack of transaction handling mechanism issue. More details here.

**Recommendation:** 
Add into the function function transfer(address _to, uint256 _value) following code:
require(_to != address(this));

**Fixed:**
Issue fixed at 26.10.2019



## Unlock time issue

**Issue:** 
In function makePassiveIncomeInvestment user can pass _unlockTime which is greater than 365 days, but he should not.

**Recommendation:**
Add checking, that _unlockTime is not greater than 365 days.

**Fixed:** 
Issue fixed at 26.10.2019





## Conclusion
**All the issues in smart contract are fixed and smart contract is free of bugs.**


Source: https://techrate.org/
