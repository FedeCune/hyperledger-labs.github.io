# Lab Name
_IBAN Portability Project._

# Short Description
_In this lab we're going to propose a project that allows a solution to the ANP issue that is characterized by a centralized shared banking platform. The solution involves:
1.	The registration of a group of Banks* (at least 2) into a shared banking platform, through a plug-in solution;
2.	The central repository of the platform will automatically import data provided by the internal database of the bank (the OnBoarding phase) (including details of the account holders, IBAN* codes, generation dates and related BICs*); 
•	automatically generate a portability code, which will be associated to every IBAN: this code will allow the portability of IBANs between banks that share the same platform; 
•	In case of a switching operation:  the new bank will have to insert the portability code received by the client or directly by the old bank. The platform will notify the old bank. If this confirms, the central repository will update the BIC;
•	After the switching operation the system will give a new portability Code to the IBAN in order to avoid risk of misuse of the code from anybody
3.	The Central Redirection Database will control the correctness of BIC code, for a given IBAN code, for every payment and will redirect consequently every payment to the right bank
4.	The Central payment mandate repository will give a centralized visibility above IBAN generation dates, lists of payments across several banks and BIC exchange dates for every client of the platform
5.	The central Know your Customer (KYC) database (Optional), will collect and share information required by relevant regulations for all the banks accounts of the platform (independently from their open or closed IBANP context)


# Scope of Lab
With this lab we would like to implement with Hyperledger Fabric a system of interchange of data relating to the consumer to allow the portability of the IBAN. The players involved will be the bank of origin, the bank of arrival and a centralized control body. Between the peers and the centralized entity must travel transactions not visible to other users of the blockchain. For this we will use the channels, to encapsulate transactions and increase privacy.

The first part of the laboratory aims to implement a blockchain network able to manage the flow of the operations in charge. You want to route the arrival bank's request to that source via json files, return the response to the centralized institution and from there to the arrival bank. A second step will be to isolate in a channel these transactions relating to the transaction between the two banks.


# Initial Committers
_Enzo Russo (e.russo@forfirm.com) CEO_
_Lorenzo Piludu (l.piludu@ibanportabilityproject.org) CTO._


# Sponsor
Vipin Bharathan (vipinsun) vipinsun@gmail.com


