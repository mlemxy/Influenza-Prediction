# Influenza Outbreak Prediction

Developed for [Code Without Barriers](https://cwb2023.devpost.com/forum_topics/37297-hcltech)'s hackathon, this project aims to predict influenza outbreaks in different regions based on historical data and various factors by analyzing previous patterns and trends in the provided dataset.



## Dataset

The [dataset](https://data.world/chhs/fc544658-35c5-4be0-af20-fc703bc57c13) used, "clinical-sentinel-laboratory-influenza-and-other-respiratory-virus-surveillance-data-by-region-and-influenza-season.csv," provides past information on the percentage of cases tested positive and is affected by variables such as season, date, region, etc.

Since there was no target variable, I used the following code to determine if the number of cases is considered an outbreak:
```
# define threshold to determine yes/no outbreak, in this case i set if >= 100 then considered outbreak
df["Outbreak"] = df["Number_Positive"].apply(lambda x: 1 if x >= 100 else 0)
```

## How to use

To clone and run this application, you will need Git:

1. Clone the repository:

```
$ git clone https://github.com/mlemxy/Influenza-Prediction

# create virtual env
py -m venv .venv
.venv\scripts\activate

# install dependencies
$ pip install -r requirements.txt
```

