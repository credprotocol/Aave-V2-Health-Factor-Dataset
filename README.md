
[![Cred][cred-shield]][cred-url]
[![Cred Protocol API][cred-api-shield]][cred-api]
[![Cred Protocol on LinkedIn][linkedin-shield]][linkedin-url]
[![Cred Protocol on Twitter][cred-twitter-shield]][cred-twitter]
[![Cred Protocol on Github][cred-github-shield]][cred-github]

<div align="center">
<h1>Aave V2 Health Factor Dataset</h1>
</div>

## ⚡️ How can I download this dataset? 

### Sample Aave V2 health factor dataset (75 rows, 40KB)

[![Sample HF Matrix][cred-sample-shield]][cred-sample] &nbsp;
[![Sample HF Matrix GD][cred-sample-shield2]][cred-sample2]

- Pandas dataframe
```python
import pandas as pd

url = "https://github.com/credprotocol/health-factor-dataset/blob/main/data/0x01acb3804ba9c42111c6e9c127831eb486ca1ac7.csv?raw=True"
df = pd.read_csv(url)
```
- Using wget
```
wget https://drive.google.com/uc?export=download&id=1nzDJ6T51avrOexboV1ZARUNEg1g--KlE
```

### Complete public Aave V2 health factor dataset (1.33M rows, 1.91GB)

[![Complete HF Matrix][cred-full-shield]][cred-full]

##  📖 Why this dataset?

A more granular version of this dataset is the solid foundation upon which our DeFi credit scoring models are built. Reconstructing historical health factors in small intervals is one of the tools we've developed the help us judge creditworthiness among DeFi users. Because we've grown to appreciate the complexities of Aave health factor data, we want to release a dataset that can help users understand the composition of a health factor.

## 💡 How was this data gathered?

The following diagram details the main phases of creating this dataset. Generally, they are as follows:
- Collecting historical off-chain datasets that are used as inputs for the calculations required to compose a health factor
- Collecting on-chain data by capturing the emission of every associated event starting at the launch of Aave V2
- Combining the off-chain and on-chain data and feeding the resulting values through transformations and ultimately the Aave health factor formula 

<div>
		<img alt="Aave V2 Health Factor Dataset Data Flow" height="400" src="https://github.com/credprotocol/health-factor-dataset/blob/main/img/Aave%20V2%20Health%20Factor%20Dataset%20Data%20Flow.jpg" width="1200">

</div>

## :floppy_disk: What kinds of values are in this dataset?

The Aave V2 Health Factor Dataset contains account-level debt, collateral, and liquidation threshold values for each Aave V2 token along with prices of the associated underlying assets. These columns are accompanied by the aggregate collateral and debt values, computed liquidation thresholds, and the resulting synthetic health factors.  

## 📖 What can I do with this dataset?

If you've borrowed using Aave V2, the most obvious usecase for this dataset would be reviewing the health factor history of your account. Has your health factor dipped to an uncomfortable level close to liquidation? Have you been successful in staying above your personal health factor benchmarks? How much collateral and debt have you owned at different points in the life of your lending and borrowing account?

## 📖 How accurate are the contents of this dataset?

In data validation checks performed against available source-of-truth health factors, Our synthetic health factors showed a mean difference of 1.33%. Our calculated aggregated collateral and debt values had mean differences of 0.42% and 1.12%, respectively. These differences can likely be attributed in part to the historical data used in the computation phase. Historical token prices can vary by up to a few percent between sources in times of high volume or volatility. 
 
## ‎‍💻 Contributors

- Julian Gay
- Xavier Quintuna
- Will Wolf
- Hamza Al Fadel
- Aaron Henry

