# Human-Capital
title: ‘Four Facts about Human Capital’ author: Venkatesh Kannan email: kannan.venkatesh@stud.hs-fresenius.de name: Venkatesh id: 400370901 date: “Last compiled on 23 July, 2024” output: bookdown::pdf_document2: keep_tex: true toc: true toc_depth: 3 number_sections: true bookdown::html_document2: toc: true toc_depth: 2 number_sections: true toc_float: collapsed: false smooth_scroll: false fig_caption: true pdf_document: toc: true toc_depth: 2 header-includes: -
fontsize: 12pt urlcolor: blue linkcolor: red csl: “https://raw.githubusercontent.com/citation-style-language/styles/master/apa.csl” editor_options: markdown: wrap: 72 bibliography: references.bib —

Abstract
The intrinsic role that human capital plays in economic development is the focus of this project, which explains David J. Deming’s seminal work, “Four Facts about Human Capital.” The paper uses data from the National Longitudinal Survey of Youth 1979 cohort and AFQT scores and discusses methodologies attached to understand the multi-faceted impacts of investments in human capital. Three areas related to the relationship between education and labor earnings, substantial economic payoffs of early childhood and young adulthood interventions, and the processes of developing foundational and higher-order skills are discussed. The project makes use of standardized data so as to arrive at correct comparisons and robust findings. It brings out through detailed empirical analysis how such strategic educational investments can actually raise productivity and earnings, thereby giving relevant insights to be taken by policy makers and educators. This comprehensive review puts a spotlight on how human capital investments can be optimized for increasing economic growth and improving individual economic outcomes.

1.Introduction
The inquiry into human capital—one of the mainstays of economic theory—has covered much ground since its conceptualization. This paper seeks to trace and review some major empirical and theoretical advances in understanding the role of human capital in economic outcomes, drawing from David J. Deming’s “Four Facts about Human Capital”. In the README file, this project combines data analysis and methodologies with a comparative study of AFQT scores to bring forth the comprehensive analysis of human capital’s impact on labor earnings and economic returns from education, all the way down to intricacies of skill formation.

According to human capital theory, investing in education and training, among other kinds of learning, has future payoffs identical to other capital investments. These investments raise workers’ productivity and, hence, their ability to generate income. An idea that began with some opposition due to the notion that people would be treated as assets has become wildly popular and remains a keystone of contemporary economic thinking. This is aptly demonstrated by the sharp rise in education levels and public expenditure on education across the world from the middle of the 20th century till date.

The theory is crystallized into four stylized facts concerning human capital. First, human capital explains a significant variation of labor earnings within and across countries. One of the core models in this theory, the Mincer equation, relates log earnings to schooling and work experience. Empirically, this is estimated to be an increase in earnings of around 10% with each additional year of schooling, after properly controlling for possible endogeneity biases using instrumental variables. Human capital investments, begun in childhood and young adulthood, pay high returns. This is a result that is very important to take away for policymakers: early childhood education matters, but so too does continued investment well into young adulthood. The Heckman curve shows the declining returns of skill investments with age, illustrating how the earlier the interventions are, the more cost-effective.

Third, the mechanisms for producing foundational skills—in literacy and numeracy—are now well understood. Resource allocation remains the primary constraint. Increasing school spending, improving class sizes, and investing in teacher quality remain some of the most effective strategies to enhance these skills. Recent research confirms that such investments bring large gains in educational attainment and future earnings. Fourth, higher-order skills—such as problem-solving and teamwork—are becoming extremely valuable in the modern economy. Despite their value, the technology for effectively developing these skills is much less well developed compared with foundational skills. While these skills are said to matter regarding outcome in the labor market, measurement and enhancement of these non-cognitive skills are the most challenging areas for further research.

Using the AFQT scores from the National Longitudinal Survey of Youth 1979 and 1997, cohorts yield an important data set to analyze the impact of human capital on labor market outcomes. The companion paper of Altonji, Bharadwaj, and Lange, 2009 outlines the necessary adjustments and relative methodologies that would line up these scores, conditioning on format and test conditions. In this sense, standardization will allow for a much more accurate examination of cognitive skills and their economic consequences across different cohorts.

