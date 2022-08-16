# MLOps Git+DVC

## When data is too big for Git

### DVC

1. Create Folder on Google Drive

2. Init the DVC
    ``` bash
    dvc init
    ```

3. add remote dvc
    ``` bash
    dvc remote add -d myremote gdrive://<link google drive folder>
    ```

4. git add, commit and push
    ``` bash
    git add .
    git commit -m "first commit"
    git push
    ```

5. get dataset
    ``` bash
    python get_data.py
    ```

6. add dvc
   ``` bash
   dvc add data.csv
   ```

7. Start Tracking Data
   ``` bash
   git add data.csv.dvc .gitignore
   git commit -m "tracking data"
   git push
   ```

8. push dvc
   ``` bash
   dvc push
   ```

### Download dataset with DVC
``` bash
dvc pull data.csv
```