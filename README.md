# Bookish_Flexdashboard
An easy way to visualise trends in reading patterns. Ideally, you shouldn't need to actually know anything about coding to run this. The markdown file pulls the data to populate your flexdashboard from a google sheet. 

If you haven't already, you'll need to download RStudio to run this markdown file and display the flexdashboard. The program is completely free, so you shouldn't have to pay anything to load it onto your computer. You can find more information about downloading R and RStudio here: https://rstudio-education.github.io/hopr/starting.html


# Why use this dashboard?
I love reading and like to keep a record of the things I read, details about the book, and how I felt about it. I also really like data science and creating products that prioritise the user benefitting from engagement. The trouble with this, though, is that it can be tricky to find data products that don't require the user to have their own substantial data science skillsets. 

To this end, I created this flexdashboard. There are a couple of small changes that you'll need to make to run it, but those are detailed in the instructions at the top of the markdown (RMD) file. There is also a CSV file which tells you what the column names should be in your google sheet and how to structure the data in it so your flexdashboard will run without errors. 

I hope you enjoy this as much as I do! 

# How are the dashboards different?
In June 2021, I added a second version of the Bookish Flexdash with added tabs for genre and subgenre-specific trends. You *should* be able to run your flexdash without making too many modifications, but these tabs will be much, much more useful if you change the names to match what *you* read.

# Using the genre tabs
To utilise this version of the flexdashboard, you will need to change the names of the tabs **and** the calls for R to subset the data by genre. The key for this will generally to be to watch for (and then change!) calls for *(Genre == "Genre_Name_Here")*. 

It's very important that you're consistently recording these terms the same way in your reading log.  R is only as clever as what you tell it to do and it won't recognise misspellings or when you fail to capitalise something ("romance" vs "Romance"). If you're careful in your data management, though, this shouldn't cause you many issues. 

**Example 1:**
*History {data-navmenu="Genres"}*

For this tab, you would want to change the tab title "History" to something else that would be more suitable for your own reading habits. 

**Example 2:**
*bigrams <- subset(TBR, (Genre == "History") & (Start_Finish == "1"))*

The same action will need to be taken here to change (Genre == "History") to whatever you would like the tab to reflect

**Example 3:**
*filter((!is.na(Month)) & (Start_Finish == "1") & (Genre == "History")) %>%*

Again, you just need to swap out the "History" term for whatever will be more relevant for you


![image](https://user-images.githubusercontent.com/60521652/129488423-e4a2190a-8f05-444a-901b-83b62f65c1a8.png)

![image](https://user-images.githubusercontent.com/60521652/129488438-7c607115-f62a-41b1-8bd6-aecdd59cd999.png)