[linkedin-shield]: https://img.shields.io/badge/-Cred%20Protocol-335EEB?&logo=linkedin&style=for-the-badge&labelColor=414141
[linkedin-url]: https://www.linkedin.com/company/credprotocol/
[cred-shield]: https://img.shields.io/badge/Sign%20up-Cred%20Protocol%20Beta-335EEB?style=for-the-badge&labelColor=414141
[cred-shield2]: https://img.shields.io/badge/Stay%20Up%20To%20Date%20With-Cred%20Protocol%20Beta-414141?style=for-the-badge&labelColor=414141
[cred-url]: https://credprotocol.typeform.com/cred-waitlist?typeform-source=www.credprotocol.com
[cred-api-shield]: https://img.shields.io/badge/DOCS-Cred%20Protocol%20API-335EEB?style=for-the-badge&labelColor=414141
[cred-api]: https://beta.credprotocol.com/docs/api
[cred-twitter-shield]: https://img.shields.io/badge/-@Cred__Protocol-335EEB?&logo=twitter&style=for-the-badge&logoColor=white&labelColor=414141
[cred-twitter]: https://twitter.com/cred_protocol
[cred-github-shield]: https://img.shields.io/badge/-credprotocol-335EEB?&logo=github&style=for-the-badge&logoColor=white&labelColor=414141
[cred-github]: https://github.com/credprotocol
[cred-sample]: https://github.com/credprotocol/health-factor-dataset/blob/main/data/0x01acb3804ba9c42111c6e9c127831eb486ca1ac7.csv
[cred-sample-shield]: https://img.shields.io/badge/Browser%20View-Aave%20Health%20Factor%20Sample%20Dataset-335EEB?style=for-the-badge&labelColor=414141
[cred-full]: https://drive.google.com/file/d/180k3AwxbLQJCt5OkIQPdv49kgRI93dT8/view?usp=sharing
[cred-full-shield]: https://img.shields.io/badge/Drive-Aave%20Health%20Factor%20Complete%20Dataset-335EEB?style=for-the-badge&labelColor=414141&logo=googledrive&logoColor=white
[cred-sample2]: https://drive.google.com/file/d/1nzDJ6T51avrOexboV1ZARUNEg1g--KlE/view
[cred-sample-shield2]: https://img.shields.io/badge/Drive-Aave%20Health%20Factor%20Sample%20Dataset-335EEB?style=for-the-badge&labelColor=414141&logo=googledrive&logoColor=white
[cred-sample3]: https://drive.google.com/uc?export=download&id=1nzDJ6T51avrOexboV1ZARUNEg1g--KlE
[cred-sample-shield3]: https://img.shields.io/badge/Download%20Link-Aave%20Health%20Factor%20Sample%20Dataset-335EEB?style=for-the-badge&labelColor=414141


## ⚙️ Full schema and dataset properties

<details>
<summary>Reveal full schema and properties</summary>

## ⚙️ Dataset specification table

