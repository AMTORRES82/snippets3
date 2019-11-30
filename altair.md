#Altair code

#Histogram

'''python
 alt.Chart(brain_body).mark_bar().encode(
            x=alt.X('Brain Weight',bin=alt.Bin(maxbins=20)),
            y="count()")
'''
##Barra
    bar_trends=alt.Chart(trends).mark_bar().encode(
            x='search_term',
            y='mean(value)',
            color='search_term')

##Line
    line_trends=alt.Chart(trends).mark_line().encode(
            x=alt.X("date:T",timeUnit="year"),
            y="mean(value)",
            color="search_term")

##Scatter

   scatter_body_brain=alt.Chart(brain_body).mark_circle().encode(
            x='Brain Weight',
            y='Body Weight',
            color=alt.value("#123456"),
        ).properties(width=800)