This project makes use of data from the NLSY79 cohort and the AFQT matching dataset. The Stata code in the README folder facilitates easy replication of the analysis for any reader interested, thus checking on transparency and reproducibility of this research. All variables on educational attainment, cognitive ability, and labor market outcomes are in the data set, which allows for an all-rounded assessment of the multifaceted impact of human capital.

This research program combines theoretical insights with sound empirical evidence in exploring the complex role of human capital in the process of economic development. Specifically, the research investigates links between education, skill formation, and labor market outcomes in detail, deriving relevant insights for policy makers and educationalists who wish to maximize human capital investments for the attainment of economic growth and human prosperity.

2.Objective
It will offer a comprehensive and detailed analysis of the impact of human capital on economic outcomes by using data from the National Longitudinal Survey of Youth 1979 cohort and AFQT scores. In this way, one could look into the effect of investments in education and skill acquisition on labor earnings and estimate the economic return to early childhood and young adult interventions, along with the mechanisms for producing foundational and higher-order skills. The empirical project tries to build on firm empirical methodologies and standardized data in constructing actionable insights for the policymakers and the educators on how to best optimize educational investments for improvement in productivity and economic growth.

3.Methodology
Data gathering is covered first, and then R and some of its features are briefly reviewed. This then moves on to the replication approach, which is followed by instructions on how to gather

3.1 R
R is a freeware programming language that is typically used for graphing and statistical calculation. Early in the 1990s, two New Zealanders named Ross Ihaka and Robert Gentleman from Auckland University created the R programming language. Over the next few years, R has developed into a feature-rich platform that includes a wide range of packages and libraries. One such distribution that is built on R is RStudio. Making the syntax powerful and simple to use is one of the objectives of language designers, particularly for jobs involving data processing and statistical computations. Additionally, this architecture makes it easier for those who are new to the fields of data analysis and replication to interact with the system.

3.2 R Markdown
A simple markup language called R Markdown was created for content organisation. It accomplishes this by fusing the simplicity of Markdown with the power of R. Users can quickly create a document that integrates data, outputs, code, and narrative writing in one go by using R Markdown. This multifunctional report generation system produces output in many different formats, including Word documents, PDFs, and HTML. The process is rather straightforward: you create a R Markdown page with explanations and conversations woven throughout, along with snippets of R code. The code snippets are run when the document is rendered, and the results are immediately added into the report.

4.Data collection
The dataset for the National Longitudinal Survey of Youth 1979 and its matching dataset to the Armed Forces Qualification Test will be used to explore human capital’s role in generating such economic outcomes. Data was obtained in various file formats, particularly .dta for Stata data files and .dct for dictionary files defining the structure of fixed-width data files.

4.1 Data collection and Preparation
The main dataset containing the AFQT scores, afqt_adjusted_final.dta, was read directly to R Studio by using the read_dta option from the haven package. This haven package is meant to ensure seamless compatibility with Stata files and brings efficient data import and handling in R. The following lines of code show how the .dta was loaded.It has variables for AFQT scores, age at testing, sample identifiers, and many other important factors relevant to studying the cognitive abilities of various cohorts.

library(ggplot2)
library(dplyr)
## 
## Attaching package: 'dplyr'
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
library(haven)
library(readxl)
library(readr)
library(foreign)

afqt_adjusted_final <-read_dta("afqt_adjusted_final.dta")
The .dct files, specifically age97.dct and nlsy79_vars.dct, are dictionary files that describe the layout of fixed-width text files. These were not directly readable within R Studio. More specifically, in order to combine these datasets, the .dct files first had to be converted outside R Studio into Excel .xlsx format. Indeed, this step in the conversion process made the data more accessible and easier to handle within the R environment. After conversion, the .xlsx files were imported into R Studio using the read_excel function from the readxl package.

age97 <- read_excel("age97.xlsx")
Weights for both the NLSY79 and NLSY97 cohorts were provided in CSV format and read into R Studio using the read_csv function from the readr package. Weights should be used in creating weighted analyses to maintain proper representation from the sample design of the survey. Here is a sample of how the CSV files were loaded

weights79 <- read_csv("weights79.csv")
## Rows: 12686 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
weights97 <- read_csv("weights97.csv")
## Rows: 8984 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
5 Graphical Representation
the code loads all of the necessary libraries: ggplot2 for plots, dplyr for general data manipulation, haven for reading in Stata files, readxl for Excel files, readr for CSV files, and foreign for other data formats. All of these libraries supply key functions used for reading the data, massaging it, and creating the visualization.

library(ggplot2)
library(dplyr)
library(haven)
library(readxl)
library(readr)
library(foreign)
The next step is to load the datasets used in the analysis. The afqt_adjusted_final dataset is a Stata file with the adjusted AFQT scores of both cohorts. In addition, the code loads age97.xlsx, an Excel file most likely containing age data pertaining only to the NLSY97 cohort. Weights for both cohorts, which need to be loaded in order to weight the data appropriately in the analysis, are loaded from weights79.csv and weights97.csv, respectively.

afqt_adjusted_final <- read_dta("afqt_adjusted_final.dta")
age97 <- read_excel("age97.xlsx")
weights79 <- read_csv("weights79.csv")
## Rows: 12686 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
weights97 <- read_csv("weights97.csv")
## Rows: 8984 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
It then subsets the data to include only those who, at the time of taking the AFQT test, were 16 years old. The filtering by cohorts is independently done, such that sample == 0 corresponds to the NLSY79 cohort and sample == 1 corresponds to the NLSY97 cohort. This will allow comparison between the same age group in the two different cohorts so meaningful analysis can be done on the AFQT score distributions.

afqt_16_nlsy79 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 0)

afqt_16_nlsy97 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 1)
Finally, the program creates a density plot of AFQT scores for both cohorts. The code employs ggplot2 to initiate the plot and geom_density for adding density plots for the AFQT scores for each of the two cohorts. The line for the NLSY79 cohort’s density plot is solid blue in color, whereas it is represented by a red dashed line for the NLSY97 cohort. Weighting is applied with the appropriate survey weights to make sure that the graph represents an accurate picture.

ggplot() +
  geom_density(data = afqt_16_nlsy79, aes(x = afqt80, weight = weight, color = "NLSY 1979"), linetype = "solid") +
  geom_density(data = afqt_16_nlsy97, aes(x = afqt80, weight = weight, color = "NLSY 1997"), linetype = "dashed") +
  labs(title = "AFQT Scores at Age 16", x = "afqt according to 1980 definition", y = "Density") +
  scale_color_manual(name = "Sample", values = c("NLSY 1979" = "blue", "NLSY 1997" = "red")) +
  theme_minimal()


Other plot customizations include adding a title and axis labels with labs, and customization of the legend to distinguish the two cohorts with scale_color_manual, which maps blue to the NLSY79 cohort and red to the NLSY97 cohort. Finally, theme_minimal provides a minimalistic theme to make sure clarity and simplicity in the presentation of the plot are ensured.

The overall structure of this code is proficient in reading a number of datasets. It generates, after filtering the data on 16-year-olds from two different cohorts, a comparative density plot of their AFQT scores. The plot that will be produced will show distributional differences and similarities between the two cohorts, thus offering insight into the cognitive abilities for both groups at a certain age.

library(ggplot2)
library(dplyr)
library(haven)
library(readxl)
library(readr)
library(foreign)

# Load datasets
afqt_adjusted_final <- read_dta("afqt_adjusted_final.dta")
age97 <- read_excel("age97.xlsx")
weights79 <- read_csv("weights79.csv")
## Rows: 12686 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
weights97 <- read_csv("weights97.csv")
## Rows: 8984 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
# Check if datasets are loaded correctly
print(head(afqt_adjusted_final))
## # A tibble: 6 × 7
##     pid weight sample   age afqt80 pafqt afqt_std
##   <dbl>  <dbl>  <dbl> <dbl>  <dbl> <dbl>    <dbl>
## 1     2     76      0    21   129      9     118.
## 2     3     54      0    18   180.    52     171.
## 3     4     57      0    18   188.    62     180.
## 4     5     76      0    20   209     88     201.
## 5     6     64      0    19   219    100     219.
## 6     7     67      0    16   162.    42     162.
print(head(age97))
## # A tibble: 6 × 8
##   Column1.2 Column1.3 Column1.4 Column1.5 Column1.6 Column1.7 Column1.8
##   <chr>     <chr>     <chr>     <chr>     <chr>     <chr>     <chr>    
## 1 1997      1998      1999      2000      2001      2002      2003     
## 2 15        16        17        18        19        20        21       
## 3 14        14        15        16        17        18        19       
## 4 15        16        17        18        19        20        21       
## 5 15        17        18        19        20        21        22       
## 6 12        13        15        16        16        18        18       
## # ℹ 1 more variable: Column1.9 <chr>
print(head(weights79))
## # A tibble: 6 × 2
##     pid weight
##   <dbl>  <dbl>
## 1     1 563563
## 2     2 763795
## 3     3 536272
## 4     4 565820
## 5     5 764753
## 6     6 636938
print(head(weights97))
## # A tibble: 6 × 2
##     pid weight
##   <dbl>  <dbl>
## 1     1 323197
## 2     2 272178
## 3     3 169357
## 4     4 149099
## 5     5 245150
## 6     6 218371
# Ensure the column names are correct in afqt_adjusted_final
print(colnames(afqt_adjusted_final))
## [1] "pid"      "weight"   "sample"   "age"      "afqt80"   "pafqt"    "afqt_std"
# Filter age 16 data from afqt_adjusted_final
afqt_16_nlsy79 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 0)

afqt_16_nlsy97 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 1)

# Create density plot
ggplot() +
  geom_density(data = afqt_16_nlsy79, aes(x = afqt80, weight = weight, color = "NLSY 1979"), linetype = "solid") +
  geom_density(data = afqt_16_nlsy97, aes(x = afqt80, weight = weight, color = "NLSY 1997"), linetype = "dashed") +
  labs(title = "AFQT Scores at Age 16", x = "AFQT according to 1980 definition", y = "Density") +
  scale_color_manual(name = "Sample", values = c("NLSY 1979" = "blue", "NLSY 1997" = "red")) +
  theme_minimal()


5.1 Modified Plots
The program starts by loading the necessary libraries, which include: ggplot2—system for beautiful plots, dplyr—used in data manipulation, haven—for reading and writing Stata, SAS, SPSS files, readxl—for Excel files, readr—for CSV files, and foreign one used to read other data formats. Then, the system proceeds to load a few datasets. This code loads the ‘afqt_adjusted_final.dta’ file where read_dta is a function from the ‘haven’ package. It uses read_excel from the readxl package to read in the age97.xlsx file. In addition, it uses the read_csv function from the readr package for the weights79.csv and weights97.csv files. It then filters the data to those records where age = 16, distinguishing the NLSY79 cohort (sample == 0) from NLSY97 cohort (sample == 1). This will allow us to plot AFQT scores side-by-side at the exact same age for both cohorts. The main plotting is now done using ggplot2. The ggplot() function initializes the plot, and we add density plots for both cohorts using geom_density(). First, the function aes() inside geom_density() plots the afqt80 variable on the x-axis, where the weight variable supplies the data with appropriate weights. It uses colour aesthetic to distinguish between cohorts: “NLSY 1979” is blue and “NLSY 1997” is red. Additionally, displays of density lines are made clearer since the use of line type and size make them thick by using solid for NLSY79 and dashed for NLSY97. Fill colours are with transparency added, i.e., alpha equals 0.3, so densities can be distinguished visually but not overloading the plot. The labs() function is used to add labels for title, subtitle, and axes. The meaning to the plot comes from the title “Density Plot of AFQT Scores at Age 16” and the subtitle “Comparison between NLSY 1979 and NLSY 1997 Cohorts.” The x-axis is labeled as “AFQT Score 1980 Definition,” while the y-axis is labeled as “Density.” Using the scale_color_manual() function defines user-specified colours for each cohort to make sure that there is no confusion between each one of them. The theme_minimal() function puts on the plot a very clean and minimalistic scheme. The base text size is customized to have 15 for readability. Further adjustments are then made using the theme function. This puts the plot title and subtitlecentering for a symmetric look using element_text(hjust = 0.5); adds margins to axis titles with element_text(margin = margin(t = 10)) and margin = margin(r = 10); places the legend at the top using legend.position = “top”; makes the legend title bold, element_text(face = “bold”) and ends. These modifications improve the plot’s visualization and make it more informative and engaging. Increased line thickness, fill colours with transparency, centred titles, and a minimalistic theme allow the user to create an aesthetically pleasing plot that is easy to interpret makes the distinction between the two cohorts: the NLSY79 are represented by a solid line in blue and the NLSY97 individuals are represented by the dashed red line. The titles of the title, x-axis and y-axis are all assigned using the labs function with the scale_color_manual function making the colours to be used evident. Finally, the function theme_minimal is used to provide a clean, minimalistic look to the plot.

