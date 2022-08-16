# MLOps Git+DVC

## When data is too big for Git

### DVC

1. Create Folder on Google Drive
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/create_folder.png)

2. Init the DVC
    ``` bash
    dvc init
    ```
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/dvc_init.png)

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
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/get_data.py.png)


6. add dvc
   ``` bash
   dvc add data.csv
   ```
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/dvc_add.png)
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/dvc_csv.png)

7. Start Tracking Data
   ``` bash
   git add data.csv.dvc .gitignore
   git commit -m "tracking data"
   git push
   ```
    ![](https://raw.githubusercontent.com/fiqgant/MLOps-Git-DVC/main/Images/tracking%20data.png)

8. push dvc
   ``` bash
   dvc push
   ```

### Download dataset with DVC
``` bash
dvc pull data.csv
```