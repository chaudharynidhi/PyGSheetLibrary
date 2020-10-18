# PyGSheetLibrary

Library: nidhichaudharygsmtpd007

To find all the files created in this repo in Master-Branch

To download the this library use: https://pypi.org/project/nidhichaudharygsmtpd007/1.0.6/

This library helps in taking the google sheets and can even convert the sheets into the pandas dataframe and then it can use this dataframe to plot it into 3 different forms of graphs:
1. Bar plot
2. Line Plot with markers and dotted line
3. Scatter Plot with the mean line and the color.

** Details of each functions are described below

1. To call the google spreadsheet:
    - Use createcredentials() for this purpose:
            
            createcredentials('your api json filename', 'spreadsheet to be called')
        Put the full path for the api json filename
    - It returns the list of the dictionary from the called spreadsheet.

2. To convert the list of dictionary returned from the createcredentials() to dataframe:
    - Use createDF() for this purpose:
            
            createDF(d) 
                - d: the returned list of dictionary
    - Returns the dataframe that can be used for plotting.

3. To plot the graphs of your choice:
    - Currently the library provides you to plot 3 graphs: Bar Plot, Line Plot, Scatter Plot.
   
    - For Barlplot you need to call:
          
            plotBar(dataframe, 'column name for the x axis', 'column name for the y axis')
        - The function automatically plots the graph for you.
    
    - For Lineplot you need to call:
            
            plotLine(dataframe, 'column name for the x axis', 'column name for the y axis')
         - The function plots the graph which is represented by the dotted line and the points are marked by the '>' symbol.

    - For Scatterplot you need to call:
            
            plotScatter(dataframe, 'column name for the x axis', 'column name for the y axis', colors)
            colors: Array for designing the colorbar.
        - The function returns the Scatterplot which is represented by the green color and along with it there shall be a color bar which describes the  variation of color throughout the plotting of graph. Along with that mean is also plotted with that.

    Note: All figures can be easily saved.

    Pre-Requisites:
    1. Google API for spreadsheets
    2. Make sure you have shared your google sheet with the mail id given by your API creds

    For creating this library I have used gspread for calling the google spreadsheet api.
    
    Example for this library: 
    ```
    import Spreadsheet1234 as sd
    
    # to get the the returned sheet from google sheets
    d = sd.create_credentials('/home/libraries/dafgierhehjghweg465465617.json','testapisheet')
    
    #to convert the sheet returned from google sheets to df
    df = sd.createDF(d)
    
    #to plot various graphs like bar plot, line plot, scatter plot
    sd.pltbar(df) #for bar plot
    sd.plotline(df) #for line plot
    sd.plotscatter(df) #for scatter plot
    ```
 
 I have used this library to print the scatter plot for the dataset: Greendeck SE Assignment Task 2
 ![alt_text](https://github.com/chaudharynidhi/PyGSheetLibrary/blob/main/scatter_plot1.png?raw=true)    
The graph shows the average_sales for 2 days for almost every minute. I have plotted the mean line which is depicted with the red line. Also the graph has a legend attached with it and a color bar too to describe the changes of color with every change in values.

This is my first attempt in creating any library, I have worked for long hours in learning and implemeting this library. I know this may not sound that hard to make,but learning was great. Thank You for believing in me to work on this assignment.