library(ggplot2)
library(dplyr)
library(haven)
library(readxl)
library(readr)
library(foreign)

# Load datasets
afqt_adjusted_final <- read_dta("afqt_adjusted_final.dta")
age97 <- read_excel("age97.xlsx")
weights79 <- read_csv("weights79.csv")
## Rows: 12686 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
weights97 <- read_csv("weights97.csv")
## Rows: 8984 Columns: 2
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## dbl (2): pid, weight
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
# Filter age 16 data from afqt_adjusted
afqt_16_nlsy79 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 0)

afqt_16_nlsy97 <- afqt_adjusted_final %>% 
  filter(age == 16 & sample == 1)

# Create density plot
ggplot() +
  geom_density(data = afqt_16_nlsy79, aes(x = afqt80, weight = weight, color = "NLSY 1979"), 
               linetype = "solid", size = 1.2, fill = "blue", alpha = 0.3) +
  geom_density(data = afqt_16_nlsy97, aes(x = afqt80, weight = weight, color = "NLSY 1997"), 
               linetype = "dashed", size = 1.2, fill = "red", alpha = 0.3) +
  labs(title = "Density Plot of AFQT Scores at Age 16",
       subtitle = "Comparison between NLSY 1979 and NLSY 1997 Cohorts",
       x = "AFQT Score (1980 Definition)",
       y = "Density",
       color = "Cohort") +
  scale_color_manual(values = c("NLSY 1979" = "blue", "NLSY 1997" = "red")) +
  theme_minimal(base_size = 15) +
  theme(plot.title = element_text(hjust = 0.5, face = "bold"),
        plot.subtitle = element_text(hjust = 0.5),
        axis.title.x = element_text(margin = margin(t = 10)),
        axis.title.y = element_text(margin = margin(r = 10)),
        legend.position = "top",
        legend.title = element_text(face = "bold"))
## Warning: Using `size` aesthetic for lines was deprecated in ggplot2 3.4.0.
## ℹ Please use `linewidth` instead.
## This warning is displayed once every 8 hours.
## Call `lifecycle::last_lifecycle_warnings()` to see where this warning was
## generated.


6.Various Facets of the process of replication
6.1 Tools used
The study primarily relied on lecture notes provided by Prof. Dr. Stephen Huber which can found at
https://hubchev.github.io/ds/
. Additional tools used were,

1.R Studio: It served as the primary platform for coding R script and preparing report using R Markdown.

2 Online Tools: Several internet-based tool such as ChatGPT and Google Bard for effective visualization solutions.

6.2 Issues faced with replication
##6.2.1 R Language

Knowing R and R markdown: Since this was my first experience with the “R” language, I needed to understand the coding and many parameters in order to complete the replication project and produce a report.

##6.2.2 Acquiring Data

The data for the project was found in a unique DCT/DO file format. This is a specialized file format used to store and manipulate data in specific software environments. Because this was not accessible, or would not be usable for our project, the data was first translated into a text file format. The data first had to be transformed to be worked on it more easily using standard data analysis tools. The data was first converted from the text file up until this point and additionally converted into an Excel file. This last conversion added further ease in which the data could be circulated and used within a format that one would find more common. We would also be able to process and analyse the data in multiple ways in Excel. I would use the standard functionalities of spreadsheets that are common and are generally known by most all of us. I was able to re-produce the graph by writing the code that would be needed for those conversions processes. Due to this multi-step transformation, the data would be well-utilized in replicating with lots of precision the graph that is desired for the analytical needs of the project.

