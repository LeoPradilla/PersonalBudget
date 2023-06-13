# Personal Budget

<p align="justify">Since coming to Canada (and before that), I have been keeping a tight budget and tracking all my expenses. In the past, I tried different apps and methods, but the one that worked for me was the old, good, and reliable spreadsheets. I've been using Google Sheets as my expense tracker (Google even gives you a template you can use), and for the last 8 months, I have logged every single transaction meticulously. I believe I have gathered enough data to mine valuable insights from my spending habits.</p>

<p align="center">
  <img src="images/Budget_Dashboard.png" style="height:537px; width:720px"/>   
</p>

Link to dashboad in <a href="https://public.tableau.com/views/PersonalBudget_16863483847390/BudgetDashboard?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link">Tableau Public</a>


## Collecting the Data

<p align="justify">Using the Google API to connect to Google services provides secure access to your information on Google Sheets. You need to set up the environment, enable the API, create credentials, install libraries, and a couple of other things. Fortunately, Google offers comprehensive documentation to achieve this using Python (or several other languages). The complete guide can be found <a href="https://developers.google.com/sheets/api/quickstart/python#configure_the_sample">here</a>.</p>

<p align="justify">To gather information from the spreadsheets, you will need the spreadsheet ID and the range of cells where the information is stored within the spreadsheet. In my case, I prefer to organize my budget on a monthly basis, so I have a separate sheet for each month of the year. Fortunately, I am using a template where the range of cells remains the same across all the spreadsheets. I created a simple CSV file with two columns: one for the name of the month and another for the corresponding spreadsheet ID.</p>

<p align="center">
  <img src="images/sheets_csv.png" style="height:182px; width:532px"/>   
</p>
<p align="center">
    <em>Expenses by Category</em>
</p>

Note: One easy method to know the ID of your spreadsheet is to look for it in the URL of your spreadsheet. For example, for this spreadsheet: `https://docs.google.com/spreadsheets/d/1XVqFHuHWjps-aq2VremvHPVY2G9MpD24U9s1mV3H_qU/edit#gid=0` the ID is `1XVqFHuHWjps-aq2VremvHPVY2G9MpD24U9s1mV3H_qU`


## EDA

*Note: To ensure the privacy and security of my personal data, I have chosen not to disclose the precise values of my expenses in this project. Instead, I will introduce a deliberate amount of noise to the data as a means to obfuscate the actual values. By doing so, I aim to maintain the confidentiality of sensitive information while still enabling meaningful analysis. I believe this approach aligns with valid and understandable reasons for protecting personal data.*

<p align="justify">Within the expenses, there are several one-time costs that occur sporadically, such as payments for college tuition and books. Additionally, there are occasional expenses, like those categorized under 'Furniture', which only appear in two months. While these categories still represent significant one-time expenses when they occur, they are infrequent and will be excluded from the analysis.</p>

<p align="justify">The 'Personal' and 'Other' categories group together expenses that are related to purchasing personal items, such as clothing, shoes, and personal care and hygiene products. These expenses may include items like toiletries, makeup, hair care products, and other personal care items. The 'Personal' category might also include expenses like haircuts or electronics, whereas the 'Other' category could include items like books or musical instruments. Although these categories share similarities in nature, they are separated to provide greater clarity when analyzing and categorizing expenses.</p>

<p align="justify">Additionally, I grouped similar categories together. For instance, I merged the categories "Internet" and "Cellphone" into a single category called "Phone and Internet". This consolidation approach was also applied to other relevant categories for improved organization and clarity in expense tracking.</p>
  
## Visualizing the Data

<p align="center">
  <img src="images/expenses_by_category.png" style="height:400px; width:600px"/>   
</p>
<p align="center">
    <em>Spreadsheet IDs</em>
</p>

<p align="justify">Rent takes the largest share, accounting for approximately 52% of the total, emphasizing the significant impact of housing expenses on the overall budget. Food expenditure follows closely behind, representing around 18% of the total. Personal and miscellaneous expenses make up approximately 12.36% of the total. Phone and internet expenses occupy a smaller portion at around 3.73%, while transportation expenses represent approximately 3.83%. Other categories, including Colombia and streaming, have relatively smaller percentages, suggesting their minor contributions to the overall budget.</p>

<p align="center">
  <img src="images/difference_by_category.png" style="height:280px; width:700px"/>   
</p>
<p align="center">
    <em>Expense Variance (CAD)</em>
</p>

<p align="justify">In the period of eight months, Personal and Misc. expenses surpassed the planned budget by a significant margin of $3517, this can easily explain by the fact we did not budget for the Winter clothing (shoes and winter jackets are expensive), beside that we needed to buy normal clothing and shoes. This category requires a reevaluation, and it is evident that a higher allocation of funds is necessary.</p>
<p align="justify">On a positive note, the "Food" category, which includes dining out, showed significant savings. This reduction in expenses can be attributed to a decrease in eating out, an increase in home cooking, and the implementation of meal planning strategies.</p>

<p align="center">
  <img src="images/difference_by_month.png" style="height:350px; width:630px"/>   
</p>
<p align="center">
    <em>Expense Variance (CAD)</em>
</p>

<p align="justify"></p>

