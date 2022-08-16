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
