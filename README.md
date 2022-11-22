<h1 align="center"><strong>Streaming Analysis</strong></h1>

# Introduction
In this notebook, I'll take a look at my streaming viewing history data from Hulu, Netflix, and Prime Video accounts. I will merge these datasets with an additional dataset that contains more information about the streaming titles like run time, genres, and Imdb score. This will enable me to gain more insight into my streaming history.

### Changes to the Project Plan
I turned in my Project Plan when I only had my Netflix data. Since then, I've able to obtain my Hulu and Prime Video data.

My original idea was to compare my streaming data to the top streaming titles but I wasn't able to find a dataset that worked with my data.

### Project Challenges
I realized (too late for this project) that Netflix and Prime Video create a new "watch event" every time a stream is paused and played again. This means that my data shows individual titles with artificially high watch counts. I made the decision not to remove the duplicates because doing so would have removed genuine new watch events and I would rather go through the datasets myself to determine which ones to delete.

I removed more data from my streaming viewing history than I would have liked in order to combine them. While Hulu had the best data because it did not count each pause as a new "watch event", the downside was the data came split over multiple PDFs and would have required far more time to clean. I made the decision to stick with the basic data from each streaming service on the basis of time.  

I struggled finding an additional dataset that worked with my combined streaming viewing history data. In the end, I stuck with the one that gave me the largest merged dataset. I know I could have used just the three streaming datasets but I wanted the challenge of merging additional data. 

# Datasets Used
### Personal Streaming Viewing History
<ul>
  <li>Hulu</li>
  <li>Netflix</li>
  <li>Prime Video</li>
</ul>

### Additional dataset
[Kaggle - Netflix, Movies, and Popularity](https://www.kaggle.com/code/advaypatil/netflix-movies-and-popularity/data)

# How to Run this Project
`Using a Virtual Environment`
  1. Clone this repo git clone https://github.com/istarlet/streaming_analysis.git
  2. Create a new folder in the cloned repo called `datasets` 
  3. Download the datasets [here](https://drive.google.com/drive/folders/1kDuL7BR_Rc3V7Fl5HHSQg8jn4fChZEP3?usp=share_link) and add the downloaded datasets to the            `datasets` folder *<strong>See note</strong>* 
  4. CD into cloned project folder
  5. Install virtual venv if you don't already have it installed `pip install virtualenv`
  6. Activate the virtual environment (see intructions [here](https://github.com/istarlet/streaming_analysis/blob/main/README.md#activating-a-virtual-environment)) 
  7. Install the requirements.txt file `pip install -r requirements.txt`
  8. Then run these Juptyer Notebook files: [Hulu](hulu.ipynb), [Imdb](imdb.ipynb), [Netflix](netflix.ipynb), [Prime Video](prime_video.ipynb) BEFORE running the main      project notebook [Streaming Data](streaming_data.ipynb)

*(**Note:** If you downloaded the dataset as a .zip file, make sure to add the individual datasets to the new `datasets` folder and not the folder they were zipped in.)*

### Activating a Virtual Environment
**On Mac/Linux**

Open the Terminal and create a virtual environment with the command `python3 -m venv virtual-env`

Activate the virtual environment with the command `source virtual-env/bin/activate`

**On Windows**

Open the Command Prompt and create a virtual environment with the command `python -m venv virtual-env`

Activate the virtual environment with the command `virtual-env\Scripts\activate.bat`
 
### Deactivate the Virtual Environment
  Type`deactivate`

### Python packages used in this project:
<ul>
  <li>datetime</li>
  <li>matplotlib</li>
  <li>pandas</li>
  <li>seaborn</li>
</ul>

# Project Requirements
## 1. Loading data - Feature 1 
`Read TWO data files (JSON, CSV, Excel, etc.).`

I read in four CSV files. 
<ul>
  <li>AshleyViewingActivity.csv</li>
  <li>DigitalPrimeVideoViewingHistory.csv</li>
  <li>HuluViewingHistoryUpdated.csv</li>
  <li>titles.csv</li>
</ul>

## 2. Clean and operate on the data while combining them - Feature 2
`Clean your data and perform a pandas merge with your two data sets, then calculate some new values based on the new data set.`

I cleaned the each dataset in their own Jupyter Notebook.

   [Hulu](hulu.ipynb)
   [Imdb](imdb.ipynb)
   [Netflix](netflix.ipynb)
   [Prime Video](prime_video.ipynb)

I then concatonated the Hulu, Netflix, and Prime Video datasets together. 

With my new combined streaming dataset, I merged it with the Imdb dataset.

I added new columns to the merged dataset by extracting the day, month, and hour from the "Date Watched" column.

## 3. Visualize / Present your data - Feature 3
`Make 3 matplotlib or seaborn (or another plotting library) visualizations to display your data.`
![image](https://user-images.githubusercontent.com/14065849/202565871-15b3fb4f-5275-4898-9ea7-8b613501426a.png)

![image](https://user-images.githubusercontent.com/14065849/202619291-4d34a9bb-d6f8-490a-aec2-14ca83cc3ea2.png)

![image](https://user-images.githubusercontent.com/14065849/202738193-be0a83ec-76b2-40b5-9939-bbbf02823c0b.png)

![image](https://user-images.githubusercontent.com/14065849/202563724-0d5363c0-f27d-4197-be3a-1206d24f0537.png)

![image](https://user-images.githubusercontent.com/14065849/202564792-ed918b3d-d55f-4879-8557-8e06915ae14e.png)

![image](https://user-images.githubusercontent.com/14065849/202758780-65884f91-2fa5-4588-b02b-94f634869680.png)

![image](https://user-images.githubusercontent.com/14065849/202563856-1bc221d6-385f-437c-a5aa-6f9ec231a6ae.png)

## 4. Best practices - Feature 4
`Utilize a virtual environment and include instructions in your README on how the user should set one up`

I created a virtual environment with instructions in the [How to Run this Project](https://github.com/istarlet/streaming_analysis/blob/main/README.md#how-to-run-this-project) section.

## 5. Interpretation of your data - Feature 5
`Annotate your code with markdown cells in Jupyter Notebook, write clear code comments, and have a well-written README.md.`

In my Jupyter Notebooks, I annotated my code with markdown cells and wrote clear code comments. I have included a README.md.  
