## ML Workspace
This branch is for creating Ainize Workspace images for machine learning developers or machine learning researcher.

### Development Extension
- [Jupyter Notebook and Lab](https://jupyter.org/)
- [Visual Studio Code](https://github.com/cdr/code-server)
- [Terminal - ttyd](https://github.com/tsl0922/ttyd)

### Major Package List
```
Package                           Version
--------------------------------- ------------
nltk                              3.2.5
numpy                             1.19.5
pandas                            1.3.3
Pillow                            7.1.2
scikit-learn                      0.22.2.post1
scipy                             1.4.1
tensorflow                        2.6.0
torch                             1.9.0
xgboost                           0.90
```

### How to Test Your Image
Build Docker Image
```bash
docker build -t <image-name> .
```
Run Docker
```bash
docker run -d -p 8000:8000 -p 8010:8010 -p 8020:8020 <image-name>
```
Run Docker with Password
```bash
docker run -d -p 8000:8000 -p 8010:8010 -p 8020:8020 -e PASSWORD=<password> <image-name>
```
Run Docker with Github Repo
```bash
docker run -d -p 8000:8000 -p 8010:8010 -p 8020:8020 -e GH_REPO=<github-repo> <image-name>
```
Run Docker with password and Github Repo
```bash
docker run -d -p 8000:8000 -p 8010:8010 -p 8020:8020 -e PASSWORD=<password> -e GH_REPO=<github-repo> <image-name>
```

* Jupyter Notebook : http://server-address:8000/
* Visual Studio Code : http://server-address:8010/
* Terminal - ttyd : http://server-address:8020/

### How to use my custom image in Ainize Workspace
Do you want to use the image you created? If so, please follow the instructions.
1. Click the "Create your workspace" button on the [Ainize Workspace page](https://ainize.ai/workspace).
2. As the Container option, select "Import from github".
3. Click the "Start with repo url" button.
4. Put "https://github.com/ainize-workspace-collections/ml-workspace" in "Enter a Github repo url". And select the "2021.09-dev" branch.
5. Select the required tool(s) and click the OK button.
6. Click "Start my work" after selecting the machine type.
Now, enjoy your own Ainize Workspace! 🎉