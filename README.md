# Real-CATS Dataset:  Real World Dataset of Cryptocurrency Addresses with Transaction Profiles

The Real-CATS dataset includes 50,943 criminal addresses from real-world reports and 102,178 benign addresses from exchange customers until May 30, 2024. We hope this dataset can contribute to cryptocurrency anti-money laundering research and foster the healthy development of the blockchain ecosystem. 

The detailed transaction record for each address is available at: https://www.kaggle.com/datasets/lvd312393/real-cats. 


### Target Audience

- Researchers committed to criminal address detection
- Engineering practices requiring feature and label data
- Other anti-money laundering practices need more seeds to extend their research

### Dataset Overview

The main body of Real-CATS dataset consists of four datasets as follows.

| File Name | Address Num. | Feature Num. | Description                    |
| --------- | ------------ | ------------ | ------------------------------ |
| CB.tsv    | 40,032       | 32           | Criminal addresses on Bitcoin  |
| BB.tsv    | 90,176       | 32           | Benign addresses on Bitcoin    |
| CE.tsv    | 12,561       | 52           | Criminal addresses on Ethereum |
| BE.tsv    | 16,020       | 52           | Benign addresses on Ethereum   |

The above data only includes addresses with at least one transaction. The file also contains over 50,000 addresses without any transactions. These addresses are typically labeled as malicious because they appeared in ransom emails or similar information, although no one was actually harmed. Despite having no transactions, more than 30,000 of these addresses have also been reported in the WatchYourBack Tag Database (https://github.com/cybersec-code/watchyourback/tree/main) and GraphSense Tag Pack (https://github.com/graphsense/graphsense-tagpacks), indicating the possibility of reuse.

For addresses on Ethereum, Real-CATS contains three files to describe the interactions with token contracts.

| File Name      | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| TI_B.tsv       | Token interactions of benign addresses. Use the index from *Identifier.tsv* to simplify the representation of a contract. |
| TI_C.tsv       | Token interactions of criminal addresses. Use the index from *Identifier.tsv* to simplify the representation of a contract. |
| Identifier.tsv | A file for querying complete contract addresses.             |


