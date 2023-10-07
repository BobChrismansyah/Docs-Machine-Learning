### Open Project

Slide is underconstruction


Repositori ini dibuat menggunakan [MkDocs](www.mkdocs.org/) dengan bantuan 

langkah langkah menjalankan di lokal


```
git clone https://github.com/BobChrismansyah/Docs-Machine-Learning.git
```

```
cd Docs-Machine-Learning
```

```
pip install -r requirements.txt
```



run:
```
mkdocs serve
```

>open in http://127.0.0.1:8000/

<br>

### File Strucure


```bash
< PROJECT ROOT >
   |
   |-- Dataset/
   |    |
   |    |-- datatraining.csv               # A dataset file using in ipynb folder
   |    |-- occupancy_data.zip             # Zip file for occupancy cataset training
   |    |
   |-- docs/                               # Directory for docs site
   |    |-- docs/                          # Directory for docs chapter
   |    |    |-- churn-prediction   
   |    |    |    |-- index.md
   |    |    |-- clustering
   |    |    |    |-- index.md
   |    |    |-- desicion-tree
   |    |    |    |-- index.md
   |    |    |-- logistic-regression
   |    |    |    |-- index.md
   |    |    |-- naive-bayes
   |    |    |    |-- index.md
   |    |    |-- neural-network
   |    |    |    |-- index.md
   |    |    |-- pandas
   |    |    |    |-- index.md
   |    |    |-- index.md
   |    |-- about.md
   |    |-- index.md
   |-- img/                                # nothing
   |-- ipynb/                              # Directory for ipynb file
   |    |-- occupancy.ipynb                # A ipynb file for datatraining.csv dataset training
   |-- theme/                              # Theme, ignore it
   |
   |-- mkdocs.yml                          # Configuration for mkdocs
   |-- requirements.txt                    # Development modules
   |
   |-- ************************************************************************
```
