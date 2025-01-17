# Real-CAD Dataset:  Real World Dataset of Cryptocurrency Addresses with Transaction Profiles

The Real-CAD dataset includes 103,203 criminal addresses from real-world reports and 106,196 benign addresses from exchange customers until May 30, 2024. We hope this dataset can contribute to cryptocurrency anti-money laundering research and foster the healthy development of the blockchain ecosystem.

Our paper can be found here:

The detailed transaction list for each address will be available soon.

### Target Audience

- Researchers committed to criminal address detection
- Engineering practices requiring feature and label data
- Other anti-money laundering practices need more seeds to extend their research

### Dataset Overview

The main body of Real-CAD dataset consists of four datasets as follows.

| File Name | Address Num. | Label Num. | Feature Num. | Description                    |
| --------- | ------------ | ---------- | ------------ | ------------------------------ |
| CB.tsv    | 90,612       | 68         | 32           | Criminal addresses on Bitcoin  |
| BB.tsv    | 90,176       | 1          | 32           | Benign addresses on Bitcoin    |
| CE.tsv    | 12,561       | 21         | 52           | Criminal addresses on Ethereum |
| BE.tsv    | 16,020       | 1          | 52           | Benign addresses on Ethereum   |

For addresses on Ethereum, Real-CAD contains three files to describe the interactions with token contracts.

| File Name      | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| TI_B.tsv       | Token interactions of benign addresses. Use the index from *Identifier.tsv* to simplify the representation of a contract. |
| TI_C.tsv       | Token interactions of criminal addresses. Use the index from *Identifier.tsv* to simplify the representation of a contract. |
| Identifier.tsv | A file for querying complete contract addresses.             |

Furthermore,  we collect a supplementary dataset Sup-CATS for evaluating the detection model. It consists of 3,147 criminal and 11,058 benign addresses labeled by *Etherscan*. These addresses are all active on August 12, 2024. Sup-CATS simulates a practical scenario where the model is deployed in the real world to detect criminal addresses.



| File Name    | Benign Num. | Criminal Num. | Feature Num. | Description         |
| ------------ | ----------- | ------------- | ------------ | ------------------- |
| Sup-CATS.tsv | 11,058      | 3,147         | 52           | Dataset for testing |