##6.2.3 Graphical Representation

In generating a comparative density plot of AFQT scores between the NLSY79 and NLSY97 cohorts, there were difficulties in data integration and the production of visualization. Specifically, it became hard to ensure that the combining of datasets is done properly and that the resulting plots are clear and informative. However, more challenging is working with different file formats, for example, the Stata, Excel, and CSV files, with relevant data transformations including weighting and filtering. One of the significant challenges in this project is the manipulation and integration of data from various sources and format. Proper reading of the afqt_adjusted_final.dta file containing the AFQT scores has to be combined with weight data from weights79.csv and weights97.csv files. The challenge was to filter this data properly to include only age 16 participants from both cohorts for a valid comparison. Another challenge will be the construction of a plot to show the differences in AFQT score distributions of two cohorts in an interesting and self-explanatory representation. This includes generating density plots but also managing a query aesthetics of plots, namely line types, colour, label, and themes, for clarity and readability. He would need an understanding of data manipulation and visualization techniques in R and therefore attention to detail so that the final plot represents the data correctly and communicates effective intended comparisons.

##6.2.4 Few reflections

Open Source and Collaboration: To make replication efforts smoother in the future, perhaps the researchers should themselves keep the data sets online along with the code followed in the process. Free and Open source both the article and methodology. Also, this would assist collaboration and validation within the academia, helping much in the replication process. Thorough methodological documentation: Researchers are in a position to give more thorough documentation of their techniques, thus leaving a step-by-step documentation of assumptions, parameters, and decision points. As a result, replication will not be so riddled with ambiguity.

##6.2.5 Future scopes

Other future scopes of this research include using the time variation of AFQT scores to examine their correlating trends with different socioeconomic outcomes like employment, income, and educational attainment, so as to provide insight into how the long-term impact of cognitive abilities influences economic mobility. Further investigations will also find out how effective the educational policies and programs put in place between the two cohort periods were, so that strong-effect ones on cognitive abilities and socioeconomic outcomes are promoted and ones with weak or null effects improved. Comparisons that extend to even more recent cohorts will be important in establishing trends in cognitive skills and economic outcomes as a function of continuing educational and labor market changes. Further elaboration of more complex statistical models could be envisioned that would, based on this Gregory observed data, predict future trends and outcomes by using, for example, machine learning techniques. A deep elucidation of the environmental factors—family background and community resources—shaping cognitive abilities and economic success over time would add much value to this research.

7. Make a pull request with Git and GitHub
I recently took an in-depth look at the terminal’s functionality, especially as it relates to Git and GitHub, and used what I learned to add to a project. I started by forking hubchev/make_a_pull_request as the repository. With this operation, a “make_a_pull_request” duplicate of the original repository was generated in my GitHub account. After that, I cloned my forked repository’s HTTPS URL. I started the cloning process by using the copied URL to run the git clone command in the terminal. “Cloning into’make_a_pull_request’” was displayed by the terminal to indicate that the cloning was successful.

I used the cd make_a_pull_request command to navigate into the directory once the repository had been cloned to my local computer. I used git status to make sure I was on the right branch and everything was current. It showed that my branch was in sync with ‘origin/main’. To make my modifications without affecting the master branch, I then had to create a new branch. I created and switched to a new branch called “Venkatesh_Data_Science_Project” with the command git switch -c Venkatesh_Data_Science_Project, and the terminal verified the switch.

I edited the file called I_am_a_data_scientist.md on the recently formed branch. I changed my name and the project’s details and saved the modifications. I staged these changes using the git add command, which included all of my edits, in order to get them ready for commit. I then used git commit -m “Updated I_am_a_data_scientist to my name and project details” to commit these changes along with a brief note, thereby documenting the changes in the project history.

I had to push the modifications to my forked repository on GitHub after the commit. The git push command, which uploaded my branch and its modifications, is how I accomplished this. After the modifications were uploaded to GitHub, I went to my forked repository and used the “compare and pull request” option to start a pull request. To make it obvious what kind of work I had contributed, I titled the pull request “VenkateshKannan - Four Facts about Human Capital”. The pull request is now undergoing review and can be found in the original repository, hubchev/make_a_pull_request. The repository maintainer has to approve and incorporate my modifications into the main project as the last stage.

