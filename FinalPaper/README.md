> 
>
> # README for my Final Paper

I investigate whether overconfidence in financial literacy affect households' financial behaviors through the lens of retirement readiness, precautionary savings, and financial market participation. The data of my study come from the National Financial Capability Studies (NFCS), which can be downloaded [here](https://www.usfinancialcapability.org/downloads.php). To be specific, I downloaded the [2018 State-by-State Survey — Tracking Dataset, Comma delimited Excel file (.csv)](https://www.usfinancialcapability.org/downloads/NFCS_2018_State_by_State_Tracking_Data_Excel.zip) and the [2012 State-by-State Survey — Respondent-Level Data, Comma delimited Excel file (.csv)](https://www.usfinancialcapability.org/downloads/NFCS_2012_State_by_State_Data_Excel.zip) to complete my analyses. They are also uploaded to my GitHub repo. The codes are divided into three parts.

## 1. Clean the NFCS dataset  

The Stata codes and results are presented in the log file `process_log.pdf`. I extract necessary variables (financial behaviors, demographic characteristics, perceived & true financial literacy) from the raw data, merge the education data from the 2012 study, and do some basic cleaning. The cleaned data are exported to `processed_NFCS.csv`.

## 2. Construct the overconfidence measures using machine learning classifiers

The python codes are in the jupyter notebook `overconfidence_measure.ipynb`. After read the pre-cleaned data, I first examine the fundamental patterns of perceived and true financial literacy to form an initial impression of the data. Then I construct a learning set where households can be unambiguously categorized as overconfident or not overconfident. After that I train the classifiers with the learning set and compare the performances of them. Finally I generate the out-of-sample predictions and export the dataset as `overconfidence_measure.csv` for later use. Several figures are exported so that I can insert them into LaTeX, but they are not uploaded to my GitHub repo because they can be better viewed in my final paper. 
## 3. Explore the effects of overconfidence

The Stata codes and results are presented in the log file `analysis_log.pdf`. I translate `overconfidence_measure.csv` into excel before I read the data into Stata because of the precision loss when importing `.csv` files into Stata. I run the logit regression model (3) presented in the paper to see whether overconfidence affects retirement readiness, precautionary savings, and financial market participation of households. Heterogeneous effects are also investigated. Multiple tables are exported but are not uploaded to my repo for the same reason mentioned above.







