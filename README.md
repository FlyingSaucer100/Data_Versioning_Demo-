# Data_Versioning_Demo-
Repository to Demo Data Versioning 

- Get the initial dataset:
 
`dvc get https://github.com/iterative/dataset-registry \
                                    tutorials/versioning/data.zip`
                                    
- Add the dataset 

`dvc add data/`

- Tell git not to track the data/ directory

`git add data.dvc .gitignore` 

- Commit and tag the data version as v1.0 

`git commit -m "Initial data version"`

`git tag -a "v1.0" -m "Data v1.0"`

**Get the new dataset**
 
`dvc get https://github.com/iterative/dataset-registry \
                                    tutorials/versioning/new-labels.zip`
                                    
- Add the dataset 

`dvc add data/`

- Tell git not to track the data/ directory

`git add data.dvc .gitignore` 

- Commit and tag the data version as v1.0 

`git commit -m "Initial data version"`

`git tag -a "v2.0" -m "Data v2.0"`

**Switch between versions**

`git checkout v1.0 \n
dvc checkout \n
dvc status 
` 