8. Publishing presentation in Github
It is in this regard that Git and GitHub offer tremendous advantages with respect to collaboration, code review, and project management. These techniques contribute to the effectiveness of software development. On the other hand, it fosters collaboration with colleagues, so GitHub is relevant to any person who wants to become a programmer. The detailed instructions to be found on the GitHub account of Professor Dr. Stephan Huber—hubchev/ds_summer23 [https://github.com/hubchev/ds_summer23%5D—summarize the submission process. Below is a quick explanation of our process: 1. The creation of GitHub account and installed Git using the link which i got in online.

2. I created the Repository (Data_Science_Projects) were I can upload the standalone html and other related files to present.

3. I committed changes in github in my repository and observed the changes.

4. With official username name of GitHub and adding Project repository name, I created website html file (https://github.com/VenkateshKannan1999/VenkateshKannan1999.github.io).

5. At last I published the files related to project in the repository of my GitHub.

#9.Conclusion

The research in this project takes a closer look at AFQT scores pioneered at age 16 years within the major data files of the NLSY79 and NLSY97 cohorts. These differences reflect questions about the shifts in cognitive abilities across these generational groups. By collating information from multiple sources using stringent statistical methods, we have arrived at meaningful insights into how such abilities may vary and eventually cause economic consequences.

Our findings point out a clear time trend in AFQT scores between the two cohorts, probably as a result of the dynamics of educational systems, societal values, and economics over this twenty-year period. The results are weighted with the representative weight data and based on age-adjusted AFQT scores; hence, they are valid and comparable.

These differences matter for policymakers and educators in that they put forward an evolution of cognitive abilities among the same birth cohort—thereby implicating a need for specific educational interventions along the life course. Better understanding of these trends might support the setting of policies aiming to compensate for weaknesses or further support strengths of birth cohorts and contribute to better economic outcomes.

Future research should focus on the extension of results obtained to later-born cohorts and further changes in cognitive skills with their economic consequences. Applying more sophisticated statistical models or machine learning methods may lead to deeper insights and better predictions. It is also worth taking into consideration factors such as family background and community resources that interact with environmental factors in influencing mental abilities and economic success. In this regard, only a comprehensive approach will yield effective policy solutions. The current research concludes that there are essential generational differences in cognitive abilities, proves a robust methodological framework for further study, and calls for continuous monitoring with a view to appropriate interventions along the course of development in search of enhanced cognitive and economic equity.

10. Affidavit
I hereby affirm that this submitted paper was authored unaided and solely by me. Additionally, no other sources than those in the reference list were used. Parts of this paper, including tables and figures, that have been taken either verbatim or analogously from other works have in each case been properly cited with regard to their origin and authorship. This paper either in parts or in its entirety, be it in the same or similar form, has not been submitted to any other examination board and has not been published.

I have read the Handbook of Academic Writing by Hildebrandt & Nelke (2019) and have endeavored to comply with the guidelines and standards set forth therein.

I acknowledge that the university may use plagiarism detection software to check my thesis. I agree t o cooperate with any investigation of suspected plagiarism and to provide any additional information or evidence requested by the university.

The report includes:

… 4000 words (+/- 500).
… a title page with personal detail (name, email, matriculation number).
… an abstract.
… a bibliography that was created using BibTeX applying an APA citation style.
… the complete R code that is necessary to replicate your results.
… Detailed instructions on data acquisition and importation into R.
… An introduction to guide the reader and a conclusion summarizing the work and discussing potential future extensions.
… All significant resources used in the report and R code development.
… the filled out Affidavit.
…A concise description of the successful use of Git and GitHub, as detailed here: make_a_pull_request.
… A concise description of the presentation published on GitHub.
The project submission includes:

… The .qmd file(s) of the report.
… The quarto.yml file of the report.
… The .pdf file of the report.
… The standalone .html file of the report.
… All necessary files (not available online) to reproduce the report and the R code.
… The standalone .html file of the presentation.
(Venkatesh Kannan) (22.07.2024,) (Cologne,Germany)
