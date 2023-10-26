# pandas-challenge

This challenge asked us to take raw school and student test score data from two CSVs and use Pandas in Jupyer Notebook to synthesize the data into a single dataframe. 
We then needed to condense this dataframe into a per school analysis in order to compare and draw larger conclusions.
This included finding average test scores and pass rates for each school.
The dataframe was reworked and sliced many different ways to analyze testing scores and outcomes across a number of different variables.
These variables included grade level, spending per student, school size, and school type.
Once we completed the code, we wrote an analysis of the results, which appears at the top of the notebook.

Most of my code was taken from in-class examples from the Pandas unit, as well as this Pandas reference sheet: https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

I worked through most of the assignment with a virtual study group that included four other students.
We worked independently where we could, but got stuck in most of the same places and collaborated to get through them.
I did reference Stack Overflow when stuck, and had two specific sticking points where I requested help from ChatGPT.

The first of these was pulling school type in a way that allowed later code and dataframes to run as required.
I was getting a variable type error when trying to sort school type into bins, and my attempts to change it with the code I knew were met with resistance.
ChatGPT gave me: school_types = school_data_complete.groupby('school_name')['type'].unique().apply(lambda x: ', '.join(x))

Prior to that my school types were appearing inside brackets in tables and would not respond properly to df.groupby()
The other issue I had was with using the provided code to format budget and budget per student into dollar values
The formatted values would not sort into bins as they were string variables
ChatGPT gave me the idea to remove the formatting long enough to sort the values into bins, then add it back in.
