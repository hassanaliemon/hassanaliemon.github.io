## Download kaggle files directly into your colab
Only for newbie(Who never done it before):
- go to the competition page and click Rules
- click I understand and agree and do the procedure
- click data
- click I understand and agree

1. If you are in colab:<br/>
``` !pip install --upgrade --force-reinstall --no-deps kaggle ``` <br/>
If in your local machine: <br/>
``` !pip install kaggle ```
2. go to your account and scroll to API section and click Create New API Token
	It will download kaggle.json file to your local machine
3. Upload That file in colab using this command
```python 
from google.colab import files
  files.upload()```
  and upload the kaggle.json file
4. Copy the json file
```! cp kaggle.json ~/.kaggle/```
5.  Change the permissions of the file!
```!chmod 600 ~/.kaggle/kaggle.json```
6.  Now go to the data section of the competition page and copy the download command. 
	For this page: https://www.kaggle.com/c/expedia-hotel-recommendations/ 
	it is:
	```!kaggle competitions download -c expedia-hotel-recommendations```

Now unzip the file using unzip command and enjoy your experiment!
