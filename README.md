# Análise dos candidatos a deputados no pleito de 2014

## Summary

* [Goal](#goal)
* [Project Development](#project-development)
* [Development Environment](#environment)
* [Dataset](#dataset)
* [Project Structure](#structure)

<h2 id='goal'>Goal</h2>

The goal this analysis is to obtain insights on the data of the Wiki Challange and to 
predict if a user is likely to contribute again after an update was reverted. 

<h2 id='project-development'>Project Development</h2>

The project was started by making some exploratory analysis on the datasets described on the section [Dataset](#dataset). All insights can be seen on the [Insights](#insights) section. 

<h2 id='environment'>Development Environment</h2>

This analysis was made using Python 3.7.

Create an virtualenv using either virtualenv or conda. Example using conda:

`$ conda create -n wiki python=3.7`

Then install the requirements using *pip*:

`$ pip install -r requirements.txt`


<h2 id='dataset'>Dataset</h2>

The data is available [on this kaggle page](https://www.kaggle.com/eliezerfb/candidatos-deputado-federal-e-estadual-2014).
Dataset was divided into 5 separated files.

* Categories
* Comments
* Edits
* Namespaces
* Titles

For this project, only the file `edits.tsv` was used for the purpose of this analysis. The file `comments.tsv` were used for a brief insight analysis, to see the possibility of adding comments as a feature.

The dataset `edits.tsv` constituted of 22,126,031 records of edition and 11 columns of information. Not all columns had metadata about them, neither on Kaggle website nor on other pages available from the webpage. 
The list of information and its metadata that were available can be observed below:

| Name                 | Detail                                  | Type of Data |
|----------------------|-----------------------------------------|--------------|
| user_id              | Number of the user that did the editing | Integer      |
| article_id           | Identifier of the article edited        | Integer      |
| revision_id          | Identifier of the number of revision    | Integer      |
| namespace            | -                                       | Integer      |
| timestamp            | Moment when the article was edited      | Datetime     |
| md5                  | -                                       | Integer      |
| reverted             | Flag if the edit was reverted           | Bool         |
| reverted_user_id     | -                                       | Integer      |
| reverted_revision_id | -                                       | Integer      |
| delta                | -                                       | Integer      |
| cur_size             | -                                       | Integer      |


<h3 id='structure'> Project Structure</h3>

This project was divided in two main folders: 

* **data**: all available data
* **notebook**: all notebooks used on this project

```
|-- README.md
|
|-- data
|   |-- candidates.csv
|-- notebooks
|   |-- analysis.ipynb
|   
`-- requirements.txt
```
