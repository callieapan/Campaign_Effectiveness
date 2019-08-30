# Determine the Effectiveness of Advertisement Spend 
packages used /n
sci-kit learn, numpy, pandas, 

Background\n
Client Tonic, wants to evaluate an experimental advertisement campaign it ran via a third party provider, Criteo, on an e-commerce client Omphalos. Criteo, at its own discretion on which products (out of the hundreds of items in the catalogue) to allocate spend, for which days and the duration. That said, it does not make decision that is necessarily in the best interest of the client Tonic. 

Using ridge linear regression, learn from this experiment on which products does advertisement has highest impact and quantify that impact. It plans to take a more active role in guiding Criteo or future providers to execute its advertisement campaign. 


Data Ingest and Cleaning\n
Two sets of data were ingested, one from Criteo on the campaign details, another from client Tonic on product sales, and brand categorization labels.
Data needed to be treated for mis-match in product identifiers, missing values, or invalid values for identifiers and send. 


Analysis Approach\n
1. Side-by-side comparison on sales across the same period between 2017 and 2018. The campaign was active for approximately 18 weeks in 2018. This approach is to use 2017 as baseline and determine if the delta sales in 2018 were driven by advertisement. However, the sales data in 2017 turned out to be unexpectedly  sparse. After some investigation with brand and sales managers, concluded that many of the products were not 'turned on' at Omphalos' e-commerce platform. Hence rendering this approach unviable. 

2. Iterate to second approach, using sales data before and after campaign weeks as baseline sales. Compare delta in sales that is between no campaign and campaign on periods across products and brands. Create visualization on ROI for top brands in sales and top brands in terms of advertisement dollars received. This has the drawback of not incorporate potential seasonality effects across the same period between consecutive years, however, given the volatile nature of total sales across all catalogue products on the Omphalos platform, Omphalos' own promotion activity to draw traffic to its own  platform can mask any impact from seasonality.  In the barchart of the ROI by product vs. by brand, one can see the cannibalization across products within the brand. 


Outputs \n
Jupyter notebook transform the data and executes ridge regression.Inside the notebook, the bar char of ROI by product (UPC) and by brand is shown inside the notebook. 
Graphical outputs in html of individual products and brand sales across the campaign period in html will be saved in the same directory 