| Specification                                                                             | Value                                                                                                                                                                  |
| :------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| columns       | 315        |
| observations               | 1333683                                                                                                                                               |
| size          | 1.91 GB  
| accounts      | 35524

	
```json

{
	"StorageDescriptor": {
		"parameters": {
			"skip.header.line.count": "1",
			"sizeKey": "18794116",
			"UPDATED_BY_CRAWLER": "aave_v2_atoken_matrix_before_dq_crawler",
			"CrawlerSchemaSerializerVersion": "1.0",
			"recordCount": "1554344",
			"averageRecordSize": "2524",
			"compressionType": "none",
			"classification": "csv",
			"columnsOrdered": "true",
			"areColumnsQuoted": "false",
			"delimiter": ",",
			"typeOfData": "file"
		},
		"cols": {
			"FieldSchema": [
				{
					"name": "block",
					"type": "double",
					"comment": ""
				},
				{
					"name": "block_timestamp",
					"type": "string",
					"comment": ""
				},
				{
					"name": "aave_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "aave_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aaave_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aave_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtaave",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtaave_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtaave_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtaave",
					"type": "double",
					"comment": ""
				},
				{
					"name": "aave_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ampl_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ampl_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aampl_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ampl_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtampl",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtampl_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtampl_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtampl",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ampl_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bal_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bal_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "abal_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "bal_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbal",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbal_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbal_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbal",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bal_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bat_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bat_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "abat_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "bat_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbat",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbat_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbat_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbat",
					"type": "double",
					"comment": ""
				},
				{
					"name": "bat_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "busd_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "busd_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "abusd_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "busd_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtbusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtbusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "busd_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "crv_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "crv_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "acrv_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "crv_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtcrv",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtcrv_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtcrv_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtcrv",
					"type": "double",
					"comment": ""
				},
				{
					"name": "crv_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dai_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dai_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "adai_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "dai_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtdai",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtdai_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtdai_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtdai",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dai_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dpi_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dpi_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "adpi_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "dpi_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtdpi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtdpi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtdpi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtdpi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "dpi_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "enj_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "enj_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aenj_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "enj_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtenj",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtenj_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtenj_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtenj",
					"type": "double",
					"comment": ""
				},
				{
					"name": "enj_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "fei_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "fei_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "afei_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "fei_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtfei",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtfei_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtfei_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtfei",
					"type": "double",
					"comment": ""
				},
				{
					"name": "fei_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "frax_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "frax_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "afrax_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "frax_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtfrax",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtfrax_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtfrax_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtfrax",
					"type": "double",
					"comment": ""
				},
				{
					"name": "frax_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "gusd_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "gusd_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "agusd_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "gusd_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtgusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtgusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtgusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtgusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "gusd_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "knc_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "knc_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aknc_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "knc_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtknc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtknc_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtknc_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtknc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "knc_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "link_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "link_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "alink_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "link_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtlink",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtlink_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtlink_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtlink",
					"type": "double",
					"comment": ""
				},
				{
					"name": "link_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mana_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mana_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "amana_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "mana_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtmana",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtmana_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtmana_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtmana",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mana_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mkr_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mkr_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "amkr_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "mkr_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtmkr",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtmkr_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtmkr_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtmkr",
					"type": "double",
					"comment": ""
				},
				{
					"name": "mkr_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "pax_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "pax_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "apax_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "pax_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtpax",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtpax_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtpax_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtpax",
					"type": "double",
					"comment": ""
				},
				{
					"name": "pax_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "rai_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "rai_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "arai_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "rai_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtrai",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtrai_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtrai_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtrai",
					"type": "double",
					"comment": ""
				},
				{
					"name": "rai_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ren_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ren_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aren_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ren_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtren",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtren_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtren_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtren",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ren_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "renfil_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "renfil_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "arenfil_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "renfil_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtrenfil",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtrenfil_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtrenfil_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtrenfil",
					"type": "double",
					"comment": ""
				},
				{
					"name": "renfil_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "snx_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "snx_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "asnx_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "snx_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsnx",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsnx_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsnx_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsnx",
					"type": "double",
					"comment": ""
				},
				{
					"name": "snx_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "steth_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "steth_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "asteth_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "steth_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsteth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsteth_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsteth_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsteth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "steth_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "susd_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "susd_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "asusd_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "susd_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtsusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtsusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "susd_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "tusd_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "tusd_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "atusd_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "tusd_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebttusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebttusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebttusd_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebttusd",
					"type": "double",
					"comment": ""
				},
				{
					"name": "tusd_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "uni_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "uni_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "auni_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "uni_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtuni",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtuni_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtuni_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtuni",
					"type": "double",
					"comment": ""
				},
				{
					"name": "uni_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdc_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdc_liqthreshold",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ausdc_balance",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdc_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtusdc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtusdc_borrow",
					"type": "double",
					"comment": ""
				},
				{
					"name": "stabledebtusdc_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtusdc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdc_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdt_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdt_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ausdt_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "usdt_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtusdt",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtusdt_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtusdt_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtusdt",
					"type": "double",
					"comment": ""
				},
				{
					"name": "usdt_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "wbtc_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "wbtc_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "awbtc_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "wbtc_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtwbtc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtwbtc_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtwbtc_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtwbtc",
					"type": "double",
					"comment": ""
				},
				{
					"name": "wbtc_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "weth_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "weth_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aweth_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "weth_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtweth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtweth_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtweth_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtweth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "weth_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "xsushi_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "xsushi_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "axsushi_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "xsushi_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtxsushi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtxsushi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtxsushi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtxsushi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "xsushi_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "yfi_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "yfi_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ayfi_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "yfi_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtyfi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtyfi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtyfi_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtyfi",
					"type": "double",
					"comment": ""
				},
				{
					"name": "yfi_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "zrx_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "zrx_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "azrx_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "zrx_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtzrx",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtzrx_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtzrx_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtzrx",
					"type": "double",
					"comment": ""
				},
				{
					"name": "zrx_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ust_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ust_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aust_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ust_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtust",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtust_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtust_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtust",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ust_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ens_deposit_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ens_liqthreshold",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "aens_balance",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "ens_debt_count",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtens",
					"type": "double",
					"comment": ""
				},
				{
					"name": "variabledebtens_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtens_borrow",
					"type": "bigint",
					"comment": ""
				},
				{
					"name": "stabledebtens",
					"type": "double",
					"comment": ""
				},
				{
					"name": "ens_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "sum_total_collateral_eth_x_lt",
					"type": "double",
					"comment": ""
				},
				{
					"name": "total_collateral_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "current_liquidation_threshold",
					"type": "double",
					"comment": ""
				},
				{
					"name": "available_borrows_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "total_debt_eth",
					"type": "double",
					"comment": ""
				},
				{
					"name": "hf",
					"type": "double",
					"comment": ""
				},
				{
					"name": "address",
					"type": "string",
					"comment": ""
				}
			]
		},
		"compressed": "false"
		}
		
	}

```

</details>
<div>
<p float="left" align="middle">
	  <a href="https://credprotocol.com">
		<img alt="Cred Protocol" height="150" src="https://github.com/credprotocol/health-factor-dataset/blob/main/img/diamondlogo-transparent.png">
</a>
</p>
	
</div>

 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; [![Cred][cred-shield2]][cred-url]
