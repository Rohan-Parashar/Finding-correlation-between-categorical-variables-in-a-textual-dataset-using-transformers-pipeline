# In this code, a textual dataset was analysed using transformers pipeline and correlations were drawn amongst them. 
# The following steps were followed to do the same - 
# 1. Data was mounted on Google Drive . The Integrated Development Environment (IDE) chosen for the code was Google Colaboratory.
# 2. The data was imported using Pandas library of Python after installing necessary libraries 
# 3. Standard EDA was performed on the data using Pandas to understand the null values, columns, and their data types. 
# 4. Some of the columns that were not of the correct/suitable data type were converted into the same. 
# 5. The columns with null values were analysed first as their number was really low (4/1000). Their language was detected and by using a transformer pipeline the crux of the three main columns CAUSAL_VERBATIM, CORRECTION_VERBATIM and CUSTOMER_VERBATIM was evaluated. 
# 6. After that, the null value entries were dropped from the dataframe. 
# 7. Different columns were analysed using univariate and multivariate analysis. The findings for some of them were written in the comments within the code, and suitable visualisations were done.
# 8. After this, the dataframe was converted into a multi-index one using COMPLAINT_CD_DESC column and its possible sub-categories. 
# 9. The level of the multi-index dataframe was then decreased by 1 to obtain 2 separate columns COMPLAINT_CD_DESC_main_categories  and COMPLAINT_CD_DESC_sub-categories. 
# 10.  Dataframe was further multi-indexed using the CAUSAL_CD_DESC column.
# 11. The level of the dataframe was decreased again by 1 to get 2 separate columns, CAUSAL_CD_DESC_main_categories and CAUSAL_CD_DESC_sub_categories. 
# 12. CAUSAL_CD_DESC and COMPLAINT_CD_DESC columns were dropped, as their categories and subcategories were taken into account in the previous step.
# 13. Then, the attempt to detect the language of the columns with textual data was carried out. It was added as an additional column to the dataframe. The analysis and the visualisation were done accordingly.
# 14. The crux of the 3 main textual columns in question  CAUSAL_VERBATIM, CORRECTION_VERBATIM and CUSTOMER_VERBATIM was evaluated using transformers pipeline with suitable task and model, in addition to best possible questions. The results were added as separate columns to the dataframe.
# 15. Now, the semantic similarity was calculated using sentence_transformers and the following comparisons were carried out
# 16. CAUSAL_CD_DESC_sub  vs.  CAUSAL_VERBATIM 
# 17. CAUSAL_CD_DESC vs. CAUSAL_VERBATIM_CRUX 
# 18. The above step was repeated for the following comparisons:
# i COMPLAIN_CD_DESC_sub  vs.  CUSTOMER_VERBATIM 
# ii. COMPLAIN_CD_DESC vs. CAUSAL_VERBATIM_CRUX.
# 19. After this, correlation was calculated amongst all the suitable combinations of different columns, and the results were visualised using heatmaps. 
